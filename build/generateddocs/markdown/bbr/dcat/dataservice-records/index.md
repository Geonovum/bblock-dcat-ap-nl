
# DCAT-AP-NL profile 3.0 - Dataservice/Records binding (Model)

`geonovum.bbr.dcat.dataservice-records` *v0.1*

DCAT-AP-NL 3.0 Dataservice profile bound to OGC API Records

[*Status*](http://www.opengis.net/def/status): Under development

## Examples

### DCAT-AP-NL 3.0 Dataservice example showing binding to OGC API record schema.
This example is to test records examples.

This snippet was retrieved from [https://raw.githubusercontent.com/opengeospatial/ogcapi-records/master/core/examples/json/record.json](https://raw.githubusercontent.com/opengeospatial/ogcapi-records/master/core/examples/json/record.json).
#### ttl
```ttl
@prefix exBB: <http://example/buildingblock> .
@prefix adms: <http://www.w3.org/ns/adms#>.
@prefix dcat: <http://www.w3.org/ns/dcat#>.
@prefix dcatap: <http://data.europa.eu/r5r/>.
@prefix dct: <http://purl.org/dc/terms/>.
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
@prefix vcard: <http://www.w3.org/2006/vcard/ns#> .
@prefix skos: <http://www.w3.org/2004/02/skos/core#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix rec: <https://www.opengis.net/def/ogc-api/records/> .
@prefix ns1: <http://www.iana.org/assignments/> .
@prefix oa: <http://www.w3.org/ns/oa#> .

exBB:2482250f-3b00-4439-9f93-f3118229b201_DS_d0e1068 a dcat:DataService ;
    dct:title "BRT TOP10NL OGC API Features"@nl ;
    dcat:endpointDescription <https://api.pdok.nl/brt/top10nl/ogc/v1> ;
    dcat:endpointURL <https://api.pdok.nl/brt/top10nl/ogc/v1/api> ;
    dct:accessRights <http://inspire.ec.europa.eu/metadata-codelist/ConditionsApplyingToAccessAndUse/noConditionsApply>,
        <http://inspire.ec.europa.eu/metadata-codelist/LimitationsOnPublicAccess/noLimitations> ;
    dcat:contactPoint [ a vcard:Individual ;
            vcard:fn "Klantcontactcenter"@nl ;
            vcard:hasAddress [ a vcard:Address ;
                    vcard:country-name "Nederland" ;
                    vcard:locality "Apeldoorn" ;
                    vcard:postal-code "7300 GH" ;
                    vcard:region "Gelderland" ;
                    vcard:street-address "Postbus 9046" ] ;
            vcard:hasEmail <mailto:kcc@kadaster.nl> ;
            vcard:hasTelephone <tel:+31088-1832200> ;
            vcard:hasURL <https://www.kadaster.nl> ;
            vcard:organization-name "Kadaster"@nl ] ;
    dct:description "TOP10NL is een digitaal objectgericht topografisch bestand wat ten grondslag ligt aan de topografische kaartseries 1:10.000 en 1:25.000 en wat veelvuldig in diverse GIS- en CAD-systemen wordt gebruikt voor ondergrond, analyse-, en beheers- en planningsactiviteiten. Heeft u een vermoedelijke fout in TOP10NL geconstateerd? Doe dan een melding op https://www.verbeterdekaart.nl of via de Terugmelding REST API: https://www.pdok.nl/restful-api/-/article/brt-terugmeldingen ."@nl ;
    dct:identifier ""^^xsd:string ;
    dct:license  <http://creativecommons.org/licenses/by/4.0/deed.nl> ;
    dct:publisher [
            dct:type <http://purl.org/adms/publishertype/LocalAuthority> ;
            a foaf:Agent ;
            foaf:name "Kadaster"@nl;
        ] ;    
    dcat:theme [ a skos:Concept ;
            dct:source <http://inspire.ec.europa.eu/metadata-codelist/SpatialScope/national> ;
            skos:prefLabel "Nationaal"@nl ],
        [ a skos:Concept ;
            dct:source <http://www.eionet.europa.eu/gemet/nl/inspire-theme/hy> ;
            skos:prefLabel "Hydrografie"@nl ],
        [ a skos:Concept ;
            dct:source <http://data.europa.eu/bna/c_dd313021> ;
            skos:prefLabel "Aardobservatie en milieu"@nl ],
        [ a skos:Concept ;
            dct:source <http://www.eionet.europa.eu/gemet/nl/inspire-theme/sr> ;
            skos:prefLabel "Zeegebieden"@nl ],
        [ a skos:Concept ;
            dct:source <http://www.eionet.europa.eu/gemet/nl/inspire-theme/gn> ;
            skos:prefLabel "Geografische namen"@nl ],
        [ a skos:Concept ;
            dct:source <http://data.europa.eu/bna/c_b79e35eb> ;
            skos:prefLabel "Mobiliteit"@nl ],
        [ a skos:Concept ;
            dct:source <http://data.europa.eu/eli/reg_impl/2023/138/oj> ;
            skos:prefLabel "HVD"@nl ],
        [ a skos:Concept ;
            dct:source <http://www.eionet.europa.eu/gemet/nl/inspire-theme/lc> ;
            skos:prefLabel "Bodemgebruik"@nl ],
        [ a skos:Concept ;
            dct:source <http://www.eionet.europa.eu/gemet/nl/inspire-theme/tn> ;
            skos:prefLabel "Vervoersnetwerken"@nl ],
        [ a skos:Concept ;
            dct:source <http://data.europa.eu/bna/c_ac64a52d> ;
            skos:prefLabel "Geospatiale data"@nl ] ;        

    rec:format <http://example.com/records/OAPIF> ;
    rec:hasLinkTemplate [ a <http://example.com/records/image/png> ;
            rdfs:label "BRT TOP10NL OGC API Features" ;
            ns1:relation <http://www.iana.org/assignments/relation/describes> ;
            oa:hasTarget "https://api.pdok.nl/brt/top10nl/ogc/v1/api"^^xsd:string ;
            ] ;
                .


```


### DCAT-AP-NL 3.0 Dataservice example showing binding to OGC API record schema.
This example is to test records examples.
#### json
```json
{
  "@context": [
    "https://schema.org/",
    "http://purl.org/dc/terms/",
    "http://www.w3.org/ns/dcat#",
    "http://xmlns.com/foaf/0.1/",
    "http://www.opengis.net/def/dcat-ap/sjp/" 
     ],
  "id": "https://data.overheid.nl/catalogus/record/pdok-top10nl-ogc-api-features-service-record",
  "conformsTo": [
      "http://www.opengis.net/spec/ogcapi-features-1/1.0/conf/core",
      "http://www.opengis.net/spec/ogcapi-features-1/1.0/conf/oas30",
      "http://www.opengis.net/spec/ogcapi-features-1/1.0/conf/geojson"
    ],
  "type": "dcat:CatalogRecord",
    "properties": {

  "dct:identifier": "pdok-top10nl-ogc-api-features-service-record",
  "dct:issued": "2024-01-15T10:00:00Z", 
  "dct:modified": "2025-06-06T17:36:43Z", 
  "dct:language": "nl",
  "dct:creator": { 
    "@type": "schema:Organization",
    "schema:name": "Nationaal Georegister (PDOK)",
    "schema:url": "https://www.pdok.nl/"
  },
  "dcat:theme": [ 
    "http://publications.europa.eu/resource/authority/data-theme/GEOS" 
  ],
  "dcat:keyword": [ 
    "OGC API", "Features", "Geospatial API", "Data Service", "Catalog"
  ],
  "dcat:primaryTopic": {
    "@id": "https://api.pdok.nl/brt/top10nl/ogc/v1",
    "@type": [
      "dcat:DataService",
      "schema:Service"
    ],
    "dct:title": "OGC API Features - TOP10NL Service",
    "dct:description": "This OGC API Features service provides programmatic access to the TOP10NL dataset, offering detailed topographic information of the Netherlands (buildings, roads, water bodies, land use). It allows for querying, filtering, and retrieving geographic features following OGC API standards.",
    "dct:publisher": {
      "@type": "schema:Organization",
      "@id": "https://www.kadaster.nl/",
      "schema:name": "Kadaster",
      "schema:url": "https://www.kadaster.nl/"
    },
    
    "dcat:endpointURL": "https://api.pdok.nl/brt/top10nl/ogc/v1",
    "dcat:endpointDescription": {
      "@id": "https://api.pdok.nl/brt/top10nl/ogc/v1/api",
      "@type": "dcat:Distribution",
      "dct:title": "OpenAPI documentation for TOP10NL OGC API Features",
      "dct:format": "http://publications.europa.eu/resource/authority/file-type/JSON",
      "dcat:mediaType": "application/vnd.oai.openapi+json;version=3.0"
    },
    "schema:serviceType": "OGC API Features",
    "schema:url": "https://api.pdok.nl/brt/top10nl/ogc/v1",
    "foaf:page": "https://www.pdok.nl/downloads/-/top10nl-ogc-api-features", 
    "dcat:theme": [ 
      "http://publications.europa.eu/resource/authority/data-theme/GEOS", 
      "http://inspire.ec.europa.eu/theme/tn" 
    ],
    "dcat:keyword": [ 
      "OGC API Features", "TOP10NL", "BGT", "Basisregistratie Topografie", "PDOK", "Kadaster", "Geodata", "API", "Features API", "Web Service"
    ],
    "dct:license": "https://creativecommons.org/publicdomain/zero/1.0/", 
    "dct:accessRights": "http://publications.europa.eu/resource/authority/access-right/PUBLIC", 
    "dcat:servesDataset": {
      "@id": "https://data.overheid.nl/dataset/top10nl", 
      "type": "dcat:Dataset",
      "dct:identifier": "top10nl-dataset-identifier",
      "dct:title": "TOP10NL Dataset",
      "dct:description": "The authoritative topographic dataset of the Netherlands at scale 1:10,000, as maintained by Kadaster. It provides detailed base maps for various applications.",
      "dct:language": "nl",
      "dcat:spatialResolutionInMeters": 10,
      "dcat:spatial": {
        "@type": "dct:Location",
        "dcat:bbox": "3.3768,50.7504,7.2272,53.5885", 
        "rdfs:label": "Netherlands"
      },
      "dcat:keyword": [
        "topografie", "basisregistratie", "kaart", "Nederland", "gebouwen", "wegen", "water", "terreindekking", "topographic map"
      ],
      "dct:temporal": { 
        "@type": "dct:PeriodOfTime",
        "dcat:startDate": "2009-01-01",
        "dcat:endDate": "2025-12-31" 
      },
      "dct:accrualPeriodicity": "http://publications.europa.eu/resource/authority/frequency/CONT", 
      "dct:license": "https://creativecommons.org/publicdomain/zero/1.0/", 
      "dct:accessRights": "http://publications.europa.eu/resource/authority/access-right/PUBLIC",
      "dct:publisher": { 
        "@type": "schema:Organization",
        "@id": "https://www.kadaster.nl/",
        "schema:name": "Kadaster",
        "schema:url": "https://www.kadaster.nl/"
      },
      "dcat:theme": [ 
        "http://publications.europa.eu/resource/authority/data-theme/GEOS",
        "http://inspire.ec.europa.eu/theme/tn"
      ]
    }
  }
}
}
```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Schema for OGCAPI records profile for DCAT Dataservoce - defines all
  extra elements defined by CAT so that the JSON-LD context can map to DCAT RDF
allOf:
- $ref: https://ogcincubator.github.io/geodcat-ogcapi-records/build/annotated/geo/geodcat/dcat-records/schema.yaml

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum.github.io/bblock-dcat-ap-nl/build/annotated/bbr/dcat/dataservice-records/schema.json)
* JSON version: [schema.json](https://geonovum.github.io/bblock-dcat-ap-nl/build/annotated/bbr/dcat/dataservice-records/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "type": "@type",
    "coordinates": {
      "@container": "@list",
      "@id": "geojson:coordinates"
    },
    "bbox": {
      "@container": "@list",
      "@id": "geojson:bbox"
    },
    "href": {
      "@type": "@id",
      "@id": "oa:hasTarget"
    },
    "rel": {
      "@context": {
        "@base": "http://www.iana.org/assignments/relation/"
      },
      "@id": "http://www.iana.org/assignments/relation",
      "@type": "@id"
    },
    "hreflang": "dct:language",
    "title": "rdfs:label",
    "length": "dct:extent",
    "created": "dct:created",
    "updated": "dct:modified",
    "uriTemplate": {
      "@type": "xsd:string",
      "@id": "oa:hasTarget"
    },
    "id": "@id",
    "properties": "@nest",
    "geometry": "geojson:geometry",
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
    "links": {
      "@context": {
        "type": "dct:type"
      },
      "@id": "rdfs:seeAlso"
    },
    "time": {
      "@id": "dct:temporal",
      "@context": {
        "interval": {
          "@id": "w3ctime:hasTime",
          "@container": "@list"
        },
        "resolution": "rec:iso8601period"
      }
    },
    "description": {
      "@container": "@set",
      "@id": "dct:description"
    },
    "keywords": {
      "@container": "@set",
      "@id": "dcat:keyword"
    },
    "conformsTo": {
      "@container": "@set",
      "@id": "dct:conformsTo",
      "@type": "@id"
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
          "@id": "rec:concept",
          "@context": {
            "id": {
              "@type": "xsd:string",
              "@id": "rec:conceptID"
            },
            "url": {
              "@type": "@id",
              "@id": "dct:theme"
            }
          }
        },
        "scheme": "rec:scheme"
      }
    },
    "formats": {
      "@container": "@set",
      "@id": "rec:format",
      "@type": "@id"
    },
    "contacts": {
      "@container": "@set",
      "@id": "dcat:contactPoint",
      "@type": "@id"
    },
    "license": "dcat:license",
    "rights": "dcat:rights",
    "linkTemplates": "rec:hasLinkTemplate",
    "variables": {
      "@container": "@id",
      "@id": "rec:hasVariable",
      "@context": {
        "@base": "http://example.com/variables/",
        "@vocab": "https://www.opengis.net/def/ogc-api/records/"
      }
    },
    "geojson": "https://purl.org/geojson/vocab#",
    "oa": "http://www.w3.org/ns/oa#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "dct": "http://purl.org/dc/terms/",
    "xsd": "http://www.w3.org/2001/XMLSchema#",
    "w3ctime": "http://www.w3.org/2006/time#",
    "rec": "https://www.opengis.net/def/ogc-api/records/",
    "dcat": "http://www.w3.org/ns/dcat#",
    "skos": "http://www.w3.org/2004/02/skos/core#",
    "owl": "http://www.w3.org/2002/07/owl#",
    "rdf": "http://www.w3.org/1999/02/22-rdf-syntax-ns#",
    "dctype": "http://purl.org/dc/dcmitype/",
    "vcard": "http://www.w3.org/2006/vcard/ns#",
    "prov": "http://www.w3.org/ns/prov#",
    "foaf": "http://xmlns.com/foaf/0.1/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://geonovum.github.io/bblock-dcat-ap-nl/build/annotated/bbr/dcat/dataservice-records/context.jsonld)

## Sources

* [DCAT-AP-NL 3.0 Specification](https://docs.geostandaarden.nl/dcat/dcat-ap-nl30/)
* [API Records Specification Repository](https://github.com/opengeospatial/ogcapi-records)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum/bblock-dcat-ap-nl](https://github.com/Geonovum/bblock-dcat-ap-nl)
* Path: `_sources/dataservice-records`

