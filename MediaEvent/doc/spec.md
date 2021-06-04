Entity: MediaEvent  
==================  
[Open License](https://github.com/smart-data-models//dataModel.Multimedia/blob/master/MediaEvent/LICENSE.md)  
[document generated automatically](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
Global description: **Base for all events raised by elements in the media server**  

## List of properties  

- `address`: The mailing address  - `alternateName`: An alternative name for this item  - `areaServed`: The geographic area where a service or offered item is provided  - `data`: Any serializable object that is attached to the event. Eg:plate-number + Attribute type  - `dataProvider`: A sequence of characters identifying the provider of the harmonised data entity.  - `dateCreated`: Entity creation timestamp. This will usually be allocated by the storage platform.  - `dateModified`: Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.  - `description`: A description of this item  - `deviceSource`: Link to the device providing the data source   - `eventType`: Type of event that was raised. (ie: PlateDetectionEvent, ColourDetectionEvent, etc.  - `id`: Unique identifier of the entity  - `location`: Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon  - `mediaSource`: Technical information of the object that raised the event  - `name`: The name of this item.  - `observedEntities`: Array of model Entities created updated or just observed by this event.  - `owner`: A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)  - `seeAlso`: list of uri pointing to additional resources about the item  - `source`: A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.  - `type`: NGSI Entity type. It has to be MediaEvent    
Required properties  
- `dateCreated`  - `eventType`  - `id`  - `type`    
The data field is open in order to be able to contain any information detected by custom filters. For example a filter for trafic plates may just have as data the plate number but a fencing filter might have as data the criticality, the actual coordinates of the violation, and the url of a taken picture  or even the BASE64 image  
## Data Model description of properties  
Sorted alphabetically (click for details)  
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
      type: Property    
      x-ngsi:    
        model: https://schema.org/address    
    alternateName:    
      description: 'An alternative name for this item'    
      type: Property    
    areaServed:    
      description: 'The geographic area where a service or offered item is provided'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Text    
    data:    
      description: 'Any serializable object that is attached to the event. Eg:plate-number + Attribute type'    
      type: Property    
      x-ngsi:    
        model: http://schema.org/StructuredValue    
    dataProvider:    
      description: 'A sequence of characters identifying the provider of the harmonised data entity.'    
      type: Property    
    dateCreated:    
      description: 'Entity creation timestamp. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: Property    
    dateModified:    
      description: 'Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.'    
      format: date-time    
      type: Property    
    description:    
      description: 'A description of this item'    
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
      type: Relationship    
      x-ngsi:    
        model: https://schema.org/URL    
    eventType:    
      description: 'Type of event that was raised. (ie: PlateDetectionEvent, ColourDetectionEvent, etc.'    
      type: Property    
      x-ngsi:    
        model: https://schema.org/Text    
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
      type: Property    
    location:    
      description: 'Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon'    
      oneOf:    
        - description: 'Geoproperty. Geojson reference to the item. Point'    
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
        - description: 'Geoproperty. Geojson reference to the item. LineString'    
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
        - description: 'Geoproperty. Geojson reference to the item. Polygon'    
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
        - description: 'Geoproperty. Geojson reference to the item. MultiPoint'    
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
        - description: 'Geoproperty. Geojson reference to the item. MultiLineString'    
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
        - description: 'Geoproperty. Geojson reference to the item. MultiLineString'    
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
      type: Geoproperty    
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
      type: Property    
      x-ngsi:    
        model: https://schema.org/URL.    
    name:    
      description: 'The name of this item.'    
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
      type: Property    
      x-ngsi:    
        model: https://schema.org/StructuredValue    
    owner:    
      description: 'A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)'    
      items:    
        anyOf: *mediaevent_-_properties_-_owner_-_items_-_anyof    
        description: 'Property. Unique identifier of the entity'    
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
      type: Property    
    source:    
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.'    
      type: Property    
    type:    
      description: 'NGSI Entity type. It has to be MediaEvent'    
      enum:    
        - MediaEvent    
      type: Property    
  required:    
    - id    
    - type    
    - eventType    
    - dateCreated    
  type: object    
```  
</details>    
## Example payloads    
#### MediaEvent NGSI-v2 key-values Example    
Here is an example of a MediaEvent in JSON-LD format as key-values. This is compatible with NGSI-v2 when  using `options=keyValues` and returns the context data of an individual entity.  
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
#### MediaEvent NGSI-v2 normalized Example    
Here is an example of a MediaEvent in JSON-LD format as normalized. This is compatible with NGSI-v2 when not using options and returns the context data of an individual entity.  
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
#### MediaEvent NGSI-LD key-values Example    
Here is an example of a MediaEvent in JSON-LD format as key-values. This is compatible with NGSI-LD when  using `options=keyValues` and returns the context data of an individual entity.  
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
  "dateCreated": "2017-11-03T10:45:23Z",  
  "@context": ["https://smartdatamodels.org/context.jsonld"]  
}  
```  
#### MediaEvent NGSI-LD normalized Example    
Here is an example of a MediaEvent in JSON-LD format as normalized. This is compatible with NGSI-LD when not using options and returns the context data of an individual entity.  
```json  
{  
  "id": "mediaEvent_1509702324600",  
  "type": "MediaEvent",  
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
  "dateCreated": {  
    "type": "Property",  
    "value": {  
      "@type": "date-time",  
      "@value": "2017-11-03T10:45:23Z"  
    }  
  },  
  "@context": [  
    "https://smartdatamodels.org/context.jsonld"  
  ]  
}  
```  
