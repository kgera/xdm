---
---

# Componentized Page Schema

```
https://ns.adobe.com/xdm/content/componentized-page
```

A componentized page is a part of a digital experience that is authored though modular components. 
Examples for componentized pages include web pages as managed by a web content management system or mobile app pages as managed by a mobile content management system.
Componentized pages are modular (consist of smaller content components), hyperlinked (link to other pages), and include digital assets (like images or videos).

| Abstract | Extensible | Custom Properties | Defined In |
|----------|------------|-------------------|------------|
| Can be instantiated | Yes | Forbidden | [content/componentized-page.schema.json](content/componentized-page.schema.json) |

## Schema Hierarchy

* Componentized Page `https://ns.adobe.com/xdm/content/componentized-page`
  * [Content](content.schema.md) `https://ns.adobe.com/xdm/content/content`

## Componentized Page Example
```json
{
  "xdm:name": "example",
  "xdm:path": "/content/example",
  "dc:title": "Example Page for XDM.",
  "xdm:shortTitle": "Example",
  "xdm:repositoryCreatedDate": "2017-09-26T13:27:36+00:00",
  "xdm:repositoryCreatedBy": "https://identity.adobe.io/users/tripod@adobe.com",
  "xdm:repositoryLastModifiedDate": "2017-09-26T13:31:19+00:00",
  "xdm:repositoryLastModifiedBy": "https://identity.adobe.io/users/trieloff@adobe.com",
  "xdm:language": "en-US",
  "xdm:template": "https://francois.corp.adobe.com:4502/apps/foundation/generic_page",
  "teaser": {
    "type": "https://francois.corp.adobe.com:4502/apps/foundation/teaser",
    "title": "Sunglasses",
    "image": {
      "@type": "http://ns.adobe.com/xdm/assets/asset",
      "xdm:assetID": "urn:aaid:aem:4123ba4c-93a8-4c5d-b979-ffbbe4318185",
      "@id": "https://francois.corp.adobe.com:4502/content/dam/Fx_DUKE-small.jpg"
    }
  },
  "par": {
    "@type": "https://francois.corp.adobe.com:4502/apps/foundation/generic_container",
    "xdm:items_order": [
      "title0",
      "text0",
      "image0"
    ],
    "xdm:items": {
      "title0": {
        "type": "https://francois.corp.adobe.com:4502/apps/foundation/title",
        "title": "Protect Your Eyes"
      },
      "image0": {
        "type": "https://francois.corp.adobe.com:4502/apps/foundation/image",
        "image": {
          "@type": "http://ns.adobe.com/xdm/assets/asset",
          "asset_id": "urn:aaid:aem:4123ba4c-93a8-4c5d-b979-1234e4318185",
          "id": "https://francois.corp.adobe.com:4502/content/dam/Glasses-small.jpg"
        }
      },
      "text0": {
        "type": "https://francois.corp.adobe.com:4502/apps/foundation/text",
        "text": "<p>Even during high UV levels...</p>"
      }
    }
  }
}
```

# Componentized Page Properties

