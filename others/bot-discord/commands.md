# Commands

Tạo cấu trúc thư mục /commands

Tạo file command tương ứng, vd: ping.js

````
```javascript
const { SlashCommandBuilder } = require('discord.js');

module.exports = {
	data: new SlashCommandBuilder()
		.setName('ping')
		.setDescription('Provides information about ping test'),
	async execute(interaction) {
		// interaction.user is the object representing the User who ran the command
		// interaction.member is the GuildMember object, which represents the user in the specific guild
    const timeTaken = Date.now() - interaction.createdTimestamp;
		await interaction.reply(`Pong! This message had a latency of ${timeTaken}ms.`);
	},
};
```
````

Bổ sung code ở app.js để đăng ký command với bot

````
```javascript
//commands
client.commands = new Collection();
const commands = [];
const infoBot = {
  token: config.BOT_TOKEN_HBOT,
  clientId: "1079594093136576592",//application id
  guildId: "1079308068199866428"//right click server copy
}
// Grab all the command files from the commands directory you created earlier
const commandsPath = path.join(__dirname, 'commands');
const commandFiles = fs.readdirSync(commandsPath).filter(file => file.endsWith('.js'));

// Grab the SlashCommandBuilder#toJSON() output of each command's data for deployment
for (const file of commandFiles) {
	const command = require(`./commands/${file}`);
	commands.push(command.data.toJSON());
  if ('data' in command && 'execute' in command) {
		client.commands.set(command.data.name, command);
	} else {
		console.log(`[WARNING] The command at ${filePath} is missing a required "data" or "execute" property.`);
	}
}

// Construct and prepare an instance of the REST module
const rest = new REST({ version: '10' }).setToken(infoBot.token);

// and deploy your commands!
(async () => {
	try {
		console.log(`Started refreshing ${commands.length} application (/) commands.`);

		// The put method is used to fully refresh all commands in the guild with the current set
		// const data = await rest.put(
		// 	Routes.applicationGuildCommands(infoBot.clientId, infoBot.guildId),
		// 	{ body: commands },
		// );

    //global command
    const data = await rest.put(
			Routes.applicationCommands(infoBot.clientId),
			{ body: commands },
		);

		console.log(`Successfully reloaded ${data.length} application (/) commands.`);
	} catch (error) {
		// And of course, make sure you catch and log any errors!
		console.error(error);
	}
})();


client.on(Events.InteractionCreate, async interaction => {	
  if (!interaction.isChatInputCommand()) return;
	console.log("interaction",interaction.commandName);  
  const command = interaction.client.commands.get(interaction.commandName);

	if (!command) {
		console.error(`No command matching ${interaction.commandName} was found.`);
		return;
	}

	try {
		await command.execute(interaction);
	} catch (error) {
    console.log("error!")
		// console.error(error);
		// if (interaction.replied || interaction.deferred) {
		// 	await interaction.followUp({ content: 'There was an error while executing this command!', ephemeral: true });
		// } else {
		// 	await interaction.reply({ content: 'There was an error while executing this command!', ephemeral: true });
		// }
	}
});
```
````

