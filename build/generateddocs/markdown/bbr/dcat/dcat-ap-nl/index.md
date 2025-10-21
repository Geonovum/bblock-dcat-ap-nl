
# DCAT-AP-NL profile 3.0 (Model)

`geonovum.bbr.dcat.dcat-ap-nl` *v0.1*

DCAT-AP-NL 3.0 (Dutch profile of DCAT-AP)

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## DCAT-AP-NL 3.0

These building blocks provide a framework to test compatibility of the DCAT-AP-NL 3.0 profile with DCAT-AP, and to make this relationship transparent to any implementation of DCAT-AP-NL using OGC standards.


Implementation is still experimental and might change at any moment. For example the shacl validation of the DatasetSeries example is failing at the moment, which is a known thing.



## Examples

### DCAT-AP-NL example - complete
An example from the DCAT-AP-NL profile
#### ttl
```ttl
@prefix exampleMS: <https://data.exampleMS.gov/id/data/>.
@prefix dcat: <http://www.w3.org/ns/dcat#>.
@prefix dct: <http://purl.org/dc/terms/>.
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
@prefix vcard: <http://www.w3.org/2006/vcard/ns#> .
@prefix eli: <http://data.europa.eu/eli/ontology#> .
@prefix adms: <http://www.w3.org/ns/adms#>.
@prefix dcatap: <http://data.europa.eu/r5r/>.
@prefix skos: <http://www.w3.org/2004/02/skos/core#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#>.
@prefix example-ds: <https://data.gov.gr/id/dataset/> .
@prefix example-ser: <https://data.gov.gr/id/datasetseries/> .

## Imports om relevante waardes uit waardelijsten of gegevens uit externe bronnen op te nemen.
##  Dit is in principe alleen nodig voor validatie en als er gebruik gemaakt kan worden van owl:imports bij validatie.
@prefix owl: <http://www.w3.org/2002/07/owl#> .
[] owl:imports 
  <http://publications.europa.eu/resource/authority/access-right/PUBLIC> ,
  <http://data.europa.eu/eli/reg_impl/2023/138/oj> ,
  <http://data.europa.eu/eli/reg/2010/1089> ,
  <http://publications.europa.eu/resource/authority/language/NLD> ,
  <http://www.geonames.org/2750405/about.rdf> ,
  <http://publications.europa.eu/resource/authority/data-theme/EDUC> .
## End Import

## Catalog

exampleMS:Datacatalog  a dcat:Catalogue;
  dct:title "De naam van de catalog"@nl;
   dcat:contactPoint [
     a vcard:Kind ;
     vcard:fn "Mijn Organisatie"@nl ;
     vcard:fn "My Organization"@en ;
     vcard:hasEmail <mailto:opendata@mijnorganisatie.nl> ;
     vcard:hasURL "http://mijnorganisatie.org/" ;
     vcard:organization-name "Mijn Organisatie"@nl ;
     vcard:organization-name "My Organization"@en
     ] ; 
  dct:description "beschrijving van de catalog"@nl;
   dct:publisher [
     dct:type <http://purl.org/adms/publishertype/LocalAuthority> ;
     a foaf:Agent ;
     foaf:name "Mijn Organisatie"@nl;
     foaf:name "My Organization"@en
     ] ;
  dcat:dataset exampleMS:1T2p3o4B ;
  dcat:service exampleMS:1T2p3o4B-dataservice-WMS
  .

## CatalogRecord

  exampleMS:1T2p3o4B-rec a dcat:CatalogRecord;
   dct:conformsTo <https://semiceu.github.io/DCAT-AP/releases/3.0.0>;
   dct:language <http://publications.europa.eu/resource/authority/language/NLD> ;
   dct:modified "2019-02-27T15:15:08Z" ; 
   foaf:primaryTopic exampleMS:1T2p3o4B ;
   dct:source <https://www.nationaalgeoregister.nl/geonetwork/srv/dut/catalog.search#/metadata/ba83c30f-12f7-4582-a590-852b6d1706de?tab=general>
  .

## Dataset

exampleMS:1T2p3o4B a dcat:Dataset;
   dct:title "Naam van de dataset"@nl;
   dct:title "Title of the dataset"@en;
   dct:accessRights <http://publications.europa.eu/resource/authority/access-right/PUBLIC>;
   dcatap:applicableLegislation <http://data.europa.eu/eli/reg_impl/2023/138/oj>;
   dct:conformsTo <http://data.europa.eu/eli/reg/2010/1089>;
   dcat:contactPoint [
     a <https://json-ld.org/playground/Organization> ;
     vcard:fn "Mijn Organisatie"@nl ;
     vcard:fn "My Organization"@en ;
     vcard:hasEmail <mailto:opendata@mijnorganisatie.nl> ;
     vcard:hasURL "http://mijnorganisatie.org/" ;
     vcard:organization-name "Mijn Organisatie"@nl ;
     vcard:organization-name "My Organization"@en
     ] ; 
   dct:creator [
     dct:type <http://purl.org/adms/publishertype/LocalAuthority> ;
     a foaf:Agent ;
     foaf:name "Mijn Organisatie"@nl;
     foaf:name "My Organization"@en
     ] ;
   dct:description "beschrijving van de dataset"@nl;
   dct:description "description of the dataset in english"@en;
   dct:identifier "https://data.exampleMS.gov/id/dataset/1T2p3o4B";
   dcat:keyword "trefwoord 1"@nl;
   dcat:keyword "trefwoord 2"@nl;
   dcat:keyword "keyword 1"@en;
   dcat:keyword "keyword 2"@en;
   dct:language <http://publications.europa.eu/resource/authority/language/NLD> ;
   dct:publisher [
     dct:type <http://purl.org/adms/publishertype/LocalAuthority> ;
     a foaf:Agent ;
     foaf:name "Mijn Organisatie"@nl;
     foaf:name "My Organization"@en
     ] ;
   dct:spatial <https://www.geonames.org/2750405>;
   dct:spatial [a dct:Location ;
                  dcat:bbox "POLYGON ((3.053 47.975,7.24 47.975,7.24 53.504,3.053 53.504,3.053 47.975))"^^rdf:wktLiteral;
  ] ;
   dct:temporal [ a dct:PeriodOfTime ;
     dcat:startDate "2016-03-28"^^xsd:date ;
     dcat:endDate   "2018-08-25"^^xsd:date ;
     ] ;
   dcat:theme <http://publications.europa.eu/resource/authority/data-theme/EDUC>;
   dcat:distribution exampleMS:1T2p3o4B-dist-SHP;
   dcat:distribution exampleMS:1T2p3o4B-dist-WMS
   .

# Aanvullingen voor EU waardelijsten, die nog niet volledig zijn ontsloten 
# De dct:RightsStatement zit niet in de waardelijst. Dat lijkt een fout in de waardelijst.
<http://publications.europa.eu/resource/authority/access-right/PUBLIC> a dct:RightsStatement .

# De typering dct:LinguisticSystem zit niet in de waardelijst. Dat lijkt een fout in de waardelijst.
<http://publications.europa.eu/resource/authority/language/NLD> a dct:LinguisticSystem .

# Geen RDF van beschikbaar
<http://data.europa.eu/eli/reg_impl/2023/138/oj> a eli:LegalResource .

# Geen RDF van beschikbaar
<http://data.europa.eu/eli/reg/2010/1089> a dct:Standard .

# Geonames is niet gedefinieert als een dct:Location. 
<https://www.geonames.org/2750405> a dct:Location .

# Deze zou je kunnen importeren, maar dan krijg je validatiefouten op ConceptScheme shapes, omdat de adms ConceptSchemes niet voldoen aan de ConceptScheme shape van DCAT-AP.
<http://purl.org/adms/publishertype/LocalAuthority> a skos:Concept ;
 skos:prefLabel"Local Authority"@en .

# ## DatasetSeries

# example-ds:BeePopulation2022 a dcat:Dataset;
#   dcat:inSeries example-ser:BeePopulation .

# example-ds:BeePopulation2023 a dcat:Dataset;
#   dcat:inSeries example-ser:BeePopulation .

# example-ser:BeePopulation a dcat:DatasetSeries;
#   dct:title "Bee population"@en;
#   dct:description "Bee population annual serie"@en;
#   .

## Distribution

exampleMS:1T2p3o4B-dist-SHP a dcat:Distribution;
   dcat:accessURL <https://orgea.exampleMS.gov/files/1T2p3o4B.shp> ;
   dcatap:applicableLegislation <http://data.europa.eu/eli/reg_impl/2023/138/oj>;
   dcat:downloadURL <https://orgea.exampleMS.gov/files/1T2p3o4B.shp> ;
   dct:language <http://publications.europa.eu/resource/authority/language/NLD> ;
   dct:license <http://creativecommons.org/publicdomain/zero/1.0/deed.nl> ;
   dct:conformsTo <http://inspire.ec.europa.eu/schemas/hy/4.0/HydroBase.xsd> ;
   dcat:mediaType <https://www.iana.org/assignments/media-types/application/vnd.shp>
   .

<https://www.iana.org/assignments/media-types/application/vnd.shp> a dct:MediaType
.
<http://inspire.ec.europa.eu/schemas/hy/4.0/HydroBase.xsd> a dct:Standard
.
<https://orgea.exampleMS.gov/files/1T2p3o4B.shp>  a rdf:Resource
.
 <https://orgea.exampleMS.gov/files/1T2p3o4B.shp> a rdf:Resource
.
<http://creativecommons.org/publicdomain/zero/1.0/deed.nl> a dct:LicenseDocument
.

## Dataservice

exampleMS:1T2p3o4B-dataservice-WMS a dcat:DataService;
   dct:title "Naam van de dataservice"@nl;
   dct:title "Title of the dataservice"@en;
   dct:accessRights <http://publications.europa.eu/resource/authority/access-right/PUBLIC>;
   dcatap:applicableLegislation <http://data.europa.eu/eli/reg_impl/2023/138/oj>;
   dct:conformsTo <http://www.opengis.net/def/serviceType/ogc/wms>;
   dcat:contactPoint [
     a vcard:Kind;
     vcard:fn "Mijn Organisatie"@nl ;
     vcard:fn "My Organization"@en ;
     vcard:hasEmail <mailto:opendata@mijnorganisatie.nl> ;
     vcard:hasURL "http://mijnorganisatie.org/" ;
     vcard:organization-name "Mijn Organisatie"@nl ;
     vcard:organization-name "My Organization"@en
     ] ; 
   dct:creator [
     dct:type <http://purl.org/adms/publishertype/LocalAuthority> ;
     a foaf:Agent ;
     foaf:name "Mijn Organisatie"@nl;
     foaf:name "My Organization"@en
     ] ;
   dct:description "beschrijving van de dataservice"@nl;
   dct:description "description of the dataservice in english"@en;
   foaf:page <https://orgea.exampleMS.gov/QoS.html> ;
   dcat:endpointDescription <https://orgea.exampleMS.gov/services/wms?&request=GetCapabilities&service=WMS>;
   dcat:endpointURL <https://orgea.exampleMS.gov/services/wms?> ;
   dct:identifier "https://data.exampleMS.gov/id/data/1T2p3o4B-dataservice-WMS";
   dcat:keyword "trefwoord 1"@nl;
   dcat:keyword "trefwoord 2"@nl;
   dcat:keyword "keyword 1"@en;
   dcat:keyword "keyword 2"@en;
   dct:language <http://publications.europa.eu/resource/authority/language/NLD> ;
   dct:license <http://creativecommons.org/publicdomain/zero/1.0/deed.nl> ;
   dct:publisher [
     dct:type <http://purl.org/adms/publishertype/LocalAuthority> ;
     a foaf:Agent ;
     foaf:name "Mijn Organisatie"@nl;
     foaf:name "My Organization"@en
     ] ;
   dcat:theme <http://publications.europa.eu/resource/authority/data-theme/EDUC>;
   dcat:servesDataset exampleMS:1T2p3o4B
.

<http://www.opengis.net/def/serviceType/ogc/wms> a dct:Standard
.
```


