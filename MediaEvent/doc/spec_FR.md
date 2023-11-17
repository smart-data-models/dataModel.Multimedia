<!-- 10-Header -->    
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)    
Entité : MediaEvent    
===================<!-- /10-Header -->    
<!-- 15-License -->    
[Licence ouverte] (https://github.com/smart-data-models//dataModel.Multimedia/blob/master/MediaEvent/LICENSE.md)    
[document généré automatiquement] (https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)    
<!-- /15-License -->    
<!-- 20-Description -->    
Description globale : **Base pour tous les événements soulevés par les éléments du serveur de médias**    
version : 0.0.2    
<!-- /20-Description -->    
<!-- 30-PropertiesList -->    
## Liste des propriétés    
<sup><sub>[*] S'il n'y a pas de type dans un attribut, c'est parce qu'il peut avoir plusieurs types ou différents formats/modèles</sub></sup>.    
- `address[object]`: L'adresse postale  . Model: [https://schema.org/address](https://schema.org/address)	- `addressCountry[string]`: Le pays. Par exemple, l'Espagne  . Model: [https://schema.org/addressCountry](https://schema.org/addressCountry)    
	- `addressLocality[string]`: La localité dans laquelle se trouve l'adresse postale et qui se trouve dans la région  . Model: [https://schema.org/addressLocality](https://schema.org/addressLocality)    
	- `addressRegion[string]`: La région dans laquelle se trouve la localité et qui se trouve dans le pays  . Model: [https://schema.org/addressRegion](https://schema.org/addressRegion)    
	- `district[string]`: Un district est un type de division administrative qui, dans certains pays, est géré par le gouvernement local.      
	- `postOfficeBoxNumber[string]`: Le numéro de la boîte postale pour les adresses de boîtes postales. Par exemple, 03578  . Model: [https://schema.org/postOfficeBoxNumber](https://schema.org/postOfficeBoxNumber)    
	- `postalCode[string]`: Le code postal. Par exemple, 24004  . Model: [https://schema.org/https://schema.org/postalCode](https://schema.org/https://schema.org/postalCode)    
	- `streetAddress[string]`: L'adresse de la rue  . Model: [https://schema.org/streetAddress](https://schema.org/streetAddress)    
- `alternateName[string]`: Un nom alternatif pour ce poste  - `areaServed[string]`: La zone géographique où un service ou un article est offert  . Model: [https://schema.org/Text](https://schema.org/Text)- `data[object]`: Tout objet sérialisable attaché à l'événement. Par exemple : numéro de plaque + type d'attribut  . Model: [http://schema.org/StructuredValue](http://schema.org/StructuredValue)- `dataProvider[string]`: Une séquence de caractères identifiant le fournisseur de l'entité de données harmonisées  - `dateCreated[date-time]`: Horodatage de la création de l'entité. Celle-ci est généralement attribuée par la plate-forme de stockage  - `dateModified[date-time]`: Date de la dernière modification de l'entité. Cette date est généralement attribuée par la plate-forme de stockage  - `description[string]`: Une description de l'article  - `deviceSource[*]`: Lien vers le dispositif fournissant la source de données  . Model: [https://schema.org/URL](https://schema.org/URL)- `eventType[string]`: Type d'événement qui a été relevé. (ie : PlateDetectionEvent, ColourDetectionEvent, etc.  . Model: [https://schema.org/Text](https://schema.org/Text)- `id[*]`: Identifiant unique de l'entité  - `location[*]`: Référence Geojson à l'élément. Il peut s'agir d'un point, d'une chaîne de ligne, d'un polygone, d'un point multiple, d'une chaîne de ligne multiple ou d'un polygone multiple.  - `mediaSource[object]`: Informations techniques sur l'objet qui a déclenché l'événement  . Model: [https://schema.org/URL](https://schema.org/URL)	- `creationTime[date-time]`: Date de création de la source de média      
	- `name[string]`: Le nom de cet élément      
	- `parent[object]`: Informations techniques sur l'objet qui a déclenché l'événement  . Model: [https://schema.org/URL](https://schema.org/URL)    
- `name[string]`: Le nom de cet élément  - `observedEntities[array]`: Tableau des Entités du modèle créées, mises à jour ou simplement observées par cet événement  . Model: [https://schema.org/StructuredValue](https://schema.org/StructuredValue)- `owner[array]`: Une liste contenant une séquence de caractères encodés JSON référençant les identifiants uniques du ou des propriétaires.  - `seeAlso[*]`: liste d'uri pointant vers des ressources supplémentaires concernant l'élément  - `source[string]`: Séquence de caractères indiquant la source originale des données de l'entité sous forme d'URL. Il est recommandé d'utiliser le nom de domaine complet du fournisseur de la source ou l'URL de l'objet source.  - `type[string]`: Type d'entité NGSI. Il doit s'agir de MediaEvent  <!-- /30-PropertiesList -->    
<!-- 35-RequiredProperties -->    
Propriétés requises    
- `dateCreated`  - `eventType`  - `id`  - `type`  <!-- /35-RequiredProperties -->    
<!-- 40-RequiredProperties -->    
Le champ de données est ouvert afin de pouvoir contenir toute information détectée par des filtres personnalisés. Par exemple, un filtre pour les plaques d'immatriculation peut n'avoir comme données que le numéro de la plaque, mais un filtre pour les clôtures peut avoir comme données la criticité, les coordonnées réelles de la violation, et l'url d'une photo prise ou même l'image BASE64.    
<!-- /40-RequiredProperties -->    
<!-- 50-DataModelHeader -->    
## Modèle de données description des propriétés    
Classés par ordre alphabétique (cliquez pour plus de détails)    
<!-- /50-DataModelHeader -->    
<!-- 60-ModelYaml -->    
<details><summary><strong>full yaml details</strong></summary>      
```yaml    
MediaEvent:      
  description: Base for all events raised by elements in the media server      
  properties:      
    address:      
      description: The mailing address      
      properties:      
        addressCountry:      
          description: 'The country. For example, Spain'      
          type: string      
          x-ngsi:      
            model: https://schema.org/addressCountry      
            type: Property      
        addressLocality:      
          description: 'The locality in which the street address is, and which is in the region'      
          type: string      
          x-ngsi:      
            model: https://schema.org/addressLocality      
            type: Property      
        addressRegion:      
          description: 'The region in which the locality is, and which is in the country'      
          type: string      
          x-ngsi:      
            model: https://schema.org/addressRegion      
            type: Property      
        district:      
          description: 'A district is a type of administrative division that, in some countries, is managed by the local government'      
          type: string      
          x-ngsi:      
            type: Property      
        postOfficeBoxNumber:      
          description: 'The post office box number for PO box addresses. For example, 03578'      
          type: string      
          x-ngsi:      
            model: https://schema.org/postOfficeBoxNumber      
            type: Property      
        postalCode:      
          description: 'The postal code. For example, 24004'      
          type: string      
          x-ngsi:      
            model: https://schema.org/https://schema.org/postalCode      
            type: Property      
        streetAddress:      
          description: The street address      
          type: string      
          x-ngsi:      
            model: https://schema.org/streetAddress      
            type: Property      
        streetNr:      
          description: Number identifying a specific property on a public street      
          type: string      
          x-ngsi:      
            type: Property      
      type: object      
      x-ngsi:      
        model: https://schema.org/address      
        type: Property      
    alternateName:      
      description: An alternative name for this item      
      type: string      
      x-ngsi:      
        type: Property      
    areaServed:      
      description: The geographic area where a service or offered item is provided      
      type: string      
      x-ngsi:      
        model: https://schema.org/Text      
        type: Property      
    data:      
      description: 'Any serializable object that is attached to the event. Eg:plate-number + Attribute type'      
      type: object      
      x-ngsi:      
        model: http://schema.org/StructuredValue      
        type: Property      
    dataProvider:      
      description: A sequence of characters identifying the provider of the harmonised data entity      
      type: string      
      x-ngsi:      
        type: Property      
    dateCreated:      
      description: Entity creation timestamp. This will usually be allocated by the storage platform      
      format: date-time      
      type: string      
      x-ngsi:      
        type: Property      
    dateModified:      
      description: Timestamp of the last modification of the entity. This will usually be allocated by the storage platform      
      format: date-time      
      type: string      
      x-ngsi:      
        type: Property      
    description:      
      description: A description of this item      
      type: string      
      x-ngsi:      
        type: Property      
    deviceSource:      
      anyOf:      
        - description: Identifier format of any NGSI entity      
          maxLength: 256      
          minLength: 1      
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$      
          type: string      
          x-ngsi:      
            type: Property      
        - description: Identifier format of any NGSI entity      
          format: uri      
          type: string      
          x-ngsi:      
            type: Property      
      description: 'Link to the device providing the data source '      
      x-ngsi:      
        model: https://schema.org/URL      
        type: Relationship      
    eventType:      
      description: 'Type of event that was raised. (ie: PlateDetectionEvent, ColourDetectionEvent, etc'      
      type: string      
      x-ngsi:      
        model: https://schema.org/Text      
        type: Property      
    id:      
      anyOf:      
        - description: Identifier format of any NGSI entity      
          maxLength: 256      
          minLength: 1      
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$      
          type: string      
          x-ngsi:      
            type: Property      
        - description: Identifier format of any NGSI entity      
          format: uri      
          type: string      
          x-ngsi:      
            type: Property      
      description: Unique identifier of the entity      
      x-ngsi:      
        type: Property      
    location:      
      description: 'Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon'      
      oneOf:      
        - description: Geojson reference to the item. Point      
          properties:      
            bbox:      
              items:      
                type: number      
              minItems: 4      
              type: array      
            coordinates:      
              items:      
                type: number      
              minItems: 2      
              type: array      
            type:      
              enum:      
                - Point      
              type: string      
          required:      
            - type      
            - coordinates      
          title: GeoJSON Point      
          type: object      
          x-ngsi:      
            type: GeoProperty      
        - description: Geojson reference to the item. LineString      
          properties:      
            bbox:      
              items:      
                type: number      
              minItems: 4      
              type: array      
            coordinates:      
              items:      
                items:      
                  type: number      
                minItems: 2      
                type: array      
              minItems: 2      
              type: array      
            type:      
              enum:      
                - LineString      
              type: string      
          required:      
            - type      
            - coordinates      
          title: GeoJSON LineString      
          type: object      
          x-ngsi:      
            type: GeoProperty      
        - description: Geojson reference to the item. Polygon      
          properties:      
            bbox:      
              items:      
                type: number      
              minItems: 4      
              type: array      
            coordinates:      
              items:      
                items:      
                  items:      
                    type: number      
                  minItems: 2      
                  type: array      
                minItems: 4      
                type: array      
              type: array      
            type:      
              enum:      
                - Polygon      
              type: string      
          required:      
            - type      
            - coordinates      
          title: GeoJSON Polygon      
          type: object      
          x-ngsi:      
            type: GeoProperty      
        - description: Geojson reference to the item. MultiPoint      
          properties:      
            bbox:      
              items:      
                type: number      
              minItems: 4      
              type: array      
            coordinates:      
              items:      
                items:      
                  type: number      
                minItems: 2      
                type: array      
              type: array      
            type:      
              enum:      
                - MultiPoint      
              type: string      
          required:      
            - type      
            - coordinates      
          title: GeoJSON MultiPoint      
          type: object      
          x-ngsi:      
            type: GeoProperty      
        - description: Geojson reference to the item. MultiLineString      
          properties:      
            bbox:      
              items:      
                type: number      
              minItems: 4      
              type: array      
            coordinates:      
              items:      
                items:      
                  items:      
                    type: number      
                  minItems: 2      
                  type: array      
                minItems: 2      
                type: array      
              type: array      
            type:      
              enum:      
                - MultiLineString      
              type: string      
          required:      
            - type      
            - coordinates      
          title: GeoJSON MultiLineString      
          type: object      
          x-ngsi:      
            type: GeoProperty      
        - description: Geojson reference to the item. MultiLineString      
          properties:      
            bbox:      
              items:      
                type: number      
              minItems: 4      
              type: array      
            coordinates:      
              items:      
                items:      
                  items:      
                    items:      
                      type: number      
                    minItems: 2      
                    type: array      
                  minItems: 4      
                  type: array      
                type: array      
              type: array      
            type:      
              enum:      
                - MultiPolygon      
              type: string      
          required:      
            - type      
            - coordinates      
          title: GeoJSON MultiPolygon      
          type: object      
          x-ngsi:      
            type: GeoProperty      
      x-ngsi:      
        type: GeoProperty      
    mediaSource:      
      description: Technical information of the object that raised the event      
      properties:      
        creationTime:      
          description: System date of creation of the Media Source      
          format: date-time      
          type: string      
          x-ngsi:      
            type: Property      
        name:      
          description: The name of this item      
          type: string      
          x-ngsi:      
            type: Property      
        parent:      
          description: Technical information of the object that raised the event      
          properties:      
            creationTime:      
              description: System date of creation of the Media Source      
              format: date-time      
              type: string      
              x-ngsi:      
                type: Property      
            name:      
              description: The name of this item      
              type: string      
              x-ngsi:      
                type: Property      
            parent:      
              description: Technical information of the object that raised the event      
              properties:      
                creationTime:      
                  description: System date of creation of the Media Source      
                  format: date-time      
                  type: string      
                  x-ngsi:      
                    type: Property      
                name:      
                  description: The name of this item      
                  type: string      
                  x-ngsi:      
                    type: Property      
                parent:      
                  description: Technical information of the object that raised the event      
                  properties:      
                    creationTime:      
                      description: System date of creation of the Media Source      
                      format: date-time      
                      type: string      
                      x-ngsi:      
                        type: Property      
                    name:      
                      description: The name of this item      
                      type: string      
                      x-ngsi:      
                        type: Property      
                    parent:      
                      description: Technical information of the object that raised the event      
                      properties:      
                        creationTime:      
                        name:      
                        parent:      
                        sendTagsInEvents:      
                      type: object      
                      x-ngsi:      
                        model: https://schema.org/URL      
                        type: Property      
                    sendTagsInEvents:      
                      description: Wether the events rise for this media source attach the tag list associated to the MediaSource      
                      type: boolean      
                      x-ngsi:      
                        type: Property      
                  type: object      
                  x-ngsi:      
                    model: https://schema.org/URL      
                    type: Property      
                sendTagsInEvents:      
                  description: Wether the events rise for this media source attach the tag list associated to the MediaSource      
                  type: boolean      
                  x-ngsi:      
                    type: Property      
              type: object      
              x-ngsi:      
                model: https://schema.org/URL      
                type: Property      
            sendTagsInEvents:      
              description: Wether the events rise for this media source attach the tag list associated to the MediaSource      
              type: boolean      
              x-ngsi:      
                type: Property      
          type: object      
          x-ngsi:      
            model: https://schema.org/URL      
            type: Property      
        sendTagsInEvents:      
          description: Wether the events rise for this media source attach the tag list associated to the MediaSource      
          type: boolean      
          x-ngsi:      
            type: Property      
      type: object      
      x-ngsi:      
        model: https://schema.org/URL      
        type: Property      
    name:      
      description: The name of this item      
      type: string      
      x-ngsi:      
        type: Property      
    observedEntities:      
      description: Array of model Entities created updated or just observed by this event      
      items:      
        anyOf:      
          - description: Identifier format of any NGSI entity      
            maxLength: 256      
            minLength: 1      
            pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$      
            type: string      
            x-ngsi:      
              type: Property      
          - description: Identifier format of any NGSI entity      
            format: uri      
            type: string      
            x-ngsi:      
              type: Property      
      type: array      
      x-ngsi:      
        model: https://schema.org/StructuredValue      
        type: Property      
    owner:      
      description: A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)      
      items:      
        anyOf:      
          - description: Identifier format of any NGSI entity      
            maxLength: 256      
            minLength: 1      
            pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$      
            type: string      
            x-ngsi:      
              type: Property      
          - description: Identifier format of any NGSI entity      
            format: uri      
            type: string      
            x-ngsi:      
              type: Property      
        description: Unique identifier of the entity      
        x-ngsi:      
          type: Property      
      type: array      
      x-ngsi:      
        type: Property      
    seeAlso:      
      description: list of uri pointing to additional resources about the item      
      oneOf:      
        - items:      
            format: uri      
            type: string      
          minItems: 1      
          type: array      
        - format: uri      
          type: string      
      x-ngsi:      
        type: Property      
    source:      
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object'      
      type: string      
      x-ngsi:      
        type: Property      
    type:      
      description: NGSI Entity type. It has to be MediaEvent      
      enum:      
        - MediaEvent      
      type: string      
      x-ngsi:      
        type: Property      
  required:      
    - id      
    - type      
    - eventType      
    - dateCreated      
  type: object      
  x-derived-from: ""      
  x-disclaimer: 'Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2022 Contributors to Smart Data Models Program'      
  x-license-url: https://github.com/smart-data-models/dataModel.Multimedia/blob/master/MediaEvent/LICENSE.md      
  x-model-schema: ""      
  x-model-tags: ""      
  x-version: 0.0.2      
```    
</details>      
<!-- /60-ModelYaml -->    
<!-- 70-MiddleNotes -->    
<!-- /70-MiddleNotes -->    
<!-- 80-Examples -->    
## Exemples de charges utiles    
#### MediaEvent Valeurs clés NGSI-v2 Exemple    
Voici un exemple d'un MediaEvent au format JSON-LD en tant que valeurs clés. Ceci est compatible avec NGSI-v2 lorsque l'on utilise `options=keyValues` et renvoie les données de contexte d'une entité individuelle.    
<details><summary><strong>show/hide example</strong></summary>      
```json  
{  
  "id": "mediaEvent_1509702324600",  
  "type": "MediaEvent",  
  "eventType": "plate-detected",  
  "mediaSource": {  
    "name": "03ea110c-0ab2-4b19-8618-57f474721c86_kurento.MediaPipeline/28e4ae84-4e96-43bb-a812-538f7950b75f_platedetector.PlateDetectorFilter",  
    "creationTime": "2017-11-03T10:45:19Z",  
    "sendTagsInEvents": false,  
    "parent": {  
      "name": "03ea110c-0ab2-4b19-8618-57f474721c86_kurento.MediaPipeline",  
      "creationTime": "2017-11-03T10:45:19Z",  
      "sendTagsInEvents": false  
    }  
  },  
  "dateCreated": "2017-11-03T10:45:23Z"  
}  
```  
</details>    
#### MediaEvent NGSI-v2 normalisé Exemple    
Voici un exemple d'un MediaEvent au format JSON-LD tel que normalisé. Ce format est compatible avec la norme NGSI-v2 lorsqu'il n'utilise pas d'options et renvoie les données contextuelles d'une entité individuelle.    
<details><summary><strong>show/hide example</strong></summary>      
```json  
{  
  "id": "mediaEvent_1509702324600",  
  "type": "MediaEvent",  
  "eventType": {  
    "type": "Text",  
    "value": "plate-detected"  
  },  
  "mediaSource": {  
    "type": "StructuredValue",  
    "value": {  
      "name": "03ea110c-0ab2-4b19-8618-57f474721c86_kurento.MediaPipeline/28e4ae84-4e96-43bb-a812-538f7950b75f_platedetector.PlateDetectorFilter",  
      "creationTime": "2017-11-03T10:45:19Z",  
      "sendTagsInEvents": false,  
      "parent": {  
        "name": "03ea110c-0ab2-4b19-8618-57f474721c86_kurento.MediaPipeline",  
        "creationTime": "2017-11-03T10:45:19Z",  
        "sendTagsInEvents": false  
      }  
    }  
  },  
  "dateCreated": {  
    "type": "DateTime",  
    "value": "2017-11-03T10:45:23Z"  
  }  
}  
```  
</details>    
#### MediaEvent Valeurs clés NGSI-LD Exemple    
Voici un exemple d'un MediaEvent au format JSON-LD sous forme de valeurs clés. Ce format est compatible avec NGSI-LD lorsque l'on utilise `options=keyValues` et renvoie les données contextuelles d'une entité individuelle.    
<details><summary><strong>show/hide example</strong></summary>      
```json  
{  
    "id": "mediaEvent_1509702324600",  
    "type": "MediaEvent",  
    "dateCreated": "2017-11-03T10:45:23Z",  
    "eventType": "plate-detected",  
    "mediaSource": {  
        "name": "03ea110c-0ab2-4b19-8618-57f474721c86_kurento.MediaPipeline/28e4ae84-4e96-43bb-a812-538f7950b75f_platedetector.PlateDetectorFilter",  
        "creationTime": "2017-11-03T10:45:19Z",  
        "sendTagsInEvents": false,  
        "parent": {  
            "name": "03ea110c-0ab2-4b19-8618-57f474721c86_kurento.MediaPipeline",  
            "creationTime": "2017-11-03T10:45:19Z",  
            "sendTagsInEvents": false  
        }  
    },  
    "@context": [  
        "https://raw.githubusercontent.com/smart-data-models/dataModel.Multimedia/master/context.jsonld"  
    ]  
}  
```  
</details>    
#### MediaEvent NGSI-LD normalisé Exemple    
Voici un exemple d'un MediaEvent au format JSON-LD tel que normalisé. Ce format est compatible avec NGSI-LD lorsqu'il n'utilise pas d'options et renvoie les données contextuelles d'une entité individuelle.    
<details><summary><strong>show/hide example</strong></summary>      
```json  
{  
    "id": "mediaEvent_1509702324600",  
    "type": "MediaEvent",  
    "dateCreated": {  
        "type": "Property",  
        "value": {  
            "@type": "date-time",  
            "@value": "2017-11-03T10:45:23Z"  
        }  
    },  
    "eventType": {  
        "type": "Property",  
        "value": "plate-detected"  
    },  
    "mediaSource": {  
        "type": "Property",  
        "value": {  
            "name": "03ea110c-0ab2-4b19-8618-57f474721c86_kurento.MediaPipeline/28e4ae84-4e96-43bb-a812-538f7950b75f_platedetector.PlateDetectorFilter",  
            "creationTime": "2017-11-03T10:45:19Z",  
            "sendTagsInEvents": false,  
            "parent": {  
                "name": "03ea110c-0ab2-4b19-8618-57f474721c86_kurento.MediaPipeline",  
                "creationTime": "2017-11-03T10:45:19Z",  
                "sendTagsInEvents": false  
            }  
        }  
    },  
    "@context": [  
        "https://raw.githubusercontent.com/smart-data-models/dataModel.Multimedia/master/context.jsonld"  
    ]  
}  
```  
</details><!-- /80-Examples -->    
<!-- 90-FooterNotes -->    
<!-- /90-FooterNotes -->    
<!-- 95-Units -->    
Voir [FAQ 10] (https://smartdatamodels.org/index.php/faqs/) pour obtenir une réponse à la question de savoir comment traiter les unités de magnitude.    
<!-- /95-Units -->    
<!-- 97-LastFooter -->    
---    
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->    
