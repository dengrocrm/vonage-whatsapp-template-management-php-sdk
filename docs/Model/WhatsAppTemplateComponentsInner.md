# # WhatsAppTemplateComponentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The type of template component. | [optional]
**format** | **string** | The format of the template component. Where &#x60;type&#x60; is &#x60;HEADER&#x60; can be &#x60;TEXT&#x60;, &#x60;IMAGE&#x60;, &#x60;DOCUMENT&#x60;, or &#x60;VIDEO&#x60;. Where type is &#x60;BODY&#x60; or &#x60;FOOTER&#x60;, must be &#x60;TEXT&#x60;. | [optional]
**text** | **string** | The text to be displayed in this template component. EIther &#x60;plain text&#x60; or &#x60;text with placeholders {{1}}&#x60;. | [optional]
**buttons** | [**\DengroCrm\VonageWhatsAppTemplateManagement\Model\TemplateComponentButtonsButtonsInner[]**](TemplateComponentButtonsButtonsInner.md) | An array of objects representing button components. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
