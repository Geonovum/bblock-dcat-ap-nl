
# DCAT-AP-NL profile 3.0 - Records binding Experimental (Model)

`geonovum.bbr.dcat.dcat-ap-nl-rec-dev` *v0.1*

DCAT-AP-NL 3.0 (Dutch profile of DCAT-AP) bound to OGC API Records. Used for experiments with semantic uplift and different patterns.

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## DCAT-AP-NL 3.0 bound to OGC API records schema


This building block defines a binding of the DCAT-AP-NL 3.0 profile to OGC API Records.

This profile extends a building block that uses the official JSON-LD context for DCAT bound to the OGC API Records.

It serves as a building block that follows the pattern for a Dataset description including distributions and dataservices.

All very much work in progress at the moment, the implementation might still change considerably.
## Examples

### DCAT-AP-NL with OGC API Records in JSON
An example based on the BAG metadata record from the NGR. 
Converted in JSON so the Semantic uplift via a JSON-LD context can be shown.

One of the reasons this does not validate is because it has multi lingual keywords... 
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
      "type": "application/xml"
    },
    {
      "rel": "access",
      "href": "https://service.pdok.nl/lv/bag/atom/bag.xml",
      "type": "application/xml"
    }
  ]
}
```

#### jsonld
```jsonld
{
  "@context": "https://geonovum.github.io/bblock-dcat-ap-nl/build/annotated/bbr/dcat/dcat-ap-nl-rec-dev/context.jsonld",
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
      "nl": "De gegevens bestaan uit BAG-panden en een deelselectie van BAG-gegevens van deze panden en de zich daarin bevindende verblijfsobjecten. Ook de ligplaatsen en standplaatsen zijn hierin opgenomen met een deelselectie van BAG-gegevens. De gegevens van de nummeraanduiding zijn in deze services onderdeel van de adresseerbare objecten, hierbij wordt slechts 1 adres opgenomen, dus objecten met meerdere adressen (hoofd- en nevenadressen) zijn niet compleet. In deze services zitten dus niet alle BAG adressen. Aangezien niet alle BAG gegevens worden geleverd, adviseren wij u om de actuele gegevens in \u00e9\u00e9n van de BAG producten te controleren. Raadpleeg de BAG Viewer voor enkele bevragingen van BAG gegevens. Een overzicht van alle beschikbare producten kunt u vinden op de website https://www.kadaster.nl/zakelijk/registraties/basisregistraties/bag . De BAG WMS, BAG WFS en BAG API Individuele bevragingen zijn expliciet niet bedoeld voor bulkbevragingen waarmee veel gegevens in \u00e9\u00e9n keer worden opgevraagd en in een database worden verwerkt. Wilt u in \u00e9\u00e9n keer meer gegevens opvragen, dan raden wij u aan om gebruik te maken van onze BAG Geopackage (https://www.kadaster.nl/zakelijk/producten/adressen-en-gebouwen/bag-geopackage) of BAG extract (https://www.kadaster.nl/zakelijk/producten/adressen-en-gebouwen/bag-2.0-extract). De BAG Geopackage en de BAG extract kunt u downloaden via de Atom downloadservice: https://service.pdok.nl/lv/bag/atom/bag.xml . Deze dataset wordt ook gebruikt voor het ontsluiten van het INSPIRE thema Gebouwen. Het betreft gebouwcontouren, constructieve onderdelen van gebouwen en ruimtelijke barrieres. Dit betreft niet-geharmoniseerde data uit de basisregistratie Adressen en Gebouwen (BAG). De service wordt dagelijks geactualiseerd."
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
      "type": "application/xml"
    },
    {
      "rel": "access",
      "href": "https://service.pdok.nl/lv/bag/atom/bag.xml",
      "type": "application/xml"
    }
  ]
}
```

#### ttl
```ttl
@prefix dcat: <http://www.w3.org/ns/dcat#> .
@prefix dct: <http://purl.org/dc/terms/> .
@prefix foaf: <http://xmlns.com/foaf/0.1/> .
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix ns1: <dcterms:> .
@prefix ns2: <dqv:> .
@prefix ns3: <http://www.iana.org/assignments/> .
@prefix oa: <http://www.w3.org/ns/oa#> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix rec: <https://www.opengis.net/def/ogc-api/records/> .
@prefix skos: <http://www.w3.org/2004/02/skos/core#> .
@prefix vcard: <http://www.w3.org/2006/vcard/ns#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<urn:ogc:record:generated-id> a "http://www.w3.org/ns/dcat#Dataset",
        "http://www.w3.org/ns/dcat#Resource",
        "http://www.w3.org/ns/prov#Entity" ;
    ns1:accessRights <http://inspire.ec.europa.eu/metadata-codelist/ConditionsApplyingToAccessAndUse/noConditionsApply> ;
    ns1:accrualPeriodicity <http://publications.europa.eu/resource/authority/frequency/DAILY> ;
    ns1:conformsTo [ a "http://purl.org/dc/terms/Standard" ;
            ns1:issued "2010-12-08" ;
            ns1:title [ ] ] ;
    ns1:created "2013-02-18" ;
    ns1:creator [ foaf:name "Kadaster"@nl ] ;
    ns1:description [ ] ;
    ns1:identifier "1fa33d90-79cb-11e2-b92a-0800200c9a66" ;
    ns1:language <http://publications.europa.eu/resource/authority/language/DUT> ;
    ns1:provenance [ a "http://purl.org/dc/terms/ProvenanceStatement" ;
            ns1:description [ ] ] ;
    ns1:publisher [ foaf:name "Klantcontactcenter"@nl ] ;
    ns1:spatial [ a "http://purl.org/dc/terms/Location" ;
            skos:prefLabel [ ] ],
        [ a "http://purl.org/dc/terms/Location" ;
            dcat:bbox [ dct:format "Polygon" ;
                    geojson:coordinates ( ( ( 2.4807e+00 5.37187e+01 ) ( 7.9685e+00 5.37187e+01 ) ( 7.9685e+00 5.06058e+01 ) ( 2.4807e+00 5.06058e+01 ) ( 2.4807e+00 5.37187e+01 ) ) ) ] ] ;
    ns1:temporal [ dcat:endDate "2025-12-31" ;
            dcat:startDate "1996-01-01" ] ;
    ns1:title [ ] ;
    ns2:hasQualityMeasurement [ a "http://www.w3.org/ns/dqv#QualityMeasurement" ;
            ns2:isMeasurementOf <http://data.europa.eu/930/spatialResolutionAsScale> ;
            ns2:value 1e-03 ] ;
    dct:conformsTo <http://modellen.geostandaarden.nl/dcat-ap-nl/>,
        <http://www.opengis.net/spec/ogcapi-records-1/1.0/req/record-core> ;
    dct:format "Feature" ;
    rdfs:seeAlso [ dct:type "application/xml" ;
            ns3:relation <http://www.iana.org/assignments/relation/access> ;
            oa:hasTarget <https://service.pdok.nl/lv/bag/wms/v2_0?request=getCapabilities&service=WMS> ],
        [ dct:type "application/xml" ;
            ns3:relation <http://www.iana.org/assignments/relation/access> ;
            oa:hasTarget <https://service.pdok.nl/lv/bag/atom/bag.xml> ] ;
    dcat:contactPoint [ ] ;
    dcat:keyword [ ],
        [ ],
        [ ],
        [ ],
        [ ],
        [ ],
        [ ] ;
    dcat:landingPage <https://api.bag.kadaster.nl/lvbag/individuelebevragingen/v2/>,
        <https://labs.kadaster.nl/cases/bag-ld> ;
    foaf:isPrimaryTopicOf [ a "http://www.w3.org/ns/dcat#CatalogRecord" ;
            ns1:identifier "aa3b5e6e-7baa-40c0-8972-3353e927ec2f" ;
            ns1:language "http://publications.europa.eu/resource/authority/language/DUT" ;
            ns1:modified "2024-08-26" ;
            dcat:contactPoint [ a "http://www.w3.org/2006/vcard/ns#Individual" ;
                    vcard:fn [ ] ;
                    vcard:hasAddress [ a "http://www.w3.org/2006/vcard/ns#Address" ;
                            vcard:country-name "Nederland" ;
                            vcard:locality "Apeldoorn" ;
                            vcard:postal-code "7311 KZ" ;
                            vcard:region "Gelderland" ;
                            vcard:street-address "Hofstraat 110" ] ;
                    vcard:hasEmail "mailto:dpi-gi@kadaster.nl" ;
                    vcard:hasURL "https://www.kadaster.nl" ;
                    vcard:organization-name [ ] ] ;
            foaf:primaryTopic "http://kadaster/1fa33d90-79cb-11e2-b92a-0800200c9a66" ] ;
    rec:themes [ skos:prefLabel [ ] ],
        [ skos:prefLabel [ ] ],
        [ skos:prefLabel [ ] ],
        [ skos:prefLabel [ ] ],
        [ skos:prefLabel [ ] ] .

<http://data.europa.eu/930/spatialResolutionAsScale> a "http://www.w3.org/ns/dqv#Metric" .

<http://inspire.ec.europa.eu/metadata-codelist/ConditionsApplyingToAccessAndUse/noConditionsApply> a "http://purl.org/dc/terms/LicenseDocument",
        "http://purl.org/dc/terms/RightsStatement" .

<http://publications.europa.eu/resource/authority/frequency/DAILY> a "http://purl.org/dc/terms/Frequency" .

<http://publications.europa.eu/resource/authority/language/DUT> a "http://purl.org/dc/terms/LinguisticSystem" .

<https://api.bag.kadaster.nl/lvbag/individuelebevragingen/v2/> a "http://xmlns.com/foaf/0.1/Document" ;
    ns1:description [ ] ;
    ns1:title [ ] .

<https://labs.kadaster.nl/cases/bag-ld> a "http://xmlns.com/foaf/0.1/Document" ;
    ns1:description [ ] ;
    ns1:title [ ] .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: Schema for OGCAPI records profile for DCAT Dataset - defines all extra
  elements defined by DCAT so that the JSON-LD context can map to DCAT RDF
allOf:
- $ref: https://ogcincubator.github.io/geodcat-ogcapi-records/build/annotated/geo/geodcat/dcat-records/schema.yaml
x-jsonld-extra-terms:
  a: '@type'
  accrualPeriodicity: http://purl.org/dc/terms/accrualPeriodicity
  distribution: http://www.w3.org/ns/dcat#distribution
  accessURL: http://www.w3.org/ns/dcat#accessURL
  mediaType: http://www.w3.org/ns/dcat#mediaType
  format: http://purl.org/dc/terms/format
  dataservice: http://www.w3.org/ns/dcat#DataService
  accessRights: http://purl.org/dc/terms/accessRights
  publisher: http://purl.org/dc/terms/publisher
  contactpunt: http://www.w3.org/ns/dcat#contactPoint
  fn:
    x-jsonld-id: http://www.w3.org/2006/vcard/ns#fn
    x-jsonld-language: nl
  organization-name:
    x-jsonld-id: http://www.w3.org/2006/vcard/ns#organization-name
    x-jsonld-container: '@language'
  hasEmail:
    x-jsonld-id: http://www.w3.org/2006/vcard/ns#hasEmail
    x-jsonld-type: '@id'
  creator: http://purl.org/dc/terms/creator
  orgtype:
    x-jsonld-id: http://purl.org/dc/terms/type
    x-jsonld-type: '@id'
  name:
    x-jsonld-id: http://xmlns.com/foaf/0.1/name
    x-jsonld-container: '@language'
  endpointURL: http://www.w3.org/ns/dcat#endpointURL
  servesDataset: http://www.w3.org/ns/dcat#servesDataset
  identifier: http://purl.org/dc/terms/identifier
  endpointDescription: http://www.w3.org/ns/dcat#endpointDescription
  themas:
    x-jsonld-id: http://www.w3.org/ns/dcat#theme
    x-jsonld-nest: nested_themes
  nested_themes:
    x-jsonld-id: '@null'
    x-jsonld-container: '@set'
  url:
    x-jsonld-id: http://www.w3.org/ns/dcat#theme
    x-jsonld-type: '@id'
x-jsonld-prefixes:
  dct: http://purl.org/dc/terms/
  dcat: http://www.w3.org/ns/dcat#
  vcard: http://www.w3.org/2006/vcard/ns#
  foaf: http://xmlns.com/foaf/0.1/
  skos: http://www.w3.org/2004/02/skos/core#

```

Links to the schema:

* YAML version: [schema.yaml](https://geonovum.github.io/bblock-dcat-ap-nl/build/annotated/bbr/dcat/dcat-ap-nl-rec-dev/schema.json)
* JSON version: [schema.json](https://geonovum.github.io/bblock-dcat-ap-nl/build/annotated/bbr/dcat/dcat-ap-nl-rec-dev/schema.yaml)


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
    "type": "dct:format",
    "id": "@id",
    "properties": "@nest",
    "geometry": {
      "@context": {
        "type": "@type"
      },
      "@id": "geojson:geometry"
    },
    "bbox": {
      "@container": "@list",
      "@id": "geojson:bbox"
    },
    "links": {
      "@context": {
        "type": "dct:type"
      },
      "@id": "rdfs:seeAlso"
    },
    "coordinates": {
      "@container": "@list",
      "@id": "geojson:coordinates"
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
            }
          }
        },
        "scheme": "rec:scheme"
      }
    },
    "formats": {
      "@id": "rec:format",
      "@context": {
        "name": "rec:name"
      }
    },
    "contacts": {
      "@container": "@set",
      "@id": "dcat:contactPoint",
      "@type": "@id"
    },
    "license": "dct:license",
    "accessrights": "dct:accessRights",
    "linkTemplates": "rec:hasLinkTemplate",
    "variables": {
      "@container": "@id",
      "@id": "rec:hasVariable",
      "@context": {
        "@base": "http://example.com/variables/",
        "@vocab": "https://www.opengis.net/def/ogc-api/records/"
      }
    },
    "a": "@type",
    "accrualPeriodicity": "dct:accrualPeriodicity",
    "distribution": "dcat:distribution",
    "accessURL": "dcat:accessURL",
    "mediaType": "dcat:mediaType",
    "format": "dct:format",
    "dataservice": "dcat:DataService",
    "accessRights": "dct:accessRights",
    "publisher": "dct:publisher",
    "contactpunt": "dcat:contactPoint",
    "fn": {
      "@id": "vcard:fn",
      "@language": "nl"
    },
    "organization-name": {
      "@id": "vcard:organization-name",
      "@container": "@language"
    },
    "hasEmail": {
      "@id": "vcard:hasEmail",
      "@type": "@id"
    },
    "creator": "dct:creator",
    "orgtype": {
      "@id": "dct:type",
      "@type": "@id"
    },
    "name": {
      "@id": "foaf:name",
      "@container": "@language"
    },
    "endpointURL": "dcat:endpointURL",
    "servesDataset": "dcat:servesDataset",
    "identifier": "dct:identifier",
    "endpointDescription": "dcat:endpointDescription",
    "themas": {
      "@id": "dcat:theme",
      "@nest": "nested_themes"
    },
    "nested_themes": {
      "@id": "@null",
      "@container": "@set"
    },
    "url": {
      "@id": "dcat:theme",
      "@type": "@id"
    },
    "geojson": "https://purl.org/geojson/vocab#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "oa": "http://www.w3.org/ns/oa#",
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
[context.jsonld](https://geonovum.github.io/bblock-dcat-ap-nl/build/annotated/bbr/dcat/dcat-ap-nl-rec-dev/context.jsonld)

## Sources

* [DCAT-AP-NL 3.0 Specification](https://docs.geostandaarden.nl/dcat/dcat-ap-nl30/)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/Geonovum/bblock-dcat-ap-nl](https://github.com/Geonovum/bblock-dcat-ap-nl)
* Path: `_sources/dcat-ap-nl-rec-dev`

