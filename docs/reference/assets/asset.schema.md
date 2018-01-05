---
---

# Asset Schema

```
https://ns.adobe.com/xdm/assets/asset
```

A digital asset, is anything that exists in a binary format and comes with the right to use. Content that does not possess that right is not considered an asset. Digital assets include but are not exclusive to: digital documents, audible content, motion picture, and other relevant digital content that is currently in circulation or production.
As described in [What is a digital asset](https://www.realstorygroup.com/Blog/3140-What-is-a-digital-asset), the definition of a digital asset can be put like this:
&gt; In theory, a digital asset is something represented in a digital form that has an intrinsic or acquired value. This initial definition is intentionally general. It could correspond to almost anything or any piece of media in a digital form, such as a photo, website, or email message. As a practical matter, however, DAM [Digital Asset Management] has evolved to support the management of digital media assets almost exclusively. This includes images, video, audio, and related artifacts (such as brochures and compound publications). You would typically use different types of technology to manage email, Word documents, relational data records, and web pages. Even some image “assets” don’t fall under the domain of DAM technology as it is known today. Scanned paper or forms that end up as TIFF or PDF files do not constitute media assets that originate through some creative process.
All digital assets are content, and some content can include, link to, or refer digital assets. Content can furthermore be transformed (rendered) into digital assets, such as when exporting a PDF. 

| Abstract | Extensible | Custom Properties | Defined In |
|----------|------------|-------------------|------------|
| Can be instantiated | Yes | Forbidden | [assets/asset.schema.json](assets/asset.schema.json) |

## Schema Hierarchy

* Asset `https://ns.adobe.com/xdm/assets/asset`
  * [Content](../content/content.schema.md) `https://ns.adobe.com/xdm/content/content`
  * [Copyright Owner](copyright-owner.schema.md) `https://ns.adobe.com/xdm/assets/copyright-owner`
  * [Layer Group](layer-group.schema.md) `https://ns.adobe.com/xdm/assets/layer-group`

## Asset Example
```json
{
  "xdm:assetID": "urn:aaid:a:b:01234578-0123-ABCD-abcd-0123456789ab",
  "xmp:createDate": "2017-09-26T15:52:25+00:00",
  "xdm:repositoryCreatedDate": "2017-09-26T15:52:25+00:00",
  "xdm:repositoryCreatedBy": "lars",
  "xmp:modifyDate": "2017-09-26T15:52:25+00:00",
  "xdm:repositoryLastModifiedDate": "2017-09-26T15:52:25+00:00",
  "xdm:repositoryLastModifiedBy": "lars",
  "xdm:versionID": "15",
  "xdm:size": 1632418,
  "xdm:path": "here",
  "xdm:etag": "15"
}
```

# Asset Properties

| Property | Type | Required | Defined by |
|----------|------|----------|------------|
| [@id](#@id) | `string` | Optional | [Content](../content/content.schema.md#@id) |
| [xdm:repositoryCreatedDate](#xdm:repositoryCreatedDate) | `string` | **Required** | [Content](../content/content.schema.md#xdm:repositoryCreatedDate) |
| [xdm:repositoryCreatedBy](#xdm:repositoryCreatedBy) | `string` | **Required** | [Content](../content/content.schema.md#xdm:repositoryCreatedBy) |
| [xdm:repositoryLastModifiedDate](#xdm:repositoryLastModifiedDate) | `string` | **Required** | [Content](../content/content.schema.md#xdm:repositoryLastModifiedDate) |
| [xdm:repositoryLastModifiedBy](#xdm:repositoryLastModifiedBy) | `string` | **Required** | [Content](../content/content.schema.md#xdm:repositoryLastModifiedBy) |
| [xdm:versionID](#xdm:versionID) | `string` | **Required** | [Content](../content/content.schema.md#xdm:versionID) |
| [plus:copyrightOwnerID](#plus:copyrightOwnerID) | `string` | Optional | [Copyright Owner](copyright-owner.schema.md#plus:copyrightOwnerID) |
| [plus:copyrightOwnerName](#plus:copyrightOwnerName) | `string` | Optional | [Copyright Owner](copyright-owner.schema.md#plus:copyrightOwnerName) |
| [xdm:assetID](#xdm:assetID) | `string` | **Required** | Asset (this schema) |
| [xdm:documentID](#xdm:documentID) | `string` | Optional | Asset (this schema) |
| [xdm:name](#xdm:name) | `string` | Optional | Asset (this schema) |
| [xdm:aliasIDs](#xdm:aliasIDs) | `array` | Optional | Asset (this schema) |
| [xmp:createDate](#xmp:createDate) | `string` | **Required** | Asset (this schema) |
| [dc:creator](#dc:creator) | `string[]` | Optional | Asset (this schema) |
| [xmp:creatorTool](#xmp:creatorTool) | `string` | Optional | Asset (this schema) |
| [xmp:modifyDate](#xmp:modifyDate) | `string` | **Required** | Asset (this schema) |
| [xdm:milestone](#xdm:milestone) | `object` | Optional | Asset (this schema) |
| [xmpRights:webStatement](#xmpRights:webStatement) | `string` | Optional | Asset (this schema) |
| [dc:rights](#dc:rights) | reference | Optional | Asset (this schema) |
| [xmpRights:marked](#xmpRights:marked) | `boolean` | Optional | Asset (this schema) |
| [xmpRights:usageTerms](#xmpRights:usageTerms) | reference | Optional | Asset (this schema) |
| [plus:copyrightOwner](#plus:copyrightOwner) | reference | Optional | Asset (this schema) |
| [photoshop:credit](#photoshop:credit) | `string` | Optional | Asset (this schema) |
| [cc:license](#cc:license) | `string` | Optional | Asset (this schema) |
| [cc:attributionUrl](#cc:attributionUrl) | `string` | Optional | Asset (this schema) |
| [cc:attributionName](#cc:attributionName) | `string` | Optional | Asset (this schema) |
| [xmpMM:manageUI](#xmpMM:manageUI) | `string` | Optional | Asset (this schema) |
| [xmpMM:manageTo](#xmpMM:manageTo) | `string` | Optional | Asset (this schema) |
| [xmpMM:history](#xmpMM:history) | reference | Optional | Asset (this schema) |
| [dc:title](#dc:title) | reference | Optional | Asset (this schema) |
| [dc:description](#dc:description) | reference | Optional | Asset (this schema) |
| [dc:format](#dc:format) |`string` | Optional | Asset (this schema) |
| [xdm:notSafe](#xdm:notSafe) | `enum` | Optional | Asset (this schema) |
| [dc:language](#dc:language) | `string[]` | Optional | Asset (this schema) |
| [xdm:size](#xdm:size) | `integer` | **Required** | Asset (this schema) |
| [xdm:path](#xdm:path) | `string` | **Required** | Asset (this schema) |
| [xdm:etag](#xdm:etag) | `string` | **Required** | Asset (this schema) |
| [xmpTPg:NPages](#xmpTPg:NPages) | `integer` | Optional | Asset (this schema) |
| [exif:gpsAltitude](#exif:gpsAltitude) | `number` | Optional | Asset (this schema) |
| [exif:gpsAltitudeRef](#exif:gpsAltitudeRef) | `enum` | Optional | Asset (this schema) |
| [exif:gpsLatitude](#exif:gpsLatitude) | `string` | Optional | Asset (this schema) |
| [exif:gpsLongitude](#exif:gpsLongitude) | `string` | Optional | Asset (this schema) |
| [xmp:rating](#xmp:rating) | `enum` | Optional | Asset (this schema) |
| [dc:subject](#dc:subject) | `string[]` | Optional | Asset (this schema) |
| [xmp:keywords](#xmp:keywords) | `array` | Optional | Asset (this schema) |
| [xmp:machineKeywords](#xmp:machineKeywords) | `array` | Optional | Asset (this schema) |
| [xmp:fonts](#xmp:fonts) | reference | Optional | Asset (this schema) |
| [xmp:layers](#xmp:layers) | complex | Optional | Asset (this schema) |
| [xmp:artboards](#xmp:artboards) | Artboard | Optional | Asset (this schema) |

## @id

A unique identifier given to every addressable piece of content in a given repository.

`@id`
* is optional
* type: `string`
* defined in [Content](../content/content.schema.md#@id)

### @id Type


`string`
* format: `uri` Uniformous Resource Identifier (according to [RFC3986](http://tools.ietf.org/html/rfc3986))






## xdm:repositoryCreatedDate

The server date and time when the resource was created in the repository, such as when an asset file is first uploaded or a directory is created by the server as the parent of a new asset. The Date Time property should conform to ISO 8601 standard. An example form is &#34;2004-10-23T12:00:00-06:00&#34;.

`xdm:repositoryCreatedDate`
* is **required**
* type: `string`
* defined in [Content](../content/content.schema.md#xdm:repositoryCreatedDate)

### xdm:repositoryCreatedDate Type


`string`
* format: `date-time` date and time (according to [RFC 3339, section 5.6](http://tools.ietf.org/html/rfc3339))






## xdm:repositoryCreatedBy

ID of the user who initiated the action that caused the resource to be created in the repository.

`xdm:repositoryCreatedBy`
* is **required**
* type: `string`
* defined in [Content](../content/content.schema.md#xdm:repositoryCreatedBy)

### xdm:repositoryCreatedBy Type


`string`






## xdm:repositoryLastModifiedDate

The server date and time when the resource was most recently modified in the repository, such as when a new version of an asset is uploaded or a directory&#39;s child resource is added or removed. The Date Time property should conform to ISO 8601 standard. An example form is &#34;2004-10-23T12:00:00-06:00&#34;.

`xdm:repositoryLastModifiedDate`
* is **required**
* type: `string`
* defined in [Content](../content/content.schema.md#xdm:repositoryLastModifiedDate)

### xdm:repositoryLastModifiedDate Type


`string`
* format: `date-time` date and time (according to [RFC 3339, section 5.6](http://tools.ietf.org/html/rfc3339))






## xdm:repositoryLastModifiedBy

ID of the user who initiated the action that most recently caused the resource to be modified in the repository.

`xdm:repositoryLastModifiedBy`
* is **required**
* type: `string`
* defined in [Content](../content/content.schema.md#xdm:repositoryLastModifiedBy)

### xdm:repositoryLastModifiedBy Type


`string`






## xdm:versionID

The version ID of the piece of content. It will be generated both on explicit and implicit save or upload.

`xdm:versionID`
* is **required**
* type: `string`
* defined in [Content](../content/content.schema.md#xdm:versionID)

### xdm:versionID Type


`string`






## plus:copyrightOwnerID
### Copyright Owner ID

ID of the copyright owner.
If the PLUS-ID being stored in this property is registered with the PLUS Coalition, it should be expressed as a URL. For example: http://plus-id.org/PLUS-ID

`plus:copyrightOwnerID`
* is optional
* type: `string`
* defined in [Copyright Owner](copyright-owner.schema.md#plus:copyrightOwnerID)

### plus:copyrightOwnerID Type


`string`






## plus:copyrightOwnerName
### Copyright Owner Name

Name of Copyright Owner.

`plus:copyrightOwnerName`
* is optional
* type: `string`
* defined in [Copyright Owner](copyright-owner.schema.md#plus:copyrightOwnerName)

### plus:copyrightOwnerName Type


`string`






## xdm:assetID

A unique identifier given to every addressable asset in a given repository.
The format is a [GUID-based URN](https://www.ietf.org/rfc/rfc4122.txt). The pattern to generate an Asset ID is ```urn:aaid:{system}:{id} - {format}:{namespace}:{system}:{id}```

`xdm:assetID`
* is **required**
* type: `string`
* defined in this schema

### xdm:assetID Type


`string`


All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5Eurn%3Aaaid%3A%5BA-Za-z0-9%5D%2B%3A%5BA-Za-z0-9%5D%2B%3A%5BA-Fa-f0-9%5D%7B8%7D-%5BA-Fa-f0-9%5D%7B4%7D-%5BA-Fa-f0-9%5D%7B4%7D-%5BA-Fa-f0-9%5D%7B4%7D-%5BA-Fa-f0-9%5D%7B12%7D%24)):
```regex
^urn:aaid:[A-Za-z0-9]+:[A-Za-z0-9]+:[A-Fa-f0-9]{8}-[A-Fa-f0-9]{4}-[A-Fa-f0-9]{4}-[A-Fa-f0-9]{4}-[A-Fa-f0-9]{12}$
```






## xdm:documentID
### Document ID

It takes the value of xmpMM:DocumentID present in the [XMP packet of the asset](http://wwwimages.adobe.com/content/dam/Adobe/en/devnet/xmp/pdfs/XMP%20SDK%20Release%20cc-2014-12/XMPSpecificationPart1.pdf). For the assets having no XMP packet this property won&#39;t be populated. 
The value is a GUID, capital A-F, 8-4-4-12, preceded by the string `uuid:`

`xdm:documentID`
* is optional
* type: `string`
* defined in this schema

### xdm:documentID Type


`string`


All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5Euuid%3A%5BA-Fa-f0-9%5D%7B8%7D-%5BA-Fa-f0-9%5D%7B4%7D-%5BA-Fa-f0-9%5D%7B4%7D-%5BA-Fa-f0-9%5D%7B4%7D-%5BA-Fa-f0-9%5D%7B12%7D%24)):
```regex
^uuid:[A-Fa-f0-9]{8}-[A-Fa-f0-9]{4}-[A-Fa-f0-9]{4}-[A-Fa-f0-9]{4}-[A-Fa-f0-9]{12}$
```






## xdm:name
### Asset Name

Name of the asset in the repository. This could be a file name or any name provided by the repository to the asset.

`xdm:name`
* is optional
* type: `string`
* defined in this schema

### xdm:name Type


`string`






## xdm:aliasIDs
### Alias IDs

List of IDs under which external systems track the asset. Example of external systems : google, facebook etc.

`xdm:aliasIDs`
* is optional
* type: `array`

* defined in this schema

### xdm:aliasIDs Type


Array type: `array`

All items must be of the type:
Unknown type `array`.

```json
{
  "type": "array",
  "meta:usereditable": false,
  "title": "Alias IDs",
  "items": {
    "properties": {
      "system": {
        "title": "External System",
        "type": "string",
        "description": "A string used to identify the external systems like google, facebook etc."
      },
      "id": {
        "type": "string",
        "title": "External ID",
        "description": "An Id under which external systems track the asset."
      }
    },
    "simpletype": "complex"
  },
  "description": "List of IDs under which external systems track the asset. Example of external systems : google, facebook etc.",
  "simpletype": "`array`"
}
```








## xmp:createDate
### Date Created

The date and time the resource was created. It will be taken from within the asset.

`xmp:createDate`
* is **required**
* type: `string`
* defined in this schema

### xmp:createDate Type


`string`
* format: `date-time` date and time (according to [RFC 3339, section 5.6](http://tools.ietf.org/html/rfc3339))






## dc:creator
### Creator

An entity primarily responsible for making the resource. Examples of a creator include a person, an organization, or a service. Typically, the name of a creator should be used to indicate the entity.
XMP usage is a list of creators. Entities should be listed in order of decreasing precedence, if such order is significant.

`dc:creator`
* is optional
* type: `string[]`

* defined in this schema

### dc:creator Type


Array type: `string[]`

All items must be of the type:
`string`









## xmp:creatorTool
### Creator Tool

Name of the application which authored the asset. It takes the value present in `xmp:CreatorTool` property in XMP.
It is recommended that the value use this format convention:
Organization Software_name Version (token;token;...)
- Organization: The name of the company or organization providing the software, no SPACEs.
- Software_name: The full name of the software, SPACEs allowed.
- version: The version of the software, no SPACEs.
- tokens: Can be used to identify an operating system, plug-in, or more detailed version information.

`xmp:creatorTool`
* is optional
* type: `string`
* defined in this schema

### xmp:creatorTool Type


`string`






## xmp:modifyDate
### Mofification Date

The date and time when asset was last modified. The Date Time property should conform to ISO 8601 standard. An example form is &#34;2004-10-23T12:00:00-06:00&#34;. Opposed to `repositoryLastModifiedDate`, this is the time when the asset was last modified locally, with or without knowledge of the repository.

`xmp:modifyDate`
* is **required**
* type: `string`
* defined in this schema

### xmp:modifyDate Type


`string`
* format: `date-time` date and time (according to [RFC 3339, section 5.6](http://tools.ietf.org/html/rfc3339))






## xdm:milestone
### Milestone

A label given to a version of the asset.

`xdm:milestone`
* is optional
* type: `object`
* defined in this schema

### xdm:milestone Type

Unknown type `object`.

```json
{
  "title": "Milestone",
  "description": "A label given to a version of the asset.",
  "type": "object",
  "properties": {
    "label": {
      "title": "Milestone Label",
      "type": "string",
      "description": "Label for the version of an asset"
    },
    "description": {
      "title": "Milestone Description",
      "type": "string",
      "description": "Description for the version of an asset"
    }
  },
  "simpletype": "`object`"
}
```





## xmpRights:webStatement

A Web URL for a statement of the ownership and usage rights for this resource. This is a normal (non-URI) simple value because of historical usage.

`xmpRights:webStatement`
* is optional
* type: `string`
* defined in this schema

### xmpRights:webStatement Type


`string`






## dc:rights
### Rights

Information about rights held in and over the resource.
We can live without mentioning locale if only one entry is there. Default locale is en_us.
Locale codes should follow IETF BCP 47 standard.

`dc:rights`
* is optional
* type: reference

* defined in this schema

### dc:rights Type


Array type: reference

All items must be of the type:
* []() – `https://ns.adobe.com/xdm/assets/language-alternative#/definitions/language-alternative`








## xmpRights:marked
### Marked

When true, indicates that this is a rights-managed resource. When false, indicates that this is a public-domain resource. Omit if the state is unknown.

`xmpRights:marked`
* is optional
* type: `boolean`
* defined in this schema

### xmpRights:marked Type


`boolean`





## xmpRights:usageTerms
### Usage Terms

A collection of text instructions on how a resource can be legally used, given in a variety of languages.

`xmpRights:usageTerms`
* is optional
* type: reference

* defined in this schema

### xmpRights:usageTerms Type


Array type: reference

All items must be of the type:
* []() – `https://ns.adobe.com/xdm/assets/language-alternative#/definitions/language-alternative`








## plus:copyrightOwner
### Copyright Owners

Owner or owners of the copyright in the licensed asset.

`plus:copyrightOwner`
* is optional
* type: reference

* defined in this schema

### plus:copyrightOwner Type


Array type: reference

All items must be of the type:
* []() – `https://ns.adobe.com/xdm/assets/copyright-owner#/definitions/copyright`








## photoshop:credit
### Credit

Who should be credited when the asset is published.

`photoshop:credit`
* is optional
* type: `string`
* defined in this schema

### photoshop:credit Type


`string`






## cc:license
### License

A license is a set of requests/permissions to users of a Work, e.g. a copyright license, the public domain, information for distributors.

`cc:license`
* is optional
* type: `string`
* defined in this schema

### cc:license Type


`string`
* format: `uri` Uniformous Resource Identifier (according to [RFC3986](http://tools.ietf.org/html/rfc3986))






## cc:attributionUrl
### Attribution URL

For licenses that require attribution, such as some Creative Commons licenses, a URL that identifies the user to which a work should be attributed. When publishing to Behance, we link to the user&#39;s profile page.

`cc:attributionUrl`
* is optional
* type: `string`
* defined in this schema

### cc:attributionUrl Type


`string`
* format: `uri` Uniformous Resource Identifier (according to [RFC3986](http://tools.ietf.org/html/rfc3986))






## cc:attributionName
### Attribution Name

For licenses that require attribution, such as some Creative Commons licenses, the user to which a work is attributed. When publishing to Behance, this is taken from the user&#39;s Behance profile information.

`cc:attributionName`
* is optional
* type: `string`
* defined in this schema

### cc:attributionName Type


`string`






## xmpMM:manageUI
### Manage UI

A URI that can be used to access information about the managed resource through a web browser.

`xmpMM:manageUI`
* is optional
* type: `string`
* defined in this schema

### xmpMM:manageUI Type


`string`
* format: `uri` Uniformous Resource Identifier (according to [RFC3986](http://tools.ietf.org/html/rfc3986))






## xmpMM:manageTo
### Manage To

A URI identifying the managed resource to the asset management system; the presence of this property is the formal indication that this resource is managed. The form and content of this URI is private to the asset management system.

`xmpMM:manageTo`
* is optional
* type: `string`
* defined in this schema

### xmpMM:manageTo Type


`string`
* format: `uri` Uniformous Resource Identifier (according to [RFC3986](http://tools.ietf.org/html/rfc3986))






## xmpMM:history
### History

High-level actions that resulted in the creation of this asset. It is intended to give human readers a description of the steps taken to make the changes from the previous version to this one. The list should be at an abstract level; it is not intended to be an exhaustive keystroke or other detailed history. The description should be sufficient for metadata management, as well as for workflow enhancement.

`xmpMM:history`
* is optional
* type: reference

* defined in this schema

### xmpMM:history Type


Array type: reference

All items must be of the type:
* []() – `https://ns.adobe.com/xdm/assets/resource-event#/definitions/resource-event`








## dc:title
### Title

A name given to the resource. Typically, a Title will be a name by which the resource is formally known.

`dc:title`
* is optional
* type: reference

* defined in this schema

### dc:title Type


Array type: reference

All items must be of the type:
* []() – `https://ns.adobe.com/xdm/assets/language-alternative#/definitions/language-alternative`








## dc:description
### Description

An account of the content of the resource. Description may include but is not limited to: an abstract, table of contents, reference to a graphical representation of content or a free-text account of the content.

`dc:description`
* is optional
* type: reference

* defined in this schema

### dc:description Type


Array type: reference

All items must be of the type:
* []() – `https://ns.adobe.com/xdm/assets/language-alternative#/definitions/language-alternative`








## dc:format
### Format

The physical or digital manifestation of the resource. Typically, Format should include the media-type of the resource. Format may be used to determine the software, hardware or other equipment needed to display or operate the resource. Recommended best practice is to select a value from a controlled vocabulary (for example, the list of [Internet Media Types](http://www.iana.org/ assignments/media-types/) defining computer media formats).

`dc:format`
* is optional
* type: string
* defined in this schema

### dc:format Type

String ``.

```json
{
  "meta:usereditable": false,
  "title": "Format",
  "pattern": "\\w+\\/[-.\\w]+(?:\\+[-.\\w]+)?",
  "meta:example": "application/vnd.adobe.photoshop",
  "description": "The physical or digital manifestation of the resource. Typically, Format should include the media-type of the resource. Format may be used to determine the software, hardware or other equipment needed to display or operate the resource. Recommended best practice is to select a value from a controlled vocabulary (for example, the list of [Internet Media Types](http://www.iana.org/ assignments/media-types/) defining computer media formats).",
  "simpletype": "complex"
}
```





## xdm:notSafe
### NSFW State

Indicates if the content is SFW (safe for work). Safe is value 0 or missing value. NSFW is value 1.

`xdm:notSafe`
* is optional
* type: `enum`
* defined in this schema

The value of this property **must** be equal to one of the [known values below](#xdm:notSafe-known-values).

### xdm:notSafe Known Values
| Value | Description |
|-------|-------------|
| `0` | The content is safe for work |
| `1` | The content is not safe for work |




## dc:language
### Language

The language or languages of the resource.
Languages are specified in language code as defined in [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt), which is part of BCP 47, which is used elsewhere in XDM.

`dc:language`
* is optional
* type: `string[]`

* defined in this schema

### dc:language Type


Array type: `string[]`

All items must be of the type:
`string`


All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E((((%5BA-Za-z%5D%7B2%2C3%7D(-(%5BA-Za-z%5D%7B3%7D(-%5BA-Za-z%5D%7B3%7D)%7B0%2C2%7D))%3F)%7C%5BA-Za-z%5D%7B4%7D%7C%5BA-Za-z%5D%7B5%2C8%7D)(-(%5BA-Za-z%5D%7B4%7D))%3F(-(%5BA-Za-z%5D%7B2%7D%7C%5B0-9%5D%7B3%7D))%3F(-(%5BA-Za-z0-9%5D%7B5%2C8%7D%7C%5B0-9%5D%5BA-Za-z0-9%5D%7B3%7D))*(-(%5B0-9A-WY-Za-wy-z%5D(-%5BA-Za-z0-9%5D%7B2%2C8%7D)%2B))*(-(x(-%5BA-Za-z0-9%5D%7B1%2C8%7D)%2B))%3F)%7C(x(-%5BA-Za-z0-9%5D%7B1%2C8%7D)%2B)%7C((en-GB-oed%7Ci-ami%7Ci-bnn%7Ci-default%7Ci-enochian%7Ci-hak%7Ci-klingon%7Ci-lux%7Ci-mingo%7Ci-navajo%7Ci-pwn%7Ci-tao%7Ci-tay%7Ci-tsu%7Csgn-BE-FR%7Csgn-BE-NL%7Csgn-CH-DE)%7C(art-lojban%7Ccel-gaulish%7Cno-bok%7Cno-nyn%7Czh-guoyu%7Czh-hakka%7Czh-min%7Czh-min-nan%7Czh-xiang)))%24)):
```regex
^(((([A-Za-z]{2,3}(-([A-Za-z]{3}(-[A-Za-z]{3}){0,2}))?)|[A-Za-z]{4}|[A-Za-z]{5,8})(-([A-Za-z]{4}))?(-([A-Za-z]{2}|[0-9]{3}))?(-([A-Za-z0-9]{5,8}|[0-9][A-Za-z0-9]{3}))*(-([0-9A-WY-Za-wy-z](-[A-Za-z0-9]{2,8})+))*(-(x(-[A-Za-z0-9]{1,8})+))?)|(x(-[A-Za-z0-9]{1,8})+)|((en-GB-oed|i-ami|i-bnn|i-default|i-enochian|i-hak|i-klingon|i-lux|i-mingo|i-navajo|i-pwn|i-tao|i-tay|i-tsu|sgn-BE-FR|sgn-BE-NL|sgn-CH-DE)|(art-lojban|cel-gaulish|no-bok|no-nyn|zh-guoyu|zh-hakka|zh-min|zh-min-nan|zh-xiang)))$
```









## xdm:size
### Size

Size of the asset in bytes

`xdm:size`
* is **required**
* type: `integer`
* defined in this schema

### xdm:size Type


`integer`






## xdm:path
### Path

Shows the hierarchy of the asset. The path semantics should be same as that defined in https://tools.ietf.org/html/rfc3986#section-3.3. In case a repository is not path based then it can return the information which will help in browsing. It could be just an asset id, or something like {catalog}/{id} in case of OZ.

`xdm:path`
* is **required**
* type: `string`
* defined in this schema

### xdm:path Type


`string`






## xdm:etag
### ETag

An  ETag is an HTTP response header returned by an HTTP/1.1 compliant web server used to determine change in content of a resource at a given URL. 

`xdm:etag`
* is **required**
* type: `string`
* defined in this schema

### xdm:etag Type


`string`






## xmpTPg:NPages
### Number of pages

The number of pages in the document (including any in contained documents).

`xmpTPg:NPages`
* is optional
* type: `integer`
* defined in this schema

### xmpTPg:NPages Type


`integer`
* minimum value: `0`






## exif:gpsAltitude
### GPS Altitude

GPS tag 6, 0x06. Indicates altitude in meters.

`exif:gpsAltitude`
* is optional
* type: `number`
* defined in this schema

### exif:gpsAltitude Type


`number`






## exif:gpsAltitudeRef
### GPS Altitude Reference

GPS tag 5, 0x5. Indicates whether the altitude is above or below sea level:
0 = Above sea level
1 = Below sea level

`exif:gpsAltitudeRef`
* is optional
* type: `enum`
* defined in this schema

The value of this property **must** be equal to one of the [known values below](#exif:gpsAltitudeRef-known-values).

### exif:gpsAltitudeRef Known Values
| Value | Description |
|-------|-------------|
| `0` | The `gpsAltitude specifies a value above sea level` |
| `1` | The `gpsAltitude specifies a value below sea level |




## exif:gpsLatitude
### GPS Latitude

GPS tag 2, 0x02 (position) and 1, 0x01 (North/South). Indicates latitude. A Text value in the form “DDD,MM,SSk” or “DDD,MM.mmk”, where:
* DDD is a number of degrees
* MM is a number of minutes
* SS is a number of seconds
* mm is a fraction of minutes
* k is a single character N or S, indicating a direction (north, south)
Leading zeros are not necessary for the for DDD, MM, and SS values. The DDD,MM.mmk form should be used when any of the native Exif component rational values has a denominator other than 1. There can be any number of fractional digits.

`exif:gpsLatitude`
* is optional
* type: `string`
* defined in this schema

### exif:gpsLatitude Type


`string`


All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E%5B%5Cd%5D%7B1%2C3%7D%2C%5B%5Cd%5D%7B1%2C2%7D(%2C%5B%5Cd%5D%7B1%2C2%7D%7C.%5B%5Cd%5D%2B)%5BNS%5D%24)):
```regex
^[\d]{1,3},[\d]{1,2}(,[\d]{1,2}|.[\d]+)[NS]$
```






## exif:gpsLongitude
### GPS Longitude

GPS tag 4, 0x04 (position) and 3, 0x03 (East/West). Indicates longitude. A Text value in the form “DDD,MM,SSk” or “DDD,MM.mmk”, where:
* DDD is a number of degrees
* MM is a number of minutes
* SS is a number of seconds
* mm is a fraction of minutes
* k is a single character E or W, indicating a direction (east, west)
Leading zeros are not necessary for the for DDD, MM, and SS values. The DDD,MM.mmk form should be used when any of the native Exif component rational values has a denominator other than 1. There can be any number of fractional digits.

`exif:gpsLongitude`
* is optional
* type: `string`
* defined in this schema

### exif:gpsLongitude Type


`string`


All instances must conform to this regular expression 
(test examples [here](https://regexr.com/?expression=%5E%5B%5Cd%5D%7B1%2C3%7D%2C%5B%5Cd%5D%7B1%2C2%7D(%2C%5B%5Cd%5D%7B1%2C2%7D%7C.%5B%5Cd%5D%2B)%5BEW%5D%24)):
```regex
^[\d]{1,3},[\d]{1,2}(,[\d]{1,2}|.[\d]+)[EW]$
```






## xmp:rating
### Rating

A user-assigned rating for this file. The value shall be -1 or in the range [0..5], where -1 indicates “rejected” and 0 indicates “unrated”. If xmp:Rating is not present, a value of 0 should be assumed. NOTE: Anticipated usage is for a typical “star rating” UI, with the addition of a notion of rejection.

`xmp:rating`
* is optional
* type: `enum`
* defined in this schema

The value of this property **must** be equal to one of the [known values below](#xmp:rating-known-values).

### xmp:rating Known Values
| Value | Description |
|-------|-------------|
| `0` |  |
| `1` | ⭑ |
| `2` | ⭑⭑ |
| `3` | ⭑⭑⭑ |
| `4` | ⭑⭑⭑⭑ |
| `5` | ⭑⭑⭑⭑⭑ |
| `-1` | rejected |




## dc:subject
### Subject

Set of descriptive phrases or keywords that describe the content of the resource. These keywords are part of the XMP metadata of the asset. Compare this with the `keyword` and `machineKeywords` properties, which provide more structure and context.

`dc:subject`
* is optional
* type: `string[]`

* defined in this schema

### dc:subject Type


Array type: `string[]`

All items must be of the type:
`string`









## xmp:keywords
### Keywords

The `keywords` property is used to track human-assigned descriptive phrases like keywords or tags of an asset. Rather than a plan list of tags, it is a structured set of keywords, where keywords can have an explicit importance ranking and a locale. This allows the management of multi-lingual keywords for a given asset. For machine-generated keywords, use the `machineKeywords` property. 

`xmp:keywords`
* is optional
* type: `array`

* defined in this schema

### xmp:keywords Type


Array type: `array`

All items must be of the type:
Unknown type `array`.

```json
{
  "type": "array",
  "title": "Keywords",
  "items": {
    "$schema": "http://json-schema.org/draft-06/schema#",
    "title": "Keyword",
    "description": "The `Keyword` schema describes a keyword in a list of keywords, with specific locale and importance relative to other keywords in the same list.",
    "properties": {
      "value": {
        "title": "Value",
        "description": "The keyword itself. A keyword can be considered like a tag, i.e. a short description of the content of the asset.",
        "type": "string"
      },
      "localeCode": {
        "type": "string",
        "pattern": "^(((([A-Za-z]{2,3}(-([A-Za-z]{3}(-[A-Za-z]{3}){0,2}))?)|[A-Za-z]{4}|[A-Za-z]{5,8})(-([A-Za-z]{4}))?(-([A-Za-z]{2}|[0-9]{3}))?(-([A-Za-z0-9]{5,8}|[0-9][A-Za-z0-9]{3}))*(-([0-9A-WY-Za-wy-z](-[A-Za-z0-9]{2,8})+))*(-(x(-[A-Za-z0-9]{1,8})+))?)|(x(-[A-Za-z0-9]{1,8})+)|((en-GB-oed|i-ami|i-bnn|i-default|i-enochian|i-hak|i-klingon|i-lux|i-mingo|i-navajo|i-pwn|i-tao|i-tay|i-tsu|sgn-BE-FR|sgn-BE-NL|sgn-CH-DE)|(art-lojban|cel-gaulish|no-bok|no-nyn|zh-guoyu|zh-hakka|zh-min|zh-min-nan|zh-xiang)))$",
        "description": "Language of the keyword. The locale code should follow [RFC BCP 47](https://tools.ietf.org/html/bcp47)",
        "meta:example": [
          "en-US",
          "de-CH"
        ]
      },
      "importance": {
        "type": "number",
        "title": "Importance",
        "minimum": 0,
        "maximum": 1,
        "description": "The importance of the keyword on a scale from zero to one. If required repository will infer it as per its policies and add it for the keywords"
      }
    },
    "required": [
      "value"
    ],
    "simpletype": "complex"
  },
  "description": "The `keywords` property is used to track human-assigned descriptive phrases like keywords or tags of an asset. Rather than a plan list of tags, it is a structured set of keywords, where keywords can have an explicit importance ranking and a locale. This allows the management of multi-lingual keywords for a given asset. For machine-generated keywords, use the `machineKeywords` property. ",
  "simpletype": "`array`"
}
```


  
The `Keyword` schema describes a keyword in a list of keywords, with specific locale and importance relative to other keywords in the same list.







## xmp:machineKeywords

The `machineKeywords` property is used to track machine-assigned descriptive phrases like keywords or tags of an asset. Rather than a plan list of tags, it is a structured set of keywords, where keywords can have an explicit confidence ranking and a locale. For human-defined keywords, use the `keywords` property. 

`xmp:machineKeywords`
* is optional
* type: `array`

* defined in this schema

### xmp:machineKeywords Type


Array type: `array`

All items must be of the type:
Unknown type `array`.

```json
{
  "meta:usereditable": false,
  "type": "array",
  "items": {
    "$schema": "http://json-schema.org/draft-06/schema#",
    "properties": {
      "confidence": {
        "type": "number",
        "minimum": 0,
        "maximum": 1,
        "description": "Confidence of the algorithm that this keyword is applicable to the asset. Confidence values are numbers between zero and one. A value of .95 indicates that the algorithm expects less than 5% of all tags with the same confidence value to be mis-applied, i.e. not to be a proper description of the asset."
      },
      "algorithm": {
        "type": "string",
        "description": "Name of the algorithm which generated the keyword."
      },
      "value": {
        "type": "string",
        "description": "The keyword itself. A keyword can be considered like a tag, i.e. a short description of the content of the asset."
      },
      "localeCode": {
        "type": "string",
        "pattern": "^(((([A-Za-z]{2,3}(-([A-Za-z]{3}(-[A-Za-z]{3}){0,2}))?)|[A-Za-z]{4}|[A-Za-z]{5,8})(-([A-Za-z]{4}))?(-([A-Za-z]{2}|[0-9]{3}))?(-([A-Za-z0-9]{5,8}|[0-9][A-Za-z0-9]{3}))*(-([0-9A-WY-Za-wy-z](-[A-Za-z0-9]{2,8})+))*(-(x(-[A-Za-z0-9]{1,8})+))?)|(x(-[A-Za-z0-9]{1,8})+)|((en-GB-oed|i-ami|i-bnn|i-default|i-enochian|i-hak|i-klingon|i-lux|i-mingo|i-navajo|i-pwn|i-tao|i-tay|i-tsu|sgn-BE-FR|sgn-BE-NL|sgn-CH-DE)|(art-lojban|cel-gaulish|no-bok|no-nyn|zh-guoyu|zh-hakka|zh-min|zh-min-nan|zh-xiang)))$",
        "description": "Language of the keyword. The locale code should follow [RFC BCP47](https://tools.ietf.org/html/bcp47)"
      }
    },
    "simpletype": "complex"
  },
  "description": "The `machineKeywords` property is used to track machine-assigned descriptive phrases like keywords or tags of an asset. Rather than a plan list of tags, it is a structured set of keywords, where keywords can have an explicit confidence ranking and a locale. For human-defined keywords, use the `keywords` property. ",
  "simpletype": "`array`"
}
```








## xmp:fonts
### Fonts

This is a list of fonts and typefaces that are used in the document. The order of fonts does not matter.

`xmp:fonts`
* is optional
* type: reference

* defined in this schema

### xmp:fonts Type


Array type: reference

All items must be of the type:
* []() – `https://ns.adobe.com/xdm/assets/font#/definitions/font`








## xmp:layers



`xmp:layers`
* is optional
* type: complex
* defined in this schema

### xmp:layers Type

Unknown type ``.

```json
{
  "properties": {
    "xdm:name": {
      "type": "string",
      "title": "Name",
      "description": "Name of the Layer Group. This will be visible to the user and users can specify names that can help them to identify different Layer Groups"
    },
    "xdm:layers": {
      "name": "Layers",
      "description": "The layers or layer groups contained in this layer group.",
      "type": "array",
      "items": {
        "anyOf": [
          {
            "$ref": "#/definitions/layer-group"
          },
          {
            "$ref": "https://ns.adobe.com/xdm/assets/layer#/definitions/layer"
          }
        ]
      }
    }
  },
  "simpletype": "complex"
}
```





## xmp:artboards
### Artboards

Contains the artboards that are being used in the document. A document can have multiple artboards.

`xmp:artboards`
* is optional
* type: Artboard

* defined in this schema

### xmp:artboards Type


Array type: Artboard

All items must be of the type:
* [Artboard](artboard.schema.md) – `https://ns.adobe.com/xdm/assets/artboard`






