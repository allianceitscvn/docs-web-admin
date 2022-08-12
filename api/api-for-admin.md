# Api for Admin

## Summary

* FirstSetting
* Login
* LoginSocial
* CategoryScreenList
* ProjectScreens
* AppScreenUIControlSetting

## Details

{% swagger method="post" path="/GlobalAppSetting/FisrtSetting" baseUrl="domain" summary="Lấy thông tin config default" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="UIAppConfig" type="Json" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-javascript"><code class="lang-javascript">{
    Data: {
<strong>        BackgroundUrl: "content/img/bg/backgound.png",
</strong>        DefaultHomeURL: null,
        DefaultValues: {},
        IsNeedCheckChangePass: false,
        LanguageList: [],
        MediaAcceptedType:"gif,.GIF,.jpg,.JPG,.jpeg,.JPEG,.png,.PNG,.doc,.DOC,.docx,.docx,.xls,.XLS,.xlsx,.xlsx,.pdf,.PDF,.txt,.TXT,.dwg,.DWG,.sql,.json,.HEIC,.HEIF,.HEVC",
        Message_IsNeedChangePass: "",
        PublicApiScreenList: [],
        TextDisplaySettings: [],
        UIAppConfig: {}
    },
    EndTime: 0,
    ExtraData: null,
    Msg: "",
    MsgShowInUI: null,
    StartTime: 0,
    StatusCode: 1,
    TotalMili: 0,
}
</code></pre>
{% endswagger-response %}
{% endswagger %}  

{% swagger method="post" path="/oauth2/token" baseUrl="domain" summary="Kiểm tra thông tin đăng nhập" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="UIAppConfig" type="Json" %}

grant_type: 
username: String
password: String
app_name: 

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-javascript"><code class="lang-javascript">{
    Data: {
      access_token: "eyJhbGciOiJIUzI1NiIsInR5cC…”,
      appLogo_background: "",
      appLogo_url:",
      app_menu: "[{\"NewWindow\":true,\"FilterString\":\"my screen\",\"Children\":null,\"OrderNo\":0,\"Name\":\"My            Screen\",\"Code\":\"DM_SCREEN_4_MOBILE\",\"Url\":\"/config-screen-4-mobile\"}]",
avatar_url: "",
configs: "{\"home_url\":\"/pos-bill\"}",
expires_in: 1689642662000,
fa2_method: "",
fa2_needenable: false,
fa2_needverify: false,
fa2_token: null,
name: "Dung Bui Test",
project_screens: "[]",
project_screens_inactive: "[]",
token_type: "Bearer",
user_id: "5",
user_mobile: "",
user_name: "dung.buiminh@allianceitsc.com",
user_type: "",
user_uniqueid: "14bc716d-1f79-4857-9ed5-ae74c842ddce"
}


</code></pre>
{% endswagger-response %}
{% endswagger %}
