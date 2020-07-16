# Multilinguality

## General approach

Multilingual aspects related to the evidence descriptions concern all attributes whose contents are expressed as strings with human-readable text. Wherever such properties are used, the string values are of one of two types:
•	The string is free text. Examples are descriptions and labels. Such text may be translated into several languages.
•	The string is an appellation of a ‘named entity’. Examples are names of organisations or persons. These names may have parallel versions in other languages but those versions don’t need to be literal translations.

Wherever values of attributes are expressed with either type of string, the attribute can be repeated with translations in the case of free text and with parallel versions in case of named entities. 
For free text, e.g. in the cases of titles, descriptions and keywords, the language tag is mandatory. For named entities, the language tag is optional and should only be provided if the parallel version of the name is strictly associated with a particular language. For example, the name ‘European Union’ has parallel versions in all official languages of the union, while a name like ‘W3C’ is not associated with a particular language and has no parallel versions.

## Examples

Language tags to be used are defined by [BCP47](http://tools.ietf.org/html/bcp47). Examples are:
### XML
```
<description xml:lang="en">Birth certificate</description>
<description xml:lang="nl">Geboorteakte</description>

<geographicName xml:lang="en">Sofia</geoGraphicName>
<geographicName xml:lang="bg-Cyrl">София</geoGraphicName>
<geographicName xml:lang="bg-Latn">Sofiya</geoGraphicName>
```

### RDF
```
dct:description "Birth certificate"@en
dct:description "Geboorteakte"@nl

locn:geographicName "Sofia"@en ;
locn:geographicName "София"@bg-Cyrl ;
locn:geographicName "Sofiya"@bg-Latn .
```

## Automated translations

This approach also allows for the tagging of automated translations using the "t" extension for text transformations defined in [RFC6497](http://tools.ietf.org/html/rfc6497) with the field "t0" indicating a machine translation. In the case of automatically translated text, a language tag will look like: "en-t-es-t0-abcd", which conveys the information that the string is in English, translated from Spanish by machine translation using a tool named "abcd".

## Language versions of web pages

For linking to different language versions of associated web pages (e.g. landing pages) or documentation, a [content negotiation](http://httpd.apache.org/docs/current/content-negotiation.html) mechanism may be used whereby different content is served based on the Accept-Languages indicated by the browser.

Using such a mechanism, the link to the page or document can resolve to different language versions of the page or document.

## Links

* [Internet Engineering Task Force (IETF). BCP47. Tags for Identifying Languages.](http://tools.ietf.org/html/bcp47)
* [Internet Engineering Task Force (IETF). BCP47 Extension T – Transformed Content.](http://tools.ietf.org/html/rfc6497)
* [Apache Web Server: content negotiation.](http://httpd.apache.org/docs/current/content-negotiation.html)
