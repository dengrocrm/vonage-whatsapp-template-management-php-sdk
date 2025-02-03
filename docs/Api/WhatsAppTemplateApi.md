# DengroCrm\VonageWhatsAppTemplateManagement\WhatsAppTemplateApi

All URIs are relative to https://api.nexmo.com/v2/whatsapp-manager, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTemplate()**](WhatsAppTemplateApi.md#createTemplate) | **POST** /wabas/{id}/templates | Create Template |
| [**deleteTemplate()**](WhatsAppTemplateApi.md#deleteTemplate) | **DELETE** /wabas/{id}/templates | Delete Template |
| [**getTemplate()**](WhatsAppTemplateApi.md#getTemplate) | **GET** /wabas/{id}/templates/{template_id} | Get Template |
| [**listTemplates()**](WhatsAppTemplateApi.md#listTemplates) | **GET** /wabas/{id}/templates | List Templates |
| [**mediaUpload()**](WhatsAppTemplateApi.md#mediaUpload) | **POST** /media/uploads | Media Upload |
| [**updateTemplate()**](WhatsAppTemplateApi.md#updateTemplate) | **PUT** /wabas/{id}/templates/{template_id} | Update Template |


## `createTemplate()`

```php
createTemplate($id, $content_type, $create_template_request): \DengroCrm\VonageWhatsAppTemplateManagement\Model\CreateTemplate200Response
```

Create Template

Submit a new template to be associated with this WABA

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = DengroCrm\VonageWhatsAppTemplateManagement\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new DengroCrm\VonageWhatsAppTemplateManagement\Api\WhatsAppTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The id of the WABA
$content_type = 'content_type_example'; // string | application/json
$create_template_request = new \DengroCrm\VonageWhatsAppTemplateManagement\Model\CreateTemplateRequest(); // \DengroCrm\VonageWhatsAppTemplateManagement\Model\CreateTemplateRequest

try {
    $result = $apiInstance->createTemplate($id, $content_type, $create_template_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WhatsAppTemplateApi->createTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The id of the WABA | |
| **content_type** | **string**| application/json | [optional] |
| **create_template_request** | [**\DengroCrm\VonageWhatsAppTemplateManagement\Model\CreateTemplateRequest**](../Model/CreateTemplateRequest.md)|  | [optional] |

### Return type

[**\DengroCrm\VonageWhatsAppTemplateManagement\Model\CreateTemplate200Response**](../Model/CreateTemplate200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteTemplate()`

```php
deleteTemplate($id, $name, $hsm_id)
```

Delete Template

Delete a template of the specified name associated with the WABA ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = DengroCrm\VonageWhatsAppTemplateManagement\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new DengroCrm\VonageWhatsAppTemplateManagement\Api\WhatsAppTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The id of the WABA
$name = 13; // string | The name of the template to be deleted. This parameter is required unless `hsm_id` is specified.
$hsm_id = 13; // string | The ID of the template to be deleted. This parameter is required unless `name` is specified.

try {
    $apiInstance->deleteTemplate($id, $name, $hsm_id);
} catch (Exception $e) {
    echo 'Exception when calling WhatsAppTemplateApi->deleteTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The id of the WABA | |
| **name** | **string**| The name of the template to be deleted. This parameter is required unless &#x60;hsm_id&#x60; is specified. | |
| **hsm_id** | **string**| The ID of the template to be deleted. This parameter is required unless &#x60;name&#x60; is specified. | |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTemplate()`

```php
getTemplate($id, $template_id): \DengroCrm\VonageWhatsAppTemplateManagement\Model\WhatsAppTemplate
```

Get Template

Get details of an existing template identified by the WABA and Template ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = DengroCrm\VonageWhatsAppTemplateManagement\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new DengroCrm\VonageWhatsAppTemplateManagement\Api\WhatsAppTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The id of the WABA
$template_id = 'template_id_example'; // string | The id of the template

try {
    $result = $apiInstance->getTemplate($id, $template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WhatsAppTemplateApi->getTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The id of the WABA | |
| **template_id** | **string**| The id of the template | |

### Return type

[**\DengroCrm\VonageWhatsAppTemplateManagement\Model\WhatsAppTemplate**](../Model/WhatsAppTemplate.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listTemplates()`

```php
listTemplates($id, $limit, $before, $after, $category, $content, $language, $name, $name_or_content, $quality_score, $status): \DengroCrm\VonageWhatsAppTemplateManagement\Model\ListTemplates200Response
```

List Templates

Get a list of templates,and their associated metadata, for the specified WABA ID. If multiple language variants exist for a template, each variant will be returned as a separate template object.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = DengroCrm\VonageWhatsAppTemplateManagement\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new DengroCrm\VonageWhatsAppTemplateManagement\Api\WhatsAppTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The id of the WABA
$limit = 10; // float | The number of templates to return in the list. Although the max size is 500, for large datasets it is recommended to use a lower limit and instead use pagination to avoid potential timeouts.
$before = MAZDZD; // string | A cursor point used for a paginated request to indicate the template to paginate backwards from.
$after = MjQZD; // string | A cursor point used for a paginated request to indicate the template to paginate forwards from.
$category = UTILITY; // string | A filter  for returning only templates matching a specific category.
$content = special offer; // string | A search filter representing the content of a template. Only matching templates will be returned in the list.
$language = en; // string | A filter  for returning only templates matching a specific language code. A list of supported languages is available in the [WhatsApp documentation](https://developers.facebook.com/docs/whatsapp/api/messages/message-templates/)
$name = My Template; // string | A search filter representing the name, either full or partial, of a template. Only matching templates will be returned in the list.
$name_or_content = special offer; // string | A search filter representing the name, either full or partial, or content of a template. Only matching templates will be returned in the list.
$quality_score = RED; // string | A search filter representing the quality score of a template. Only matching templates will be returned in the list.
$status = APPROVED; // string | A filter for returning only templates matching a specific status.

try {
    $result = $apiInstance->listTemplates($id, $limit, $before, $after, $category, $content, $language, $name, $name_or_content, $quality_score, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WhatsAppTemplateApi->listTemplates: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The id of the WABA | |
| **limit** | **float**| The number of templates to return in the list. Although the max size is 500, for large datasets it is recommended to use a lower limit and instead use pagination to avoid potential timeouts. | [optional] [default to 25] |
| **before** | **string**| A cursor point used for a paginated request to indicate the template to paginate backwards from. | [optional] |
| **after** | **string**| A cursor point used for a paginated request to indicate the template to paginate forwards from. | [optional] |
| **category** | **string**| A filter  for returning only templates matching a specific category. | [optional] |
| **content** | **string**| A search filter representing the content of a template. Only matching templates will be returned in the list. | [optional] |
| **language** | **string**| A filter  for returning only templates matching a specific language code. A list of supported languages is available in the [WhatsApp documentation](https://developers.facebook.com/docs/whatsapp/api/messages/message-templates/) | [optional] |
| **name** | **string**| A search filter representing the name, either full or partial, of a template. Only matching templates will be returned in the list. | [optional] |
| **name_or_content** | **string**| A search filter representing the name, either full or partial, or content of a template. Only matching templates will be returned in the list. | [optional] |
| **quality_score** | **string**| A search filter representing the quality score of a template. Only matching templates will be returned in the list. | [optional] |
| **status** | **string**| A filter for returning only templates matching a specific status. | [optional] |

### Return type

[**\DengroCrm\VonageWhatsAppTemplateManagement\Model\ListTemplates200Response**](../Model/ListTemplates200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `mediaUpload()`

```php
mediaUpload($file_type, $content_type, $mediafile): \DengroCrm\VonageWhatsAppTemplateManagement\Model\MediaUpload200Response
```

Media Upload

Upload media files to the WhatsApp platform. Once uploaded, you can use an uploaded file's handle to create a media template.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = DengroCrm\VonageWhatsAppTemplateManagement\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new DengroCrm\VonageWhatsAppTemplateManagement\Api\WhatsAppTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$file_type = 'file_type_example'; // string | The file's MIME type. Valid values are: `image/jpeg`, `image/jpg`, `image/png`, and `video/mp4`.
$content_type = 'content_type_example'; // string | multipart/form-data
$mediafile = '/path/to/file.txt'; // \SplFileObject | The file to be uploaded. [See an example cURL request](/messages/guides/whatsapp-template-management#uploading-media)

try {
    $result = $apiInstance->mediaUpload($file_type, $content_type, $mediafile);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WhatsAppTemplateApi->mediaUpload: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **file_type** | **string**| The file&#39;s MIME type. Valid values are: &#x60;image/jpeg&#x60;, &#x60;image/jpg&#x60;, &#x60;image/png&#x60;, and &#x60;video/mp4&#x60;. | |
| **content_type** | **string**| multipart/form-data | |
| **mediafile** | **\SplFileObject****\SplFileObject**| The file to be uploaded. [See an example cURL request](/messages/guides/whatsapp-template-management#uploading-media) | [optional] |

### Return type

[**\DengroCrm\VonageWhatsAppTemplateManagement\Model\MediaUpload200Response**](../Model/MediaUpload200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTemplate()`

```php
updateTemplate($id, $template_id, $content_type, $update_template_request)
```

Update Template

Update an existing template identified by the WABA and Template ID

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = DengroCrm\VonageWhatsAppTemplateManagement\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new DengroCrm\VonageWhatsAppTemplateManagement\Api\WhatsAppTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The id of the WABA
$template_id = 'template_id_example'; // string | The id of the template to be updated
$content_type = 'content_type_example'; // string | application/json
$update_template_request = new \DengroCrm\VonageWhatsAppTemplateManagement\Model\UpdateTemplateRequest(); // \DengroCrm\VonageWhatsAppTemplateManagement\Model\UpdateTemplateRequest

try {
    $apiInstance->updateTemplate($id, $template_id, $content_type, $update_template_request);
} catch (Exception $e) {
    echo 'Exception when calling WhatsAppTemplateApi->updateTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| The id of the WABA | |
| **template_id** | **string**| The id of the template to be updated | |
| **content_type** | **string**| application/json | [optional] |
| **update_template_request** | [**\DengroCrm\VonageWhatsAppTemplateManagement\Model\UpdateTemplateRequest**](../Model/UpdateTemplateRequest.md)|  | [optional] |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