### DCAT-AP-NL with OGC API Records in JSON
An example based on the BAG metadata record from the NGR. 
Converted in JSON so the Semantic uplift via a JSON-LD context can be shown.
#### json
```json
{
  "type": "Feature",
  "conformsTo": [
    "http://www.opengis.net/spec/ogcapi-records-1/1.0/req/record-core",
    "http://modellen.geostandaarden.nl/dcat-ap-nl/"
  ],
  "id": "urn:ogc:record:generated-id",
  "geometry": null,
  "properties": {
    "rdf:type": [
      "http://www.w3.org/ns/dcat#Dataset",
      "http://www.w3.org/ns/dcat#Resource",
      "http://www.w3.org/ns/prov#Entity"
    ],
    "dcat:contactPoint": {
      "organizationName": {
        "nl": "Directie Operatie, Dienstverlening en Registratie, afdeling Data-, Proces- en Informatiemanagement"
      },
      "email": "mailto:dpi-gi@kadaster.nl"
    },
    "dcterms:accrualPeriodicity": {
      "@id": "http://publications.europa.eu/resource/authority/frequency/DAILY",
      "rdf:type": "http://purl.org/dc/terms/Frequency"
    },
    "dcterms:accessRights": {
      "@id": "http://inspire.ec.europa.eu/metadata-codelist/ConditionsApplyingToAccessAndUse/noConditionsApply",
      "rdf:type": [
        "http://purl.org/dc/terms/LicenseDocument",
        "http://purl.org/dc/terms/RightsStatement"
      ]
    },
    "dcterms:conformsTo": {
      "rdf:type": "http://purl.org/dc/terms/Standard",
      "dcterms:issued": "2010-12-08",
      "dcterms:title": {
        "nl": "VERORDENING (EU) Nr. 1089/2010 VAN DE COMMISSIE van 23 november 2010 ter uitvoering van Richtlijn 2007/2/EG van het Europees Parlement en de Raad betreffende de interoperabiliteit van verzamelingen ruimtelijke gegevens en van diensten met betrekking tot ruimtelijke gegevens"
      }
    },
    "dcterms:created": "2013-02-18",
    "dcterms:description": {
      "nl": "De gegevens bestaan uit BAG-panden en een deelselectie van BAG-gegevens van deze panden en de zich daarin bevindende verblijfsobjecten. Ook de ligplaatsen en standplaatsen zijn hierin opgenomen met een deelselectie van BAG-gegevens. De gegevens van de nummeraanduiding zijn in deze services onderdeel van de adresseerbare objecten, hierbij wordt slechts 1 adres opgenomen, dus objecten met meerdere adressen (hoofd- en nevenadressen) zijn niet compleet. In deze services zitten dus niet alle BAG adressen. Aangezien niet alle BAG gegevens worden geleverd, adviseren wij u om de actuele gegevens in één van de BAG producten te controleren. Raadpleeg de BAG Viewer voor enkele bevragingen van BAG gegevens. Een overzicht van alle beschikbare producten kunt u vinden op de website https://www.kadaster.nl/zakelijk/registraties/basisregistraties/bag . De BAG WMS, BAG WFS en BAG API Individuele bevragingen zijn expliciet niet bedoeld voor bulkbevragingen waarmee veel gegevens in één keer worden opgevraagd en in een database worden verwerkt. Wilt u in één keer meer gegevens opvragen, dan raden wij u aan om gebruik te maken van onze BAG Geopackage (https://www.kadaster.nl/zakelijk/producten/adressen-en-gebouwen/bag-geopackage) of BAG extract (https://www.kadaster.nl/zakelijk/producten/adressen-en-gebouwen/bag-2.0-extract). De BAG Geopackage en de BAG extract kunt u downloaden via de Atom downloadservice: https://service.pdok.nl/lv/bag/atom/bag.xml . Deze dataset wordt ook gebruikt voor het ontsluiten van het INSPIRE thema Gebouwen. Het betreft gebouwcontouren, constructieve onderdelen van gebouwen en ruimtelijke barrieres. Dit betreft niet-geharmoniseerde data uit de basisregistratie Adressen en Gebouwen (BAG). De service wordt dagelijks geactualiseerd."
    },
    "dcterms:identifier": "1fa33d90-79cb-11e2-b92a-0800200c9a66",
    "dcterms:language": {
      "@id": "http://publications.europa.eu/resource/authority/language/DUT",
      "rdf:type": "http://purl.org/dc/terms/LinguisticSystem"
    },
    "dcterms:provenance": {
      "rdf:type": "http://purl.org/dc/terms/ProvenanceStatement",
      "dcterms:description": {
        "nl": "Ontwikkeld uit de Basisregistratie Adressen en Gebouwen (BAG)"
      }
    },
    "dcterms:spatial": [
      {
        "rdf:type": "http://purl.org/dc/terms/Location",
        "skos:prefLabel": {
          "nl": "Nederland"
        }
      },
      {
        "rdf:type": "http://purl.org/dc/terms/Location",
        "dcat:bbox": {
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
        }
      }
    ],
    "dcterms:temporal": {
      "dcat:startDate": "1996-01-01",
      "dcat:endDate": "2025-12-31"
    },
    "dcterms:title": {
      "nl": "Basisregistratie Adressen en gebouwen (BAG)"
    },
    "dcterms:publisher": {
      "name": {
        "nl": "Klantcontactcenter"
      },
      "email": "mailto:bag@kadaster.nl"
    },
    "dcterms:creator": {
      "name": {
        "nl": "Kadaster"
      },
      "email": null
    },
    "distributions": [
      {
        "type": "dcat:Distribution",
        "dcterms:title": {
          "nl": "BAG (WMS)"
        },
        "dcterms:description": {
          "nl": "accessPoint"
        },
        "dcat:accessURL": "https://service.pdok.nl/lv/bag/wms/v2_0?request=getCapabilities&service=WMS",
        "dcat:mediaType": null,
        "dcterms:format": null,
        "dcterms:license": {
          "@id": "http://creativecommons.org/publicdomain/mark/1.0/deed.nl",
          "rdf:type": [
            "http://purl.org/dc/terms/LicenseDocument",
            "http://purl.org/dc/terms/RightsStatement"
          ]
        },
        "dcat:accessService": {
          "@id": "http://kadaster/1fa33d90-79cb-11e2-b92a-0800200c9a66/DS/d0e1000",
          "rdf:type": "http://www.w3.org/ns/dcat#DataService",
          "dcterms:description": {
            "nl": "accessPoint"
          },
          "dcterms:license": "http://creativecommons.org/publicdomain/mark/1.0/deed.nl",
          "dcat:theme": [
            {
              "rdf:type": "http://www.w3.org/2004/02/skos/core#Concept",
              "dcterms:source": "https://op.europa.eu/web/eu-vocabularies/concept/-/resource?uri=http://data.europa.eu/bna/c_dd313021",
              "skos:prefLabel": {
                "nl": "Geodata"
              }
            },
            {
              "rdf:type": "http://www.w3.org/2004/02/skos/core#Concept",
              "dcterms:source": "http://www.eionet.europa.eu/gemet/nl/inspire-theme/ad",
              "skos:prefLabel": {
                "nl": "Adressen"
              }
            },
            {
              "rdf:type": "http://www.w3.org/2004/02/skos/core#Concept",
              "dcterms:source": "http://www.eionet.europa.eu/gemet/nl/inspire-theme/bu",
              "skos:prefLabel": {
                "nl": "Gebouwen"
              }
            },
            {
              "rdf:type": "http://www.w3.org/2004/02/skos/core#Concept",
              "dcterms:source": "http://inspire.ec.europa.eu/metadata-codelist/SpatialScope/national",
              "skos:prefLabel": {
                "nl": "Nationaal"
              }
            }
          ],
          "dcterms:accessRights": "http://inspire.ec.europa.eu/metadata-codelist/ConditionsApplyingToAccessAndUse/noConditionsApply",
          "dcat:contactPoint": {
            "rdf:type": [
              "http://www.w3.org/2006/vcard/ns#Individual",
              "http://www.w3.org/2006/vcard/ns#Kind"
            ],
            "vcard:fn": {
              "nl": "Directie Operatie, Dienstverlening en Registratie, afdeling Data-, Proces- en Informatiemanagement"
            },
            "vcard:hasAddress": {
              "rdf:type": "http://www.w3.org/2006/vcard/ns#Address",
              "vcard:country-name": "Nederland",
              "vcard:locality": "Apeldoorn",
              "vcard:postal-code": "7311 KZ",
              "vcard:region": "Gelderland",
              "vcard:street-address": "Hofstraat 110"
            },
            "vcard:hasEmail": "mailto:dpi-gi@kadaster.nl",
            "vcard:hasURL": "https://www.kadaster.nl",
            "vcard:organization-name": {
              "nl": "Kadaster"
            }
          },
          "dcterms:publisher": {
            "dcterms:type": "http://purl.org/adms/publishertype/LocalAuthority",
            "rdf:type": "http://xmlns.com/foaf/0.1/Agent",
            "foaf:name": {
              "nl": "Kadaster"
            }
          },
          "dcterms:identifier": "http://kadaster/1fa33d90-79cb-11e2-b92a-0800200c9a66/DS/d0e1000",
          "dcterms:title": {
            "nl": "BAG (WMS)"
          },
          "dcat:endpointDescription": "https://service.pdok.nl/lv/bag/wms/v2_0?request=getCapabilities&service=WMS",
          "dcat:endpointURL": "https://service.pdok.nl/lv/bag/wms/v2_0"
        },
        "dcterms:conformsTo": null,
        "odrl:hasPolicy": null
      },
      {
        "type": "dcat:Distribution",
        "dcterms:title": {
          "nl": "BAG download Geopackage"
        },
        "dcterms:description": {
          "nl": "accessPoint"
        },
        "dcat:accessURL": "https://service.pdok.nl/lv/bag/atom/bag.xml",
        "dcat:mediaType": null,
        "dcterms:format": null,
        "dcterms:license": "http://creativecommons.org/publicdomain/mark/1.0/deed.nl",
        "dcat:accessService": null,
        "dcterms:conformsTo": null,
        "odrl:hasPolicy": null
      }
    ],
    "keywords": [
      {
        "nl": "gebouw",
        "en": "building"
      },
      {
        "nl": "ligplaats"
      },
      {
        "nl": "nummeraanduiding"
      },
      {
        "nl": "pand"
      },
      {
        "nl": "standplaats"
      },
      {
        "nl": "verblijfsobject"
      },
      {
        "nl": "woonplaats"
      }
    ],
    "dcat:landingPage": [
      {
        "@id": "https://api.bag.kadaster.nl/lvbag/individuelebevragingen/v2/",
        "rdf:type": "http://xmlns.com/foaf/0.1/Document",
        "dcterms:description": {
          "nl": "accessPoint"
        },
        "dcterms:title": {
          "nl": "BAG API Individuele Bevragingen"
        }
      },
      {
        "@id": "https://labs.kadaster.nl/cases/bag-ld",
        "rdf:type": "http://xmlns.com/foaf/0.1/Document",
        "dcterms:description": {
          "nl": "accessPoint"
        },
        "dcterms:title": {
          "nl": "Linked open data BAG"
        }
      }
    ],
    "themes": [
      {
        "skos:prefLabel": {
          "nl": "HVD"
        }
      },
      {
        "skos:prefLabel": {
          "nl": "Geodata"
        }
      },
      {
        "skos:prefLabel": {
          "nl": "Adressen"
        }
      },
      {
        "skos:prefLabel": {
          "nl": "Gebouwen",
          "en": "Buildings"
        }
      },
      {
        "skos:prefLabel": {
          "nl": "Nationaal"
        }
      }
    ],
    "dqv:hasQualityMeasurement": {
      "rdf:type": "http://www.w3.org/ns/dqv#QualityMeasurement",
      "dqv:isMeasurementOf": {
        "@id": "http://data.europa.eu/930/spatialResolutionAsScale",
        "rdf:type": "http://www.w3.org/ns/dqv#Metric"
      },
      "dqv:value": 0.001
    },
    "foaf:isPrimaryTopicOf": {
      "rdf:type": "http://www.w3.org/ns/dcat#CatalogRecord",
      "dcterms:identifier": "aa3b5e6e-7baa-40c0-8972-3353e927ec2f",
      "dcterms:language": "http://publications.europa.eu/resource/authority/language/DUT",
      "dcterms:modified": "2024-08-26",
      "dcat:contactPoint": {
        "rdf:type": "http://www.w3.org/2006/vcard/ns#Individual",
        "vcard:fn": {
          "nl": "Directie Operatie, Dienstverlening en Registratie, afdeling Data-, Proces- en Informatiemanagement"
        },
        "vcard:hasAddress": {
          "rdf:type": "http://www.w3.org/2006/vcard/ns#Address",
          "vcard:country-name": "Nederland",
          "vcard:locality": "Apeldoorn",
          "vcard:postal-code": "7311 KZ",
          "vcard:region": "Gelderland",
          "vcard:street-address": "Hofstraat 110"
        },
        "vcard:hasEmail": "mailto:dpi-gi@kadaster.nl",
        "vcard:hasURL": "https://www.kadaster.nl",
        "vcard:organization-name": {
          "nl": "Kadaster"
        }
      },
      "foaf:primaryTopic": "http://kadaster/1fa33d90-79cb-11e2-b92a-0800200c9a66"
    }
  },
  "links": [
    {
      "rel": "access",
      "href": "https://service.pdok.nl/lv/bag/wms/v2_0?request=getCapabilities&service=WMS",
      "type": null
    },
    {
      "rel": "access",
      "href": "https://service.pdok.nl/lv/bag/atom/bag.xml",
      "type": null
    }
  ]
}
```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
$defs:
  Dataset:
    description: ''
    type: object
    title: ''
    required:
    - id
    - description
    - title
    properties:
      contactPoint:
        description: Contact information that can be used for sending comments about
          the Dataset.
        title: contact point
      hasVersion:
        description: A related Dataset that is a version, edition, or adaptation of
          the described Dataset.
        title: has version
      description:
        description: A free-text account of the Dataset.
        title: description
      language:
        description: A language of the Dataset.
        title: language
      source:
        description: A related Dataset from which the described Dataset is derived.
        title: source
      title:
        type: string
        description: A name given to the Dataset.
        title: title
      type:
        description: A type of the Dataset.
        title: type
      distribution:
        description: An available Distribution for the Dataset.
        title: dataset distribution
      relation:
        description: A related resource.
        title: related resource
      isReferencedBy:
        description: A related resource, such as a publication, that references, cites,
          or otherwise points to the dataset.
        title: is referenced by
      wasGeneratedBy:
        description: An activity that generated, or provides the business context
          for, the creation of the dataset.
        title: was generated by
      provenance:
        description: A statement about the lineage of a Dataset.
        title: provenance
      inSeries:
        description: A dataset series of which the dataset is part.
        title: in series
      temporalResolution:
        format: duration
        description: The minimum time period resolvable in the dataset.
        type: string
        title: temporal resolution
      spatialResolutionInMeters:
        description: The minimum spatial separation resolvable in a dataset, measured
          in meters.
        type: string
        title: spatial resolution
      qualifiedRelation:
        description: A description of a relationship with another resource.
        title: qualified relation
      modified:
        description: The most recent date on which the Dataset was changed or modified.
        title: modification date
      theme:
        description: A category of the Dataset.
        title: theme
      id:
        format: iri-reference
        type: string
      issued:
        description: The date of formal issuance (e.g., publication) of the Dataset.
        title: release date
      spatial:
        description: A geographic region that is covered by the Dataset.
        title: geographical coverage
      keyword:
        description: A keyword or tag describing the Dataset.
        title: keyword
      temporal:
        description: A temporal period that the Dataset covers.
        title: temporal coverage
      identifier:
        description: A secondary identifier of the Dataset
        title: other identifier
      creator:
        description: An entity responsible for producing the dataset.
        title: creator
      landingPage:
        description: A web page that provides access to the Dataset, its Distributions
          and/or additional information.
        title: landing page
      version:
        description: The version indicator (name or identifier) of a resource.
        title: version
      sample:
        description: A sample distribution of the dataset.
        title: sample
      publisher:
        description: An entity (organisation) responsible for making the Dataset available.
        title: publisher
      accrualPeriodicity:
        description: The frequency at which the Dataset is updated.
        title: frequency
      accessRights:
        description: Information that indicates whether the Dataset is publicly accessible,
          has access restrictions or is not public.
        title: access rights
      conformsTo:
        description: An implementing rule or other specification.
        title: conforms to
      page:
        description: A page or document about this Dataset.
        title: documentation
      versionNotes:
        description: A description of the differences between this version and a previous
          version of the Dataset.
        title: version notes
      qualifiedAttribution:
        description: An Agent having some form of responsibility for the resource.
        title: qualified attribution
      applicableLegislation:
        description: The legislation that mandates the creation or management of the
          Dataset.
        title: applicable legislation
  '@context':
    format: iri-reference
    $comment: The URL of the JSON-LD @context
    type: string
properties:
  data:
    minItems: 1
    type: array
    items:
      $ref: '#/$defs/Dataset'
  '@context':
    $ref: '#/$defs/@context'

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum.github.io/bblock-dcat-ap-nl/build/annotated/bbr/dcat/dcat-ap-nl/schema.json)
* JSON version: [schema.json](https://geonovum.github.io/bblock-dcat-ap-nl/build/annotated/bbr/dcat/dcat-ap-nl/schema.yaml)

## Sources

* [DCAT-AP-NL 3.0 Specification](https://docs.geostandaarden.nl/dcat/dcat-ap-nl30/)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum/bblock-dcat-ap-nl](https://github.com/Geonovum/bblock-dcat-ap-nl)
* Path: `_sources/dcat-ap-nl`

