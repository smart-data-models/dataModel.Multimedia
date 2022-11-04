<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
Entidad: MediaEvent  
===================<!-- /10-Header -->  
<!-- 15-License -->  
[Licencia abierta](https://github.com/smart-data-models//dataModel.Multimedia/blob/master/MediaEvent/LICENSE.md)  
[documento generado automáticamente](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
Descripción global: **Base para todos los eventos levantados por elementos en el servidor de medios**  
versión: 0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## Lista de propiedades  

<sup><sub>[*] Si no hay un tipo en un atributo es porque puede tener varios tipos o diferentes formatos/patrones</sub></sup>  
- `address[object]`: La dirección postal  . Model: [https://schema.org/address](https://schema.org/address)- `alternateName[string]`: Un nombre alternativo para este artículo  - `areaServed[string]`: La zona geográfica en la que se presta un servicio o se ofrece un artículo  . Model: [https://schema.org/Text](https://schema.org/Text)- `data[object]`: Cualquier objeto serializable que se adjunte al evento. Eg:número de placa + tipo de atributo  . Model: [http://schema.org/StructuredValue](http://schema.org/StructuredValue)- `dataProvider[string]`: Una secuencia de caracteres que identifica al proveedor de la entidad de datos armonizada.  - `dateCreated[string]`: Marca de tiempo de creación de la entidad. Suele ser asignada por la plataforma de almacenamiento.  - `dateModified[string]`: Marca de tiempo de la última modificación de la entidad. Normalmente será asignada por la plataforma de almacenamiento.  - `description[string]`: Una descripción de este artículo  - `deviceSource[*]`: Enlace al dispositivo que proporciona la fuente de datos  . Model: [https://schema.org/URL](https://schema.org/URL)- `eventType[string]`: Tipo de evento que se ha producido. (es decir, PlateDetectionEvent, ColourDetectionEvent, etc.).  . Model: [https://schema.org/Text](https://schema.org/Text)- `id[*]`: Identificador único de la entidad  - `location[*]`: Referencia Geojson al elemento. Puede ser Point, LineString, Polygon, MultiPoint, MultiLineString o MultiPolygon  - `mediaSource[object]`: Información técnica del objeto que ha provocado el evento  . Model: [https://schema.org/URL.](https://schema.org/URL.)- `name[string]`: El nombre de este artículo.  - `observedEntities[array]`: Array de Entidades modelo creadas actualizadas o simplemente observadas por este evento.  . Model: [https://schema.org/StructuredValue](https://schema.org/StructuredValue)- `owner[array]`: Una lista que contiene una secuencia de caracteres codificada en JSON que hace referencia a los identificadores únicos de los propietarios  - `seeAlso[*]`: lista de uri que apuntan a recursos adicionales sobre el artículo  - `source[string]`: Una secuencia de caracteres que indica la fuente original de los datos de la entidad en forma de URL. Se recomienda que sea el nombre de dominio completo del proveedor de origen o la URL del objeto de origen.  - `type[string]`: Tipo de entidad NGSI. Tiene que ser MediaEvent  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
Propiedades requeridas  
- `dateCreated`  - `eventType`  - `id`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-RequiredProperties -->  
El campo de datos está abierto para poder contener cualquier información detectada por los filtros personalizados. Por ejemplo, un filtro de matrículas de tráfico puede tener como datos sólo el número de matrícula, pero un filtro de vallas puede tener como datos la criticidad, las coordenadas reales de la infracción y la url de una foto tomada o incluso la imagen BASE64  
<!-- /40-RequiredProperties -->  
<!-- 50-DataModelHeader -->  
## Descripción del modelo de datos de las propiedades  
Ordenados alfabéticamente (haga clic para ver los detalles)  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
MediaEvent:    
  description: 'Base for all events raised by elements in the media server'    
  properties:    
    address:    
      description: 'The mailing address'    
      properties:    
        addressCountry:    
          description: 'Property. The country. For example, Spain. Model:''https://schema.org/addressCountry'''    
          type: string    
        addressLocality:    
          description: 'Property. The locality in which the street address is, and which is in the region. Model:''https://schema.org/addressLocality'''    
          type: string    
        addressRegion:    
          description: 'Property. The region in which the locality is, and which is in the country. Model:''https://schema.org/addressRegion'''    
          type: string    
        postOfficeBoxNumber:    
          description: 'Property. The post office box number for PO box addresses. For example, 03578. Model:''https://schema.org/postOfficeBoxNumber'''    
          type: string    
        postalCode:    
          description: 'Property. The postal code. For example, 24004. Model:''https://schema.org/https://schema.org/postalCode'''    
          type: string    
        streetAddress:    
          description: 'Property. The street address. Model:''https://schema.org/streetAddress'''    
          type: string    
      type: object    
      x-ngsi:    
        model: https://schema.org/address    
        type: Property    
    alternateName:    
      description: 'An alternative name for this item'    
      type: string    
      x-ngsi:    
        type: Property    
    areaServed:    
      description: 'The geographic area where a service or offered item is provided'    
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
      description: 'A sequence of characters identifying the provider of the harmonised data entity.'    
      type: string    
      x-ngsi:    
        type: Property    
    dateCreated:    
      description: 'Entity creation timestamp. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    dateModified:    
      description: 'Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    description:    
      description: 'A description of this item'    
      type: string    
      x-ngsi:    
        type: Property    
    deviceSource:    
      anyOf:    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'Link to the device providing the data source '    
      x-ngsi:    
        model: https://schema.org/URL    
        type: Relationship    
    eventType:    
      description: 'Type of event that was raised. (ie: PlateDetectionEvent, ColourDetectionEvent, etc.'    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    id:    
      anyOf: &mediaevent_-_properties_-_owner_-_items_-_anyof    
        - description: 'Property. Identifier format of any NGSI entity'    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: 'Property. Identifier format of any NGSI entity'    
          format: uri    
          type: string    
      description: 'Unique identifier of the entity'    
      x-ngsi:    
        type: Property    
    location:    
      description: 'Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon'    
      oneOf:    
        - description: 'GeoProperty. Geojson reference to the item. Point'    
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
          title: 'GeoJSON Point'    
          type: object    
        - description: 'GeoProperty. Geojson reference to the item. LineString'    
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
          title: 'GeoJSON LineString'    
          type: object    
        - description: 'GeoProperty. Geojson reference to the item. Polygon'    
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
          title: 'GeoJSON Polygon'    
          type: object    
        - description: 'GeoProperty. Geojson reference to the item. MultiPoint'    
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
          title: 'GeoJSON MultiPoint'    
          type: object    
        - description: 'GeoProperty. Geojson reference to the item. MultiLineString'    
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
          title: 'GeoJSON MultiLineString'    
          type: object    
        - description: 'GeoProperty. Geojson reference to the item. MultiLineString'    
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
          title: 'GeoJSON MultiPolygon'    
          type: object    
      x-ngsi:    
        type: GeoProperty    
    mediaSource:    
      description: 'Technical information of the object that raised the event'    
      properties: &mediaevent_-_properties_-_mediasource_-_properties_-_parent_-_properties    
        creationTime:    
          description: 'Property. System date of creation of the Media Source'    
          format: date-time    
          type: string    
        name:    
          description: 'Property. The name of this item.'    
          type: string    
        parent:    
          description: 'Property. Technical information of the object that raised the event. Model:''https://schema.org/URL''.'    
          properties: *mediaevent_-_properties_-_mediasource_-_properties_-_parent_-_properties    
          type: object    
        sendTagsInEvents:    
          description: 'Property. Does the events rise for this media source attach the tag list associated to the MediaSource?'    
          type: boolean    
      type: object    
      x-ngsi:    
        model: https://schema.org/URL.    
        type: Property    
    name:    
      description: 'The name of this item.'    
      type: string    
      x-ngsi:    
        type: Property    
    observedEntities:    
      description: 'Array of model Entities created updated or just observed by this event.'    
      items:    
        anyOf:    
          - description: 'Property. Identifier format of any NGSI entity'    
            maxLength: 256    
            minLength: 1    
            pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
            type: string    
          - description: 'Property. Identifier format of any NGSI entity'    
            format: uri    
            type: string    
      type: array    
      x-ngsi:    
        model: https://schema.org/StructuredValue    
        type: Property    
    owner:    
      description: 'A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)'    
      items:    
        anyOf: *mediaevent_-_properties_-_owner_-_items_-_anyof    
        description: 'Property. Unique identifier of the entity'    
      type: array    
      x-ngsi:    
        type: Property    
    seeAlso:    
      description: 'list of uri pointing to additional resources about the item'    
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
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.'    
      type: string    
      x-ngsi:    
        type: Property    
    type:    
      description: 'NGSI Entity type. It has to be MediaEvent'    
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
  x-disclaimer: 'Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2021 Contributors to Smart Data Models Program'    
  x-license-url: https://github.com/smart-data-models/dataModel.Multimedia/blob/master/MediaEvent/LICENSE.md    
  x-model-schema: ""    
  x-model-tags: ""    
  x-version: 0.0.1    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## Ejemplo de carga útil  
#### MediaEvent NGSI-v2 key-values Ejemplo  
Aquí hay un ejemplo de un MediaEvent en formato JSON-LD como valores-clave. Esto es compatible con NGSI-v2 cuando se utiliza `options=keyValues` y devuelve los datos de contexto de una entidad individual.  
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
#### MediaEvent NGSI-v2 normalizado Ejemplo  
Este es un ejemplo de un MediaEvent en formato JSON-LD normalizado. Esto es compatible con NGSI-v2 cuando no se utilizan opciones y devuelve los datos de contexto de una entidad individual.  
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
#### MediaEvent NGSI-LD key-values Ejemplo  
Aquí hay un ejemplo de un MediaEvent en formato JSON-LD como valores-clave. Esto es compatible con NGSI-LD cuando se utiliza `options=keyValues` y devuelve los datos de contexto de una entidad individual.  
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
#### MediaEvent NGSI-LD normalizado Ejemplo  
Este es un ejemplo de un MediaEvent en formato JSON-LD normalizado. Esto es compatible con NGSI-LD cuando no se utilizan opciones y devuelve los datos de contexto de una entidad individual.  
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
Consulte [FAQ 10](https://smartdatamodels.org/index.php/faqs/) para obtener una respuesta sobre cómo tratar las unidades de magnitud  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
