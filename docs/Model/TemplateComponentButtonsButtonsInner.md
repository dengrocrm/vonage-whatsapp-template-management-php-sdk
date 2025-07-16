# # TemplateComponentButtonsButtonsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | The type of button | [optional]
**text** | **string** | The text displayed on the button. | [optional]
**url** | **string** | URL to which the end-user will be directed when hitting the button. | [optional]
**phone_number** | **string** | Phone number to which a phone call would be placed by the end-user when hitting the button. | [optional]
**flow_id** | **string** | The unique ID of the Flow. Cannot be used if flow_name or flow_json parameters are provided. Only one of these parameters is required. | [optional]
**flow_name** | **string** | The name of the Flow. Supported in Cloud API only. The Flow ID is stored in the message template, not the name, so changing the Flow name will not affect existing message templates. Cannot be used if flow_id or flow_json parameters are provided. Only one of these parameters is required. | [optional]
**flow_json** | **string** | The Flow JSON encoded as string with escaping. The Flow JSON specifies the content of the Flow. Supported in Cloud API only. Cannot be used if flow_id or flow_name parameters are provided. Only one of these parameters is required. | [optional]
**flow_action** | **string** | Either navigate or data_exchange. (Default value: navigate) | [optional]
**navigate_screen** | **string** | Optional if flow_action is navigate. The unique ID of the Screen in the Flow. Only used if flow_action is set to navigate. (Default value: \&quot;FIRST_ENTRY_SCREEN\&quot;) | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
