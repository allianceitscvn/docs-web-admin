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
