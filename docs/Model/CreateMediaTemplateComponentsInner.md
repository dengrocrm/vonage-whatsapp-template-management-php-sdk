# # CreateMediaTemplateComponentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The type of template component. &#x60;HEADER&#x60;, &#x60;FOOTER&#x60;, and &#x60;BUTTONS&#x60; are optional, a &#x60;BODY&#x60; is always a required component of a template. | [optional]
**format** | **string** | The format of the template component. Where &#x60;type&#x60; is &#x60;HEADER&#x60; can be &#x60;TEXT&#x60;, &#x60;IMAGE&#x60;, &#x60;DOCUMENT&#x60;, or &#x60;VIDEO&#x60;. Where type is &#x60;BODY&#x60; or &#x60;FOOTER&#x60;, must be &#x60;TEXT&#x60;. | [optional]
**text** | **string** | The text to be displayed in this template component. EIther &#x60;plain text&#x60; or &#x60;text with placeholders {{1}}&#x60;. **Note: when using text with placeholders, you must include the &#x60;example&#x60; parameter in the component object.** | [optional]
**example** | [**\DengroCrm\VonageWhatsAppTemplateManagement\Model\CreateMediaTemplateComponentsInnerExample**](CreateMediaTemplateComponentsInnerExample.md) |  | [optional]
**buttons** | [**\DengroCrm\VonageWhatsAppTemplateManagement\Model\CreateMediaTemplateComponentsInnerButtonsInner[]**](CreateMediaTemplateComponentsInnerButtonsInner.md) | Where &#x60;type&#x60; is set to &#x60;BUTTONS&#x60;, an array of button objects representing the properties of each button. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
