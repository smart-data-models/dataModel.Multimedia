<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
实体：媒体事件  
=======<!-- /10-Header -->  
<!-- 15-License -->  
[开放许可](https://github.com/smart-data-models//dataModel.Multimedia/blob/master/MediaEvent/LICENSE.md)  
[文件自动生成](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
全局描述：媒体服务器元素引发的所有事件的**基础**  
版本： 0.0.2  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## 属性列表  

<sup><sub>[*] 如果属性中没有类型，是因为它可能有多个类型或不同的格式/模式</sub></sup>。  
- `address[object]`: 邮寄地址  . Model: [https://schema.org/address](https://schema.org/address)	- `addressCountry[string]`: 国家。例如，西班牙  . Model: [https://schema.org/addressCountry](https://schema.org/addressCountry)  
	- `addressLocality[string]`: 街道地址所在的地点，以及该地点所在的区域  . Model: [https://schema.org/addressLocality](https://schema.org/addressLocality)  
	- `addressRegion[string]`: 地点所在的地区，以及该地区位于哪个国家  . Model: [https://schema.org/addressRegion](https://schema.org/addressRegion)  
	- `district[string]`: 地区是一种行政区划，在一些国家由地方政府管理    
	- `postOfficeBoxNumber[string]`: 用于邮政信箱地址的邮政信箱号码。例如：03578  . Model: [https://schema.org/postOfficeBoxNumber](https://schema.org/postOfficeBoxNumber)  
	- `postalCode[string]`: 邮政编码。例如：24004  . Model: [https://schema.org/https://schema.org/postalCode](https://schema.org/https://schema.org/postalCode)  
	- `streetAddress[string]`: 街道地址  . Model: [https://schema.org/streetAddress](https://schema.org/streetAddress)  
- `alternateName[string]`: 该项目的替代名称  - `areaServed[string]`: 提供服务或提供物品的地理区域  . Model: [https://schema.org/Text](https://schema.org/Text)- `data[object]`: 附加到事件的任何可序列化对象。例如：牌号 + 属性类型  . Model: [http://schema.org/StructuredValue](http://schema.org/StructuredValue)- `dataProvider[string]`: 标识统一数据实体提供者的字符序列  - `dateCreated[date-time]`: 实体创建时间戳。通常由存储平台分配  - `dateModified[date-time]`: 实体最后一次修改的时间戳。通常由存储平台分配  - `description[string]`: 项目描述  - `deviceSource[*]`: 链接到提供数据源的设备  . Model: [https://schema.org/URL](https://schema.org/URL)- `eventType[string]`: 触发事件的类型。(即：PlateDetectionEvent、ColourDetectionEvent 等  . Model: [https://schema.org/Text](https://schema.org/Text)- `id[*]`: 实体的唯一标识符  - `location[*]`: 项目的 Geojson 引用。它可以是点、线条字符串、多边形、多点、多线条字符串或多多边形  - `mediaSource[object]`: 事件发生对象的技术信息  . Model: [https://schema.org/URL](https://schema.org/URL)	- `creationTime[date-time]`: 媒体源的系统创建日期    
	- `name[string]`: 该项目的名称    
	- `parent[object]`: 事件发生对象的技术信息  . Model: [https://schema.org/URL](https://schema.org/URL)  
- `name[string]`: 该项目的名称  - `observedEntities[array]`: 由该事件创建、更新或刚刚观察到的模型实体的数组  . Model: [https://schema.org/StructuredValue](https://schema.org/StructuredValue)- `owner[array]`: 包含一个 JSON 编码字符序列的列表，其中引用了所有者的唯一 Ids  - `seeAlso[*]`: 指向有关该项目的其他资源的 uri 列表  - `source[string]`: 以 URL 形式给出实体数据原始来源的字符串。建议使用源提供者的完全合格域名或源对象的 URL  - `type[string]`: NGSI 实体类型。必须是 MediaEvent  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
所需属性  
- `dateCreated`  - `eventType`  - `id`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-RequiredProperties -->  
数据字段是开放的，可以包含自定义过滤器检测到的任何信息。例如，车牌过滤器的数据可能只有车牌号，但围栏过滤器的数据可能包括临界值、违规行为的实际坐标、所拍图片的网址甚至 BASE64 图像。  
<!-- /40-RequiredProperties -->  
<!-- 50-DataModelHeader -->  
## 属性的数据模型描述  
按字母顺序排列（点击查看详情）  
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
## 有效载荷示例  
#### MediaEvent NGSI-v2 键值示例  
下面是一个以 JSON-LD 格式作为键值的 MediaEvent 示例。当使用 `options=keyValues` 时，它与 NGSI-v2 兼容，并返回单个实体的上下文数据。  
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
#### 媒体事件 NGSI-v2 标准化示例  
下面是一个规范化 JSON-LD 格式的 MediaEvent 示例。当不使用选项时，它与 NGSI-v2 兼容，并返回单个实体的上下文数据。  
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
#### 媒体事件 NGSI-LD 键值示例  
下面是一个以 JSON-LD 格式作为键值的 MediaEvent 示例。当使用 `options=keyValues` 时，它与 NGSI-LD 兼容，并返回单个实体的上下文数据。  
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
#### 媒体事件 NGSI-LD 标准化示例  
下面是一个规范化 JSON-LD 格式的 MediaEvent 示例。在不使用选项时，它与 NGSI-LD 兼容，并返回单个实体的上下文数据。  
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
请参阅 [FAQ 10](https://smartdatamodels.org/index.php/faqs/)，获取如何处理幅度单位的答案。  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
