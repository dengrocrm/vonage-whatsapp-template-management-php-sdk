# # CreateTemplateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The name of the template |
**language** | **string** | The language of the template. The same template name can be used for multiple language versions. A list of supported languages is available in the [WhatsApp documentation](https://developers.facebook.com/docs/whatsapp/api/messages/message-templates/). Note: Adding new languages on *legacy* template categories has been disabled by Meta, see the documentation for [Language Variants](/messages/whatsapp-template-management/overview#language-variants) and [Categories](/messages/whatsapp-template-management/overview#template-categories) |
**category** | **string** | The required category of the template. The category determines what the template will be used for. Note: Adding new languages on *legacy* template categories has been disabled by Meta, see the documentation for [Language Variants](/messages/whatsapp-template-management/overview#language-variants) and [Categories](/messages/whatsapp-template-management/overview#template-categories) |
**allow_category_change** | **bool** | An optional parameter which, when set to &#x60;true&#x60;, can avoid template rejection due to mis-categorization. Including this parameter, with a value of &#x60;true&#x60;, will allow Meta to re-assign the template to a different category as appropriate. | [optional]
**components** | [**\OpenAPI\Client\Model\CreateMediaTemplateComponentsInner[]**](CreateMediaTemplateComponentsInner.md) | An array of objects representing the parts of the template itself. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
