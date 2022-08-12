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

{% swagger method="post" path="/oauth2/token" baseUrl="domain" summary="Login - Kiểm tra thông tin đăng nhập" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="UIAppConfig" type="Json" %}
{  
    "username": "dung.buiminh@allianceitsc.com",  
    "password": "123$56"  
}  
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-javascript"><code class="lang-javascript">{
    Data: {
      access_token: "eyJhbGciOiJIUzI1NiIsInR5cC…”,
      appLogo_background: "",
      appLogo_url:",
      app_menu: "[{\"NewWindow\":true,\"FilterString\":\"my screen\",\"Children\":null,\"OrderNo\":0,\"Name\":\"My                Screen\",\"Code\":\"DM_SCREEN_4_MOBILE\",\"Url\":\"/config-screen-4-mobile\"}]",
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
}
</code></pre>
{% endswagger-response %}
{% endswagger %}
  
  
{% swagger method="post" path="/MyProfileUserPassword/CheckNeedChangePassword" baseUrl="domain" summary="Login - CheckNeedChangePassword" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="UIAppConfig" type="Json" %}
{}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-javascript"><code class="lang-javascript">{
   Data: {
      DocumentWidth: 0,
      IM_CreatedBy: null,
      IM_CreatedDate: null,
      IM_UpdatedBy: null,
      IM_UpdatedDate: null,
      Id: null,
      IsNeedChangePassword: false,
      LastDayUpdatePassword: null,
      Msg: null,
      UI_StartAt: null,
      Url: null,
      UserId: null,
   }
   EndTime: 1658106662647.8853,
   ExtraData: null,
   Msg: "",
   MsgShowInUI: null,
   StartTime: 1658106662646.6348,
   StatusCode: 1,
   TotalMili: 1.25048828125,
}
</code></pre>
{% endswagger-response %}
{% endswagger %}  
  
  
{% swagger method="post" path="/ConfigMenu/CategoryScreenList" baseUrl="domain" summary="Login - Lấy thông tin các url của ui" %}
{% swagger-description %}
{% endswagger-description %}

{% swagger-parameter in="body" name="UIAppConfig" type="Json" %}
{}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-javascript"><code class="lang-javascript">{
   Data: [
    {
        APIName: "UserAccount",  ,  
        Config: null,  
        Id: "a25607e3-11ad-4156-b25d-52a0bbbf9d72",  
        RequestData: null,  
        ScreenCode: "DM_USER_ACCOUNT",  
        Title: "Account Login",  
        Type: "SIDE_MENU",  
        UIType: null,  
        UIUrl: "/config-account-login"
     } 
   ]
}
</code></pre>
{% endswagger-response %}
{% endswagger %}  
  
  
{% swagger method="post" path="ProjectScreenHeader/ProjectScreens" baseUrl="domain" summary="Lấy thông tin project screen" %}
{% swagger-description %}
{% endswagger-description %}

{% swagger-parameter in="body" name="UIAppConfig" type="Json" %}
{}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-javascript"><code class="lang-javascript">{
   Data: [
    {
        APIName: "UserAccount",    
        Config: null,  
        Id: "a25607e3-11ad-4156-b25d-52a0bbbf9d72",  
        RequestData: null,  
        ScreenCode: "DM_USER_ACCOUNT",  
        Title: "Account Login",  
        Type: "SIDE_MENU",  
        UIType: null,  
        UIUrl: "/config-account-login"
     } 
   ]
}
</code></pre>
{% endswagger-response %}
{% endswagger %}  
  
  
{% swagger method="post" path="AppScreenUIControlSetting/Options" baseUrl="domain" summary="Lấy thông tin UIControlSetting" %}
{% swagger-description %}
{% endswagger-description %}

{% swagger-parameter in="body" name="UIAppConfig" type="Json" %}
{  
"ScreenGUID": "07feaab5-78e8-401f-ade5-0ef3944524f3"  
}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
<pre class="language-javascript"><code class="lang-javascript">{
   Data: {  
        ButtonList: [],
        ChartConfig: null,
        Configs: {},
        DiagramChart: null,
        FormAddNewConfig: null,
        HeaderConfig: {
            Avatar: null,
            ButtonList: [],
            Title: null,
        },
        PageConfig: {  
            APIMethod: null,
            APIName: "AppScreenUIControlSetting",
            Config: "",
            ConfigsExt: null,  
        },  
        Contents: [
            APIMethod: null,
            APIName: "Bill",
            Config: "",
            ConfigsExt: null,
            Contents: null,
            Id: "ui-ctrl-290",
            RequestData: null,
            ScreenCode: "ALLIANCE_POS_BILL",
            Title: "Bán hàng",
            Type: null,
            UIType: "Table",
            UIUrl: null,
        ],
        Id: "07feaab5-78e8-401f-ade5-0ef3944524f3",
        RequestData: null,
        ScreenCode: "ALLIANCE_POS_BILL",
        Title: "Bán hàng",
        Type: "SIDE_MENU",
        UIType: "Tab",
        UIUrl: null,
        Signature: null,
    },
}
</code></pre>
{% endswagger-response %}
{% endswagger %}  
