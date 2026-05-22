
# DCAT-DataService/Records binding (Schema)

`geonovum-labs.bbr.dcat.dcat-dataservice-records` *v0.1*

DCAT profile of OGC API Records binds the OGC API Records schema to a DCAT Dataservice. This is the baseline for semantic equivalence of OGC API records and a DCAT DataService.

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## DCAT DataService baseline bound to OGC API records schema

This building block defines a binding from OGC API Records schema to the DCAT DataService Class.



__NOTE:__ Still work in progress !! context mapping is not complete for example

![dcat-classes](./assets/dcat-classes.png)
## Examples

### DCAT DataService with OGC API Records in JSON
An example based on the BAG API metadata record . 
Converted in JSON so the Semantic uplift via a JSON-LD context can be shown.
#### json
```json
{
  "type": "Feature",
  "conformsTo": [
    "http://www.opengis.net/spec/ogcapi-records-1/1.0/req/record-core"
  ],
  "id": "urn:ogc:record:bag-api",
  "geometry": {
    "type": "Polygon",
    "coordinates": [
      [
        [ 2.4807, 53.7187 ],
        [ 7.9685, 53.7187 ],
        [ 7.9685, 50.6058 ],
        [ 2.4807, 50.6058 ],  
        [ 2.4807, 53.7187 ]
      ]
    ]
  },
  "properties": {
    "type": "DataService",
    "contactPoint": {
      "organizationName": "Directie Operatie, Dienstverlening en Registratie, afdeling Data-, Proces- en Informatiemanagement",
      "email": "mailto:dpi-gi@kadaster.nl"
    },
    "accessRights": "http://inspire.ec.europa.eu/metadata-codelist/ConditionsApplyingToAccessAndUse/noConditionsApply",
    "created": "2013-02-18",
    "description": "De gegevens bestaan uit BAG-panden en een deelselectie van BAG-gegevens van deze panden en de zich daarin bevindende verblijfsobjecten. Ook de ligplaatsen en standplaatsen zijn hierin opgenomen met een deelselectie van BAG-gegevens. De gegevens van de nummeraanduiding zijn in deze services onderdeel van de adresseerbare objecten, hierbij wordt slechts 1 adres opgenomen, dus objecten met meerdere adressen (hoofd- en nevenadressen) zijn niet compleet. In deze services zitten dus niet alle BAG adressen. Aangezien niet alle BAG gegevens worden geleverd, adviseren wij u om de actuele gegevens in één van de BAG producten te controleren. Raadpleeg de BAG Viewer voor enkele bevragingen van BAG gegevens. Een overzicht van alle beschikbare producten kunt u vinden op de website https://www.kadaster.nl/zakelijk/registraties/basisregistraties/bag . De BAG WMS, BAG WFS en BAG API Individuele bevragingen zijn expliciet niet bedoeld voor bulkbevragingen waarmee veel gegevens in één keer worden opgevraagd en in een database worden verwerkt. Wilt u in één keer meer gegevens opvragen, dan raden wij u aan om gebruik te maken van onze BAG Geopackage (https://www.kadaster.nl/zakelijk/producten/adressen-en-gebouwen/bag-geopackage) of BAG extract (https://www.kadaster.nl/zakelijk/producten/adressen-en-gebouwen/bag-2.0-extract). De BAG Geopackage en de BAG extract kunt u downloaden via de Atom downloadservice: https://service.pdok.nl/lv/bag/atom/bag.xml . Deze dataset wordt ook gebruikt voor het ontsluiten van het INSPIRE thema Gebouwen. Het betreft gebouwcontouren, constructieve onderdelen van gebouwen en ruimtelijke barrieres. Dit betreft niet-geharmoniseerde data uit de basisregistratie Adressen en Gebouwen (BAG). De service wordt dagelijks geactualiseerd.",
    "identifier": "5c075a13-9194-4ad3-bf37-e46a0f4727bc",
    "language": {
      "code": "http://publications.europa.eu/resource/authority/language/DUT",
      "name": "Dutch"
    },
    "provenance": {
      "description": "Ontwikkeld uit de Basisregistratie Adressen en Gebouwen (BAG)"
    },
    "title": "BAG OGC API Features",
    "publisher": {
      "name": "Klantcontactcenter",
      "email": "mailto:bag@kadaster.nl"
    },
    "creator": {
      "name": "Kadaster",
      "email": null
    },
    "keywords": [
      "building",
      "base registry"
    ],
    "servesDataset": "urn:ogc:record:bag-dataset"
  },
  "links": [
    {
      "rel": "related",
      "href": "https://bag-dataset",
      "type": "Dataset"
    }
  ]
}
```