| Property | Type | Required | Defined by |
|----------|------|----------|------------|
| [@id](#@id) | `string` | Optional | [Content](content.schema.md#@id) |
| [xdm:repositoryCreatedDate](#xdm:repositoryCreatedDate) | `string` | **Required** | [Content](content.schema.md#xdm:repositoryCreatedDate) |
| [xdm:repositoryCreatedBy](#xdm:repositoryCreatedBy) | `string` | **Required** | [Content](content.schema.md#xdm:repositoryCreatedBy) |
| [xdm:repositoryLastModifiedDate](#xdm:repositoryLastModifiedDate) | `string` | **Required** | [Content](content.schema.md#xdm:repositoryLastModifiedDate) |
| [xdm:repositoryLastModifiedBy](#xdm:repositoryLastModifiedBy) | `string` | **Required** | [Content](content.schema.md#xdm:repositoryLastModifiedBy) |
| [xdm:versionID](#xdm:versionID) | `string` | Optional | [Content](content.schema.md#xdm:versionID) |
| [xdm:path](#xdm:path) | `string` | **Required** | Componentized Page (this schema) |
| [xdm:name](#xdm:name) | `string` | **Required** | Componentized Page (this schema) |
| [dc:title](#dc:title) | `string` | Optional | Componentized Page (this schema) |
| [xdm:shortTitle](#xdm:shortTitle) | `string` | Optional | Componentized Page (this schema) |
| [xdm:unlisted](#xdm:unlisted) | `boolean` | Optional | Componentized Page (this schema) |
| [xdm:template](#xdm:template) | `string` | Optional | Componentized Page (this schema) |
| [xdm:language](#xdm:language) | `string` | Optional | Componentized Page (this schema) |

## @id

A unique identifier given to every addressable piece of content in a given repository.

`@id`
* is optional
* type: `string`
* defined in [Content](content.schema.md#@id)

### @id Type


`string`
* format: `uri` Uniformous Resource Identifier (according to [RFC3986](http://tools.ietf.org/html/rfc3986))






## xdm:repositoryCreatedDate

The server date and time when the resource was created in the repository, such as when an asset file is first uploaded or a directory is created by the server as the parent of a new asset. The Date Time property should conform to ISO 8601 standard. An example form is &#34;2004-10-23T12:00:00-06:00&#34;.

`xdm:repositoryCreatedDate`
* is **required**
* type: `string`
* defined in [Content](content.schema.md#xdm:repositoryCreatedDate)

### xdm:repositoryCreatedDate Type


`string`
* format: `date-time` date and time (according to [RFC 3339, section 5.6](http://tools.ietf.org/html/rfc3339))






## xdm:repositoryCreatedBy

ID of the user who initiated the action that caused the resource to be created in the repository.

`xdm:repositoryCreatedBy`
* is **required**
* type: `string`
* defined in [Content](content.schema.md#xdm:repositoryCreatedBy)

### xdm:repositoryCreatedBy Type


`string`






## xdm:repositoryLastModifiedDate

The server date and time when the resource was most recently modified in the repository, such as when a new version of an asset is uploaded or a directory&#39;s child resource is added or removed. The Date Time property should conform to ISO 8601 standard. An example form is &#34;2004-10-23T12:00:00-06:00&#34;.

`xdm:repositoryLastModifiedDate`
* is **required**
* type: `string`
* defined in [Content](content.schema.md#xdm:repositoryLastModifiedDate)

### xdm:repositoryLastModifiedDate Type


`string`
* format: `date-time` date and time (according to [RFC 3339, section 5.6](http://tools.ietf.org/html/rfc3339))






## xdm:repositoryLastModifiedBy

ID of the user who initiated the action that most recently caused the resource to be modified in the repository.

`xdm:repositoryLastModifiedBy`
* is **required**
* type: `string`
* defined in [Content](content.schema.md#xdm:repositoryLastModifiedBy)

### xdm:repositoryLastModifiedBy Type


`string`






## xdm:versionID

The version ID of the piece of content. It will be generated both on explicit and implicit save or upload.

`xdm:versionID`
* is optional
* type: `string`
* defined in [Content](content.schema.md#xdm:versionID)

### xdm:versionID Type


`string`






## xdm:path

Shows the hierarchy of the page. The path semantics should be same as that defined in [RFC 3986](https://tools.ietf.org/html/rfc3986#section-3.3). In case a repository is not path based then it can return the information which will help in browsing. It could be just an document id, or something like `{catalog}/{id}` in case of a document database.

`xdm:path`
* is **required**
* type: `string`
* defined in this schema

### xdm:path Type


`string`






## xdm:name

Name of the page in the repository. This could be a file name or any name provided by the repository to the page.

`xdm:name`
* is **required**
* type: `string`
* defined in this schema

### xdm:name Type


`string`






## dc:title

Full title of the page.

`dc:title`
* is optional
* type: `string`
* defined in this schema

### dc:title Type


`string`






## xdm:shortTitle

Short title of the page that is suitable to be displayed in navigation links.

`xdm:shortTitle`
* is optional
* type: `string`
* defined in this schema

### xdm:shortTitle Type


`string`






## xdm:unlisted

Indicates if this page should be hidden by default in navigational collections.

`xdm:unlisted`
* is optional
* type: `boolean`
* defined in this schema

### xdm:unlisted Type


`boolean`





## xdm:template

The template that was used to create this page.

`xdm:template`
* is optional
* type: `string`
* defined in this schema

### xdm:template Type


`string`
* format: `uri-reference` URI Reference (according to [RFC3986](https://tools.ietf.org/html/rfc3986))






## xdm:language

Specifies the language of this page. the language property should conform to BPC 47, for example `en-GB`

`xdm:language`
* is optional
* type: `string`
* defined in this schema

### xdm:language Type


`string`


All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E((((%5BA-Za-z%5D%7B2%2C3%7D(-(%5BA-Za-z%5D%7B3%7D(-%5BA-Za-z%5D%7B3%7D)%7B0%2C2%7D))%3F)%7C%5BA-Za-z%5D%7B4%7D%7C%5BA-Za-z%5D%7B5%2C8%7D)(-(%5BA-Za-z%5D%7B4%7D))%3F(-(%5BA-Za-z%5D%7B2%7D%7C%5B0-9%5D%7B3%7D))%3F(-(%5BA-Za-z0-9%5D%7B5%2C8%7D%7C%5B0-9%5D%5BA-Za-z0-9%5D%7B3%7D))*(-(%5B0-9A-WY-Za-wy-z%5D(-%5BA-Za-z0-9%5D%7B2%2C8%7D)%2B))*(-(x(-%5BA-Za-z0-9%5D%7B1%2C8%7D)%2B))%3F)%7C(x(-%5BA-Za-z0-9%5D%7B1%2C8%7D)%2B)%7C((en-GB-oed%7Ci-ami%7Ci-bnn%7Ci-default%7Ci-enochian%7Ci-hak%7Ci-klingon%7Ci-lux%7Ci-mingo%7Ci-navajo%7Ci-pwn%7Ci-tao%7Ci-tay%7Ci-tsu%7Csgn-BE-FR%7Csgn-BE-NL%7Csgn-CH-DE)%7C(art-lojban%7Ccel-gaulish%7Cno-bok%7Cno-nyn%7Czh-guoyu%7Czh-hakka%7Czh-min%7Czh-min-nan%7Czh-xiang)))%24)):
```regex
^(((([A-Za-z]{2,3}(-([A-Za-z]{3}(-[A-Za-z]{3}){0,2}))?)|[A-Za-z]{4}|[A-Za-z]{5,8})(-([A-Za-z]{4}))?(-([A-Za-z]{2}|[0-9]{3}))?(-([A-Za-z0-9]{5,8}|[0-9][A-Za-z0-9]{3}))*(-([0-9A-WY-Za-wy-z](-[A-Za-z0-9]{2,8})+))*(-(x(-[A-Za-z0-9]{1,8})+))?)|(x(-[A-Za-z0-9]{1,8})+)|((en-GB-oed|i-ami|i-bnn|i-default|i-enochian|i-hak|i-klingon|i-lux|i-mingo|i-navajo|i-pwn|i-tao|i-tay|i-tsu|sgn-BE-FR|sgn-BE-NL|sgn-CH-DE)|(art-lojban|cel-gaulish|no-bok|no-nyn|zh-guoyu|zh-hakka|zh-min|zh-min-nan|zh-xiang)))$
```




