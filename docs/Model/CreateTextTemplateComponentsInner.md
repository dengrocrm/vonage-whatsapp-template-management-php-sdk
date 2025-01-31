# # CreateTextTemplateComponentsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The type of template component. &#x60;HEADER&#x60;, &#x60;FOOTER&#x60;, and &#x60;BUTTONS&#x60; are optional, a &#x60;BODY&#x60; is always a required component of a template. | [optional]
**format** | **string** | The format of the template component. For a Text Template, &#x60;format&#x60; is always &#x60;TEXT&#x60; for &#x60;HEADER&#x60;, &#x60;BODY&#x60; or &#x60;FOOTER&#x60; components. | [optional]
**text** | **string** | The text to be displayed in this template component. EIther &#x60;plain text&#x60; or &#x60;text with placeholders {{1}}&#x60;. | [optional]
**example** | [**\OpenAPI\Client\Model\CreateTextTemplateComponentsInnerExample**](CreateTextTemplateComponentsInnerExample.md) |  | [optional]
**buttons** | [**\OpenAPI\Client\Model\CreateTextTemplateComponentsInnerButtonsInner[]**](CreateTextTemplateComponentsInnerButtonsInner.md) | Where &#x60;type&#x60; is set to &#x60;BUTTONS&#x60;, an array of button objects representing the properties of each button. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