#### jsonld
```jsonld
{
  "@context": "https://geonovum.github.io/bblock-dcat-ap-nl/build/annotated/bbr/dcat/dcat-dataservice-records/context.jsonld",
  "type": "Feature",
  "conformsTo": [
    "http://www.opengis.net/spec/ogcapi-records-1/1.0/req/record-core"
  ],
  "id": "urn:ogc:record:bag-api",
  "geometry": {
    "type": "Polygon",
    "coordinates": [
      [
        [
          2.4807,
          53.7187
        ],
        [
          7.9685,
          53.7187
        ],
        [
          7.9685,
          50.6058
        ],
        [
          2.4807,
          50.6058
        ],
        [
          2.4807,
          53.7187
        ]
      ]
    ]
  },
  "properties": {
    "type": "DataService",
    "contactPoint": {
      "organizationName": "Directie Operatie, Dienstverlening en Registratie, afdeling Data-, Proces- en Informatiemanagement",
      "email": "mailto:dpi-gi@kadaster.nl"
    },
    "accessRights": "http://inspire.ec.europa.eu/metadata-codelist/ConditionsApplyingToAccessAndUse/noConditionsApply",
    "created": "2013-02-18",
    "description": "De gegevens bestaan uit BAG-panden en een deelselectie van BAG-gegevens van deze panden en de zich daarin bevindende verblijfsobjecten. Ook de ligplaatsen en standplaatsen zijn hierin opgenomen met een deelselectie van BAG-gegevens. De gegevens van de nummeraanduiding zijn in deze services onderdeel van de adresseerbare objecten, hierbij wordt slechts 1 adres opgenomen, dus objecten met meerdere adressen (hoofd- en nevenadressen) zijn niet compleet. In deze services zitten dus niet alle BAG adressen. Aangezien niet alle BAG gegevens worden geleverd, adviseren wij u om de actuele gegevens in \u00e9\u00e9n van de BAG producten te controleren. Raadpleeg de BAG Viewer voor enkele bevragingen van BAG gegevens. Een overzicht van alle beschikbare producten kunt u vinden op de website https://www.kadaster.nl/zakelijk/registraties/basisregistraties/bag . De BAG WMS, BAG WFS en BAG API Individuele bevragingen zijn expliciet niet bedoeld voor bulkbevragingen waarmee veel gegevens in \u00e9\u00e9n keer worden opgevraagd en in een database worden verwerkt. Wilt u in \u00e9\u00e9n keer meer gegevens opvragen, dan raden wij u aan om gebruik te maken van onze BAG Geopackage (https://www.kadaster.nl/zakelijk/producten/adressen-en-gebouwen/bag-geopackage) of BAG extract (https://www.kadaster.nl/zakelijk/producten/adressen-en-gebouwen/bag-2.0-extract). De BAG Geopackage en de BAG extract kunt u downloaden via de Atom downloadservice: https://service.pdok.nl/lv/bag/atom/bag.xml . Deze dataset wordt ook gebruikt voor het ontsluiten van het INSPIRE thema Gebouwen. Het betreft gebouwcontouren, constructieve onderdelen van gebouwen en ruimtelijke barrieres. Dit betreft niet-geharmoniseerde data uit de basisregistratie Adressen en Gebouwen (BAG). De service wordt dagelijks geactualiseerd.",
    "identifier": "5c075a13-9194-4ad3-bf37-e46a0f4727bc",
    "language": {
      "code": "http://publications.europa.eu/resource/authority/language/DUT",
      "name": "Dutch"
    },
    "provenance": {
      "description": "Ontwikkeld uit de Basisregistratie Adressen en Gebouwen (BAG)"
    },
    "title": "BAG OGC API Features",
    "publisher": {
      "name": "Klantcontactcenter",
      "email": "mailto:bag@kadaster.nl"
    },
    "creator": {
      "name": "Kadaster",
      "email": null
    },
    "keywords": [
      "building",
      "base registry"
    ],
    "servesDataset": "urn:ogc:record:bag-dataset"
  },
  "links": [
    {
      "rel": "related",
      "href": "https://bag-dataset",
      "type": "Dataset"
    }
  ]
}
```

