# # WhatsAppTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The unique identifier for this template. | [optional]
**name** | **string** | The name of the template | [optional]
**language** | **string** | The language of the template. The same template name can be used for multiple language versions. A list of supported languages is available in the [WhatsApp documentation](https://developers.facebook.com/docs/whatsapp/api/messages/message-templates/) | [optional]
**status** | **string** | The status of the template. Templates with a status of &#x60;APPROVED&#x60; can be used in WhatsApp template messages. | [optional]
**category** | **string** | The category of the template. This determines the purpose of the template. Note: until June 1st 2023 some older template categories may be listed. These should be updated to one the valid categories or they will be automatically migrated. | [optional]
**previous_category** | **string** | If the template has been updated to a different category, shows the previous category of the template. | [optional]
**components** | [**\OpenAPI\Client\Model\WhatsAppTemplateComponentsInner[]**](WhatsAppTemplateComponentsInner.md) | An array of objects representing the parts of the template itself. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
