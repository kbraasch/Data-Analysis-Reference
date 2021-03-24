# Data Classification

## Quantitative

Numeric data that represents quantity, measurement, calculation, etc.

- Discrete: Data that can only take certain values, often integer numbers.
- Continuous: Data that can take any value within a range.

## Qualitative

Data that describes qualities or characteristics. Often collected in text form.

- Categorical
  - Nominal: The categories do not have a natural ordering.
  - Ordinal: The categories have a natural ordering.
- Unstructured response

## Boolean

Data with only two possible values, and is represented in terms of truth logic. It is either true, or false (1 or 0).

<br>

# Structured Data (Tabular)

## Excel (.xls)

### Data Types

<!-- prettier-ignore -->
| Excel Type | Description | NumPy Type | Standard |
| --- | --- | --- | --- |
| Whole Number   | 64 bit integer <br> [-9,223,372,036,854,775,808 (-2^63) to 9,223,372,036,854,775,807 (2^63-1)] | int64 | |
| Decimal Number | 64 bit real number <br> [-1.79E +308 through -2.23E -308] <br> Zero <br> [2.23E -308 through 1.79E + 308] <br> Limited to 15 decimal digits | float64 | [IEEE 745](https://en.wikipedia.org/wiki/Double-precision_floating-point_format) <br> _nan_ <br> _-inf_ <br> _inf_ |
| True/False | Boolean | bool\_ | |
| Text | Unicode character string <br> max length 268,435,456 Unicode characters or 536,870,912 bytes | object |
| Date | Date-time <br> dates after January 1, 1900 | datetime64 | |
| Currency | [-922,337,203,685,477.5808 to 922,337,203,685,477.5807] <br> 4 decimal place fixed precision | float64 |
| N/A | Empty cell | [nan](https://numpy.org/doc/stable/user/misc.html) | |

Extracting min/max data from numeric columns would allow for smaller types to be assigned on import, reducing memory usage.

### Metadata

[OpenPyXl](openpyxl.readthedocs.io) is available to pull cell data and file properties.

<br>

## CSV (.csv)

### Datatypes

W3C provides a [Model for Tabular Data and Metadata on the Web](https://www.w3.org/TR/tabular-data-model/) recommendation which specifies the following data types for a tabular model.

![W3C Tabular Type Recommendation](/tabular_datatypes.png)

[Pandas](https://pandas.pydata.org/) will attempt to infer data types when reading in a CSV. If the metadata has specified data types, you can pass them to the parser, however the parser will pass the values through the 64 bit types before downcasting.
[Here is a short read](https://rushter.com/blog/pandas-data-type-inference/) about how Pandas attempts to infer data types and potential typing errors.

### Metadata

W3C recommends [Metadata Vocabulary for Tabular Data](https://www.w3.org/TR/2015/REC-tabular-metadata-20151217/) as a method of using a JSON file to describe the dataset. Additionally in this recommendation is a method for creating and managing relational table groups, even without a relational database management software. For most CSV applications, the JSON file would begin at the "Table" level.

![W3C Tabular Metadata Recommendation](/metadata_format_recommendation.png)

<br>

## SQL Database (.DB, .SQLITE3, .ACCDB, etc.)

### Datatypes ([More details](https://www.journaldev.com/16774/sql-data-types))

<!-- prettier-ignore -->
| Category | Data Types | |
| --- | --- | --- |
| Numeric | bit <br> tinyint <br> smallint <br> int <br> bigint | decimal <br> numeric <br> float <br> real |
| Date/Time | Date <br> Time <br> Datetime | Timestamp <br> Year|
| Character/String | Char <br> Varchar | Text <br> Varchar (max) |
| Unicode Character/<br>String | NChar <br> NVarchar | NText <br> NVarchar (max) |
| Binary | Binary <br> Varbinary | Image <br> Varbinary (max) |
| Miscellaneous | Clob <br> Blob | XML <br> JSON |

### Metadata

Catalog Views or Data Dictionary Views are standard views in most relational databases that provide access to metadata.

Usually consists of:

- Schema (tables, columns, constraints, foreign keys, indexes, and sequences)
- Programs (views, functions, procedures, and triggers)
- Security (users, groups, and privileges)
- Physical implementation (Partitions, files, and backups)
- Storage (Table dimensions and storage size)
- Auditing (Session, connection, and query history)

<br>

# Unstructured Data

Unstructured data does not have a pre-defined structure and comes in many forms. Most data is unstructured data. It comes in the form of text documents, images, video, audio, etc.

## Documents (.txt, .doc, PDF, RTF, HTML, etc.)

Files containing binary or text and sometimes formatting parameters. Some more complex [document types](https://en.wikipedia.org/wiki/Document_file_format) can include multimedia data. Often the documents have a specified encoding, typically [ASCII](https://en.wikipedia.org/wiki/ASCII). Usually have end-of-line delimiters for processing.

### Metadata

- [.doc](https://support.microsoft.com/en-us/topic/view-or-change-the-properties-for-an-office-file-21d604c2-481e-4379-8e54-1dd4622c6b75)
- [PDF](https://helpx.adobe.com/acrobat/using/pdf-properties-metadata.html)
- [RTF](https://en.wikipedia.org/wiki/Rich_Text_Format#Common_uses_and_interoperability)
- [HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML)

<br>

## Images (PNG, JPEG, GIF, TIFF, Bitmap, RAW, etc.)

[Image files](https://en.wikipedia.org/wiki/Image_file_formats) are composed of digital data in an uncompressed format, a compressed format (which may be lossless or lossy), or a vector format so that the data can be rasterized for use on a computer display. Rasterization converts the image data into a grid of pixels. Each pixel has a number of bits to designate its color (and in some formats, its transparency).

### Metadata

- [Exchangeable image file format (Exif)](https://en.wikipedia.org/wiki/Exif) is a standard for digital image capture. Supported by [JPEG](https://dev.exiv2.org/projects/exiv2/wiki/The_Metadata_in_JPEG_files), [TIFF](https://dev.exiv2.org/projects/exiv2/wiki/The_Metadata_in_TIFF_files), .WAV, & [PNG](https://dev.exiv2.org/projects/exiv2/wiki/The_Metadata_in_PNG_files)
- IPTC offers an [overview and standard](https://iptc.org/standards/photo-metadata/photo-metadata/) for photo metadata

<br>

# Semi-structured

[Semi-structured data](https://en.wikipedia.org/wiki/Semi-structured_data) is a form of structured data that does not obey the tabular structure of data models associated with relational databases or other forms of data tables, but nonetheless contains tags or other markers to separate semantic elements and enforce hierarchies of records and fields within the data.

## JavaScript Object Notation (JSON)

[JSON](https://en.wikipedia.org/wiki/JSON) is an open standard format that uses human-readable text to transmit data objects consisting of attribute–value pairs.  
Key-value pairs are stored within an object-like nesting structure.  
`{ `<br> &nbsp;&nbsp;&nbsp;` "key": value,`<br>`}`

### Data Types

- Number
- String
- Boolean
- Array
- Object
- null

### Schema & Metadata

JSON Schema offers a [specification](https://json-schema.org/specification.html) and [guide to implementing](https://json-schema.org/) JSON document annotation and validation.

<br>

## Extensible Markup Language (XML)

[XML](https://en.wikipedia.org/wiki/XML) is a markup language that defines a set of rules for encoding documents in a format that is both human-readable and machine-readable. An XML document is a string of characters. It is more complicated than JSON.

### Concepts

- **Character** - [Unicode](https://en.wikipedia.org/wiki/Unicode) character
- **Processor and application** - processor analyzes the markup and passes structured information to the application.
- **Markup and content** - Markup is for machine processing, content is everything else intended for human consumption.
- **Tag** - Machine processed markup (begins with < ends with >).
- **Element** - Logical document component enclosed in tags.
- **Attribute** - A markup consisting of a name-value pair.
- **XML declaration** - Header in XML document to describe document details.

### Schema & Metadata

W3C provides a recommendation for [XML schema](https://www.w3.org/TR/xmlschema-1/). Metadata is typically supplied in schema files.

<br>

# Metadata

Data that helps describe the content or characteristics of a file.  
Adobe's [Extensible Metadata Platform (XMP)](https://www.adobe.com/products/xmp.html) is a file labeling technology that lets you embed metadata into files themselves during the content creation process and can be used as a single solution for all file types.

<!-- # Time Series # Big Data -->