#### ttl
```ttl
@prefix dcat: <http://www.w3.org/ns/dcat#> .
@prefix dct: <http://purl.org/dc/terms/> .
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix ns1: <http://www.iana.org/assignments/> .
@prefix oa: <http://www.w3.org/ns/oa#> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix rec: <https://www.opengis.net/def/ogc-api/records/> .
@prefix skos: <http://www.w3.org/2004/02/skos/core#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<urn:ogc:record:bag-api> a <file:///github/workspace/DataService>,
        geojson:Feature ;
    dct:conformsTo <http://www.opengis.net/spec/ogcapi-records-1/1.0/req/record-core> ;
    dct:created "2013-02-18" ;
    dct:description "De gegevens bestaan uit BAG-panden en een deelselectie van BAG-gegevens van deze panden en de zich daarin bevindende verblijfsobjecten. Ook de ligplaatsen en standplaatsen zijn hierin opgenomen met een deelselectie van BAG-gegevens. De gegevens van de nummeraanduiding zijn in deze services onderdeel van de adresseerbare objecten, hierbij wordt slechts 1 adres opgenomen, dus objecten met meerdere adressen (hoofd- en nevenadressen) zijn niet compleet. In deze services zitten dus niet alle BAG adressen. Aangezien niet alle BAG gegevens worden geleverd, adviseren wij u om de actuele gegevens in één van de BAG producten te controleren. Raadpleeg de BAG Viewer voor enkele bevragingen van BAG gegevens. Een overzicht van alle beschikbare producten kunt u vinden op de website https://www.kadaster.nl/zakelijk/registraties/basisregistraties/bag . De BAG WMS, BAG WFS en BAG API Individuele bevragingen zijn expliciet niet bedoeld voor bulkbevragingen waarmee veel gegevens in één keer worden opgevraagd en in een database worden verwerkt. Wilt u in één keer meer gegevens opvragen, dan raden wij u aan om gebruik te maken van onze BAG Geopackage (https://www.kadaster.nl/zakelijk/producten/adressen-en-gebouwen/bag-geopackage) of BAG extract (https://www.kadaster.nl/zakelijk/producten/adressen-en-gebouwen/bag-2.0-extract). De BAG Geopackage en de BAG extract kunt u downloaden via de Atom downloadservice: https://service.pdok.nl/lv/bag/atom/bag.xml . Deze dataset wordt ook gebruikt voor het ontsluiten van het INSPIRE thema Gebouwen. Het betreft gebouwcontouren, constructieve onderdelen van gebouwen en ruimtelijke barrieres. Dit betreft niet-geharmoniseerde data uit de basisregistratie Adressen en Gebouwen (BAG). De service wordt dagelijks geactualiseerd." ;
    dct:title "BAG OGC API Features" ;
    rdfs:seeAlso [ a <file:///github/workspace/Dataset> ;
            ns1:relation <http://www.iana.org/assignments/relation/related> ;
            oa:hasTarget <https://bag-dataset> ] ;
    dcat:keyword "base registry",
        "building" ;
    geojson:geometry [ a geojson:Polygon ;
            geojson:coordinates ( ( ( 2.4807e+00 5.37187e+01 ) ( 7.9685e+00 5.37187e+01 ) ( 7.9685e+00 5.06058e+01 ) ( 2.4807e+00 5.06058e+01 ) ( 2.4807e+00 5.37187e+01 ) ) ) ] ;
    rec:language [ skos:prefLabel "Dutch" ;
            rec:languageCode "http://publications.europa.eu/resource/authority/language/DUT" ] .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$id: https://geonovum-labs.bbr.dcat.dataservice-records.json
title: DCAT DataService OGC API record definition
description: DCAT DataService OGC API record definition
allOf:
- $ref: https://ogcincubator.github.io/geodcat-ogcapi-records/build/annotated/geo/geodcat/dcat-records/schema.yaml
properties:
  properties:
    type: object
    required:
    - type
    properties:
      type:
        type: string
        enum:
        - DataService
        x-jsonld-id: '@type'
    x-jsonld-id: '@nest'
  links:
    type: array
    minItems: 1
    items:
      $ref: '#/definitions/Link'
    x-jsonld-id: http://www.w3.org/2000/01/rdf-schema#seeAlso
    x-jsonld-extra-terms:
      hreflang: http://purl.org/dc/terms/language
      length: http://purl.org/dc/terms/extent
      distribution:
        x-jsonld-context:
          mediaType: https://www.opengis.net/def/ogc-api/records/mediaType
          name: https://www.opengis.net/def/ogc-api/records/name
          description: https://www.opengis.net/def/ogc-api/records/description
          license: https://www.opengis.net/def/ogc-api/records/license
          accessRights: https://www.opengis.net/def/ogc-api/records/accessRights
          conformsTo:
            '@container': '@set'
            '@id': http://purl.org/dc/terms/conformsTo
            '@type': '@id'
        x-jsonld-id: http://www.w3.org/ns/dcat#distribution
        x-jsonld-type: '@id'
definitions:
  Link:
    title: Link object definition
    description: Link object definition including distribution
    type: object
    required:
    - href
    properties:
      href:
        type: string
        format: uri
        x-jsonld-type: '@id'
        x-jsonld-id: http://www.w3.org/ns/oa#hasTarget
      rel:
        type: string
        x-jsonld-id: http://www.iana.org/assignments/relation
        x-jsonld-type: '@id'
        x-jsonld-base: http://www.iana.org/assignments/relation/
      type:
        type: string
        x-jsonld-id: '@type'
      title:
        type: string
        x-jsonld-container: '@set'
        x-jsonld-id: http://purl.org/dc/terms/title
  LanguageMap:
    type: object
    description: A language-mapped string where keys are BCP 47 language tags and
      values are the localized strings.
    patternProperties:
      ^[a-zA-Z]{2,8}(-[a-zA-Z0-9]{2,8})*$:
        type: string
    additionalProperties: false
  MultilingualString:
    oneOf:
    - type: string
    - $ref: '#/definitions/LanguageMap'
x-jsonld-extra-terms:
  Feature: https://purl.org/geojson/vocab#Feature
  FeatureCollection: https://purl.org/geojson/vocab#FeatureCollection
  GeometryCollection: https://purl.org/geojson/vocab#GeometryCollection
  LineString: https://purl.org/geojson/vocab#LineString
  MultiLineString: https://purl.org/geojson/vocab#MultiLineString
  MultiPoint: https://purl.org/geojson/vocab#MultiPoint
  MultiPolygon: https://purl.org/geojson/vocab#MultiPolygon
  Point: https://purl.org/geojson/vocab#Point
  Polygon: https://purl.org/geojson/vocab#Polygon
  features:
    x-jsonld-container: '@set'
    x-jsonld-id: https://purl.org/geojson/vocab#features
  id: '@id'
  geometry:
    x-jsonld-context:
      coordinates:
        '@container': '@list'
        '@id': https://purl.org/geojson/vocab#coordinates
    x-jsonld-id: https://purl.org/geojson/vocab#geometry
  bbox:
    x-jsonld-container: '@list'
    x-jsonld-id: https://purl.org/geojson/vocab#bbox
  conformsTo:
    x-jsonld-container: '@set'
    x-jsonld-id: http://purl.org/dc/terms/conformsTo
    x-jsonld-type: '@id'
  time: http://purl.org/dc/terms/temporal
  linkTemplates:
    x-jsonld-context:
      rel:
        '@context':
          '@base': http://www.iana.org/assignments/relation/
        '@id': http://www.iana.org/assignments/relation
        '@type': '@id'
      type: http://purl.org/dc/terms/format
      hreflang: http://purl.org/dc/terms/language
      title: http://www.w3.org/2000/01/rdf-schema#label
      length: http://purl.org/dc/terms/extent
      uriTemplate:
        '@type': http://www.w3.org/2001/XMLSchema#string
        '@id': https://www.opengis.net/def/ogc-api/records/uriTemplate
      varBase: https://www.opengis.net/def/ogc-api/records/varBase
      variables:
        '@id': https://www.opengis.net/def/ogc-api/records/hasVariable
        '@container': '@index'
        '@index': http://purl.org/dc/terms/identifier
    x-jsonld-id: https://www.opengis.net/def/ogc-api/records/hasLinkTemplate
  created: http://purl.org/dc/terms/created
  updated: http://purl.org/dc/terms/modified
  description:
    x-jsonld-container: '@set'
    x-jsonld-id: http://purl.org/dc/terms/description
  keywords:
    x-jsonld-container: '@set'
    x-jsonld-id: http://www.w3.org/ns/dcat#keyword
  language:
    x-jsonld-id: https://www.opengis.net/def/ogc-api/records/language
    x-jsonld-context:
      code: https://www.opengis.net/def/ogc-api/records/languageCode
      name: http://www.w3.org/2004/02/skos/core#prefLabel
  languages:
    x-jsonld-container: '@set'
    x-jsonld-id: https://www.opengis.net/def/ogc-api/records/languages
    x-jsonld-context:
      code: https://www.opengis.net/def/ogc-api/records/languageCode
      name: http://www.w3.org/2004/02/skos/core#prefLabel
  resourceLanguages:
    x-jsonld-container: '@set'
    x-jsonld-id: https://www.opengis.net/def/ogc-api/records/resourceLanguages
    x-jsonld-context:
      code: https://www.opengis.net/def/ogc-api/records/languageCode
      name: http://www.w3.org/2004/02/skos/core#prefLabel
  externalIds:
    x-jsonld-container: '@set'
    x-jsonld-id: https://www.opengis.net/def/ogc-api/records/scopedIdentifier
    x-jsonld-context:
      scheme: https://www.opengis.net/def/ogc-api/records/scheme
      value: https://www.opengis.net/def/ogc-api/records/id
  themes:
    x-jsonld-container: '@set'
    x-jsonld-id: https://www.opengis.net/def/ogc-api/records/themes
    x-jsonld-context:
      concepts:
        '@id': https://w3id.org/ogc/stac/themes/concepts
        '@context':
          id:
            '@type': http://www.w3.org/2001/XMLSchema#string
            '@id': https://w3id.org/ogc/stac/themes/id
          url:
            '@type': '@id'
            '@id': '@id'
        '@container': '@set'
      scheme: https://w3id.org/ogc/stac/themes/scheme
  formats:
    x-jsonld-id: https://www.opengis.net/def/ogc-api/records/format
    x-jsonld-context:
      name: https://www.opengis.net/def/ogc-api/records/name
      mediaType: https://www.opengis.net/def/ogc-api/records/mediaType
    x-jsonld-container: '@set'
    x-jsonld-type: '@id'
  contacts:
    x-jsonld-container: '@set'
    x-jsonld-id: http://www.w3.org/ns/dcat#contactPoint
    x-jsonld-type: '@id'
  license: http://www.w3.org/ns/dcat#license
  accessrights: http://purl.org/dc/terms/accessRights
  variables:
    x-jsonld-container: '@id'
    x-jsonld-id: https://www.opengis.net/def/ogc-api/records/hasVariable
    x-jsonld-context:
      '@base': http://example.com/variables/
      '@vocab': https://www.opengis.net/def/ogc-api/records/
  rights: http://www.w3.org/ns/dcat#rights
x-jsonld-prefixes:
  geojson: https://purl.org/geojson/vocab#
  rdfs: http://www.w3.org/2000/01/rdf-schema#
  dct: http://purl.org/dc/terms/
  dcat: http://www.w3.org/ns/dcat#
  rec: https://www.opengis.net/def/ogc-api/records/
  xsd: http://www.w3.org/2001/XMLSchema#
  skos: http://www.w3.org/2004/02/skos/core#
  thns: https://w3id.org/ogc/stac/themes/
  oa: http://www.w3.org/ns/oa#
  owl: http://www.w3.org/2002/07/owl#
  rdf: http://www.w3.org/1999/02/22-rdf-syntax-ns#
  w3ctime: http://www.w3.org/2006/time#
  dctype: http://purl.org/dc/dcmitype/
  vcard: http://www.w3.org/2006/vcard/ns#
  prov: http://www.w3.org/ns/prov#
  foaf: http://xmlns.com/foaf/0.1/

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum.github.io/bblock-dcat-ap-nl/build/annotated/bbr/dcat/dcat-dataservice-records/schema.json)
* JSON version: [schema.json](https://geonovum.github.io/bblock-dcat-ap-nl/build/annotated/bbr/dcat/dcat-dataservice-records/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "Feature": "geojson:Feature",
    "FeatureCollection": "geojson:FeatureCollection",
    "GeometryCollection": "geojson:GeometryCollection",
    "LineString": "geojson:LineString",
    "MultiLineString": "geojson:MultiLineString",
    "MultiPoint": "geojson:MultiPoint",
    "MultiPolygon": "geojson:MultiPolygon",
    "Point": "geojson:Point",
    "Polygon": "geojson:Polygon",
    "features": {
      "@container": "@set",
      "@id": "geojson:features"
    },
    "type": "@type",
    "id": "@id",
    "properties": "@nest",
    "geometry": {
      "@context": {
        "coordinates": {
          "@container": "@list",
          "@id": "geojson:coordinates"
        }
      },
      "@id": "geojson:geometry"
    },
    "bbox": {
      "@container": "@list",
      "@id": "geojson:bbox"
    },
    "links": {
      "@context": {
        "rel": {
          "@context": {
            "@base": "http://www.iana.org/assignments/relation/"
          },
          "@id": "http://www.iana.org/assignments/relation",
          "@type": "@id"
        },
        "hreflang": "dct:language",
        "length": "dct:extent",
        "distribution": {
          "@context": {
            "mediaType": "rec:mediaType",
            "name": "rec:name",
            "description": "rec:description",
            "license": "rec:license",
            "accessRights": "rec:accessRights"
          },
          "@id": "dcat:distribution",
          "@type": "@id"
        }
      },
      "@id": "rdfs:seeAlso"
    },
    "conformsTo": {
      "@container": "@set",
      "@id": "dct:conformsTo",
      "@type": "@id"
    },
    "time": "dct:temporal",
    "linkTemplates": {
      "@context": {
        "rel": {
          "@context": {
            "@base": "http://www.iana.org/assignments/relation/"
          },
          "@id": "http://www.iana.org/assignments/relation",
          "@type": "@id"
        },
        "type": "dct:format",
        "hreflang": "dct:language",
        "title": "rdfs:label",
        "length": "dct:extent",
        "uriTemplate": {
          "@type": "xsd:string",
          "@id": "rec:uriTemplate"
        },
        "varBase": "rec:varBase",
        "variables": {
          "@id": "rec:hasVariable",
          "@container": "@index",
          "@index": "dct:identifier"
        }
      },
      "@id": "rec:hasLinkTemplate"
    },
    "created": "dct:created",
    "updated": "dct:modified",
    "title": {
      "@container": "@set",
      "@id": "dct:title"
    },
    "description": {
      "@container": "@set",
      "@id": "dct:description"
    },
    "keywords": {
      "@container": "@set",
      "@id": "dcat:keyword"
    },
    "language": {
      "@id": "rec:language",
      "@context": {
        "code": "rec:languageCode",
        "name": "skos:prefLabel"
      }
    },
    "languages": {
      "@container": "@set",
      "@id": "rec:languages",
      "@context": {
        "code": "rec:languageCode",
        "name": "skos:prefLabel"
      }
    },
    "resourceLanguages": {
      "@container": "@set",
      "@id": "rec:resourceLanguages",
      "@context": {
        "code": "rec:languageCode",
        "name": "skos:prefLabel"
      }
    },
    "externalIds": {
      "@container": "@set",
      "@id": "rec:scopedIdentifier",
      "@context": {
        "scheme": "rec:scheme",
        "value": "rec:id"
      }
    },
    "themes": {
      "@container": "@set",
      "@id": "rec:themes",
      "@context": {
        "concepts": {
          "@id": "thns:concepts",
          "@context": {
            "id": {
              "@type": "xsd:string",
              "@id": "thns:id"
            },
            "url": {
              "@type": "@id",
              "@id": "@id"
            }
          },
          "@container": "@set"
        },
        "scheme": "thns:scheme"
      }
    },
    "formats": {
      "@id": "rec:format",
      "@context": {
        "name": "rec:name",
        "mediaType": "rec:mediaType"
      },
      "@container": "@set",
      "@type": "@id"
    },
    "contacts": {
      "@container": "@set",
      "@id": "dcat:contactPoint",
      "@type": "@id"
    },
    "license": "dcat:license",
    "accessrights": "dct:accessRights",
    "variables": {
      "@container": "@id",
      "@id": "rec:hasVariable",
      "@context": {
        "@base": "http://example.com/variables/",
        "@vocab": "https://www.opengis.net/def/ogc-api/records/"
      }
    },
    "rights": "dcat:rights",
    "href": {
      "@type": "@id",
      "@id": "oa:hasTarget"
    },
    "geojson": "https://purl.org/geojson/vocab#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "oa": "http://www.w3.org/ns/oa#",
    "dct": "http://purl.org/dc/terms/",
    "dcat": "http://www.w3.org/ns/dcat#",
    "rec": "https://www.opengis.net/def/ogc-api/records/",
    "skos": "http://www.w3.org/2004/02/skos/core#",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "owl": "http://www.w3.org/2002/07/owl#",
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "w3ctime": "http://www.w3.org/2006/time#",
    "dctype": "http://purl.org/dc/dcmitype/",
    "vcard": "http://www.w3.org/2006/vcard/ns#",
    "prov": "http://www.w3.org/ns/prov#",
    "foaf": "http://xmlns.com/foaf/0.1/",
    "thns": "https://w3id.org/ogc/stac/themes/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://geonovum.github.io/bblock-dcat-ap-nl/build/annotated/bbr/dcat/dcat-dataservice-records/context.jsonld)

## Sources

* [DCAT v3 Specification](https://www.w3.org/TR/vocab-dcat-3/)
* [API Records Specification Repository](https://github.com/opengeospatial/ogcapi-records)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum/bblock-dcat-ap-nl](https://github.com/Geonovum/bblock-dcat-ap-nl)
* Path: `_sources/dcat-dataservice-records`

