# OpenAPIClient-php

The Messages API now offers the WhatsApp Template Management API that allow you to manage templates for your WABAs and cut out the manual step of submitting and checking templates manually. You can manage your templates using the Template Management API, including adding new templates, retrieving their statuses, and deleting any that are already in use. Different sorts of media can be sent with each WhatsApp message template. You can manage your media files via the API and set up extra features to improve their functionality.

For more information, please visit [https://developer.vonage.com/](https://developer.vonage.com/).

## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/dengrocrm/vonage-whatsapp-template-management-php-sdk.git"
    }
  ],
  "require": {
    "dengrocrm/vonage-whatsapp-template-management-php-sdk": "1.4.0"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure Bearer (JWT) authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string | The id of the WABA
$content_type = 'content_type_example'; // string | application/json
$create_template_request = new \OpenAPI\Client\Model\CreateTemplateRequest(); // \OpenAPI\Client\Model\CreateTemplateRequest

try {
    $result = $apiInstance->createTemplate($id, $content_type, $create_template_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->createTemplate: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api.nexmo.com/v2/whatsapp-manager*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DefaultApi* | [**createTemplate**](docs/Api/DefaultApi.md#createtemplate) | **POST** /wabas/{id}/templates | Create Template
*DefaultApi* | [**deleteTemplate**](docs/Api/DefaultApi.md#deletetemplate) | **DELETE** /wabas/{id}/templates | Delete Template
*DefaultApi* | [**getTemplate**](docs/Api/DefaultApi.md#gettemplate) | **GET** /wabas/{id}/templates/{template_id} | Get Template
*DefaultApi* | [**listTemplates**](docs/Api/DefaultApi.md#listtemplates) | **GET** /wabas/{id}/templates | List Templates
*DefaultApi* | [**mediaUpload**](docs/Api/DefaultApi.md#mediaupload) | **POST** /media/uploads | Media Upload
*DefaultApi* | [**updateTemplate**](docs/Api/DefaultApi.md#updatetemplate) | **PUT** /wabas/{id}/templates/{template_id} | Update Template

## Models

- [CreateMediaTemplate](docs/Model/CreateMediaTemplate.md)
- [CreateMediaTemplateComponentsInner](docs/Model/CreateMediaTemplateComponentsInner.md)
- [CreateMediaTemplateComponentsInnerButtonsInner](docs/Model/CreateMediaTemplateComponentsInnerButtonsInner.md)
- [CreateMediaTemplateComponentsInnerExample](docs/Model/CreateMediaTemplateComponentsInnerExample.md)
- [CreateTemplate200Response](docs/Model/CreateTemplate200Response.md)
- [CreateTemplateRequest](docs/Model/CreateTemplateRequest.md)
- [CreateTextTemplate](docs/Model/CreateTextTemplate.md)
- [CreateTextTemplateComponentsInner](docs/Model/CreateTextTemplateComponentsInner.md)
- [CreateTextTemplateComponentsInnerButtonsInner](docs/Model/CreateTextTemplateComponentsInnerButtonsInner.md)
- [CreateTextTemplateComponentsInnerExample](docs/Model/CreateTextTemplateComponentsInnerExample.md)
- [ErrorResponse400](docs/Model/ErrorResponse400.md)
- [ErrorResponse401](docs/Model/ErrorResponse401.md)
- [ErrorResponse404](docs/Model/ErrorResponse404.md)
- [ErrorResponse422](docs/Model/ErrorResponse422.md)
- [ErrorResponse429](docs/Model/ErrorResponse429.md)
- [ErrorResponse500](docs/Model/ErrorResponse500.md)
- [GetTemplate404Response](docs/Model/GetTemplate404Response.md)
- [ListTemplates200Response](docs/Model/ListTemplates200Response.md)
- [ListTemplates200ResponsePaging](docs/Model/ListTemplates200ResponsePaging.md)
- [ListTemplates200ResponsePagingCursors](docs/Model/ListTemplates200ResponsePagingCursors.md)
- [MediaUpload200Response](docs/Model/MediaUpload200Response.md)
- [TemplateComponentButtons](docs/Model/TemplateComponentButtons.md)
- [TemplateComponentButtonsButtonsInner](docs/Model/TemplateComponentButtonsButtonsInner.md)
- [TemplateComponentStandard](docs/Model/TemplateComponentStandard.md)
- [TemplateNotFound](docs/Model/TemplateNotFound.md)
- [UpdateMediaTemplate](docs/Model/UpdateMediaTemplate.md)
- [UpdateTemplateRequest](docs/Model/UpdateTemplateRequest.md)
- [UpdateTextTemplate](docs/Model/UpdateTextTemplate.md)
- [WabaNotFound](docs/Model/WabaNotFound.md)
- [WhatsAppTemplate](docs/Model/WhatsAppTemplate.md)
- [WhatsAppTemplateComponentsInner](docs/Model/WhatsAppTemplateComponentsInner.md)

## Authorization

Authentication schemes defined for the API:
### bearerAuth

- **Type**: Bearer authentication (JWT)

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.4.0`
    - Generator version: `7.12.0-SNAPSHOT`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
