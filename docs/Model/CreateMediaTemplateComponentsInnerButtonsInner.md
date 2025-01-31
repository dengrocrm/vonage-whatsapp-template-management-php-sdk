# # CreateMediaTemplateComponentsInnerButtonsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The type of button. | [optional]
**text** | **string** | The text to appear on the button. | [optional]
**otp_type** | **string** | The type of OTP button. Mandatory if the button &#x60;type&#x60; is &#x60;OTP&#x60; | [optional]
**autofill_text** | **string** | Mandatory if &#x60;otp_type&#x60; is &#x60;ONE_TAP&#x60; | [optional]
**package_name** | **string** | Your Android app&#39;s package name. Mandatory if &#x60;otp_type&#x60; is &#x60;ONE_TAP&#x60; | [optional]
**signature_hash** | **string** | Your app signing key hash. See [App Signing Key Hash](https://developers.facebook.com/docs/whatsapp/business-management-api/authentication-templates#app-signing-key-hash). Mandatory if &#x60;otp_type&#x60; is &#x60;ONE_TAP&#x60; | [optional]
**url** | **string** | A URL to which the end-user will be directed when hitting the button. Must be set when &#x60;type&#x60; is &#x60;URL&#x60;. | [optional]
**phone_number** | **string** | Phone number to which a phone call would be placed by the end-user when hitting the button. Must be set when &#x60;type&#x60; is &#x60;PHONE_NUMBER&#x60;. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
