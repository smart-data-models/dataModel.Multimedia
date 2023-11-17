<!-- 10-Header -->    
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)    
エンティティメディアイベント    
==============<!-- /10-Header -->    
<!-- 15-License -->    
[オープン・ライセンス](https://github.com/smart-data-models//dataModel.Multimedia/blob/master/MediaEvent/LICENSE.md)    
[文書は自動的に生成される](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)    
<!-- /15-License -->    
<!-- 20-Description -->    
グローバルな記述：**メディアサーバーのエレメントによって発生する全てのイベントのベースとなる。    
バージョン: 0.0.2    
<!-- /20-Description -->    
<!-- 30-PropertiesList -->    
## プロパティのリスト    
<sup><sub>[*] 属性に型がない場合は、複数の型があるか、異なるフォーマット/パターンがある可能性があるためです</sub></sup>。    
- `address[object]`: 郵送先住所  . Model: [https://schema.org/address](https://schema.org/address)	- `addressCountry[string]`: 国。例えば、スペイン  . Model: [https://schema.org/addressCountry](https://schema.org/addressCountry)    
	- `addressLocality[string]`: 番地がある地域と、その地域に含まれる地域  . Model: [https://schema.org/addressLocality](https://schema.org/addressLocality)    
	- `addressRegion[string]`: その地域がある地域、またその国がある地域  . Model: [https://schema.org/addressRegion](https://schema.org/addressRegion)    
	- `district[string]`: 地区とは行政区画の一種で、国によっては地方自治体によって管理されている。      
	- `postOfficeBoxNumber[string]`: 私書箱の住所のための私書箱番号。例：03578  . Model: [https://schema.org/postOfficeBoxNumber](https://schema.org/postOfficeBoxNumber)    
	- `postalCode[string]`: 郵便番号。例：24004  . Model: [https://schema.org/https://schema.org/postalCode](https://schema.org/https://schema.org/postalCode)    
	- `streetAddress[string]`: 番地  . Model: [https://schema.org/streetAddress](https://schema.org/streetAddress)    
- `alternateName[string]`: この項目の別名  - `areaServed[string]`: サービスまたは提供品が提供される地理的地域  . Model: [https://schema.org/Text](https://schema.org/Text)- `data[object]`: イベントにアタッチされるシリアライズ可能なオブジェクト。例：プレート番号 + 属性タイプ  . Model: [http://schema.org/StructuredValue](http://schema.org/StructuredValue)- `dataProvider[string]`: ハーモナイズされたデータ・エンティティの提供者を識別する一連の文字。  - `dateCreated[date-time]`: エンティティの作成タイムスタンプ。これは通常、ストレージプラットフォームによって割り当てられます。  - `dateModified[date-time]`: エンティティの最終変更のタイムスタンプ。これは通常、ストレージプラットフォームによって割り当てられる。  - `description[string]`: この商品の説明  - `deviceSource[*]`: データソースを提供するデバイスへのリンク  . Model: [https://schema.org/URL](https://schema.org/URL)- `eventType[string]`: 発生したイベントの種類。(例: PlateDetectionEvent、ColourDetectionEventなど。  . Model: [https://schema.org/Text](https://schema.org/Text)- `id[*]`: エンティティの一意識別子  - `location[*]`: アイテムへの Geojson 参照。Point、LineString、Polygon、MultiPoint、MultiLineString、MultiPolygon のいずれか。  - `mediaSource[object]`: イベントを発生させたオブジェクトの技術情報  . Model: [https://schema.org/URL](https://schema.org/URL)	- `creationTime[date-time]`: メディアソースの作成日      
	- `name[string]`: このアイテムの名前      
	- `parent[object]`: イベントを発生させたオブジェクトの技術情報  . Model: [https://schema.org/URL](https://schema.org/URL)    
- `name[string]`: このアイテムの名前  - `observedEntities[array]`: このイベントによって更新または観測された、作成されたモデル・エンティティの配列。  . Model: [https://schema.org/StructuredValue](https://schema.org/StructuredValue)- `owner[array]`: 所有者の固有IDを参照するJSONエンコードされた文字列を含むリスト。  - `seeAlso[*]`: アイテムに関する追加リソースを指すURIのリスト  - `source[string]`: エンティティ・データの元のソースを URL として示す一連の文字。ソース・プロバイダの完全修飾ドメイン名、またはソース・オブジェクトの URL を推奨する。  - `type[string]`: NGSI エンティティタイプ。これは MediaEvent でなければならない。  <!-- /30-PropertiesList -->    
<!-- 35-RequiredProperties -->    
必須プロパティ    
- `dateCreated`  - `eventType`  - `id`  - `type`  <!-- /35-RequiredProperties -->    
<!-- 40-RequiredProperties -->    
データフィールドは、カスタムフィルターによって検出されたあらゆる情報を含むことができるようにオープンになっています。例えば、ナンバープレート用のフィルターはナンバープレートだけをデータとして持つかもしれませんが、フェンス用のフィルターは、クリティカリティ、違反の実際の座標、撮影された画像のURL、あるいはBASE64画像をデータとして持つかもしれません。    
<!-- /40-RequiredProperties -->    
<!-- 50-DataModelHeader -->    
## プロパティのデータモデル記述    
アルファベット順（クリックで詳細表示）    
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
## ペイロードの例    
#### MediaEvent NGSI-v2 キー値の例    
以下は、JSON-LD形式のMediaEventのkey-valuesの例である。これは、`options=keyValues`を使用した場合にNGSI-v2と互換性があり、個々のエンティティのコンテキストデータを返す。    
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
#### MediaEvent NGSI-v2 正規化例    
以下は、正規化されたJSON-LDフォーマットのMediaEventの例である。これは、オプションを使用しない場合、NGSI-v2と互換性があり、個々のエンティティのコンテキスト・データを返す。    
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
#### MediaEvent NGSI-LD キー値の例    
以下は、MediaEventをJSON-LD形式でkey-valuesとした例である。これは、`options=keyValues`を使用した場合にNGSI-LDと互換性があり、個々のエンティティのコンテキストデータを返す。    
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
#### メディアイベント NGSI-LD 正規化例    
以下は、正規化されたJSON-LDフォーマットのMediaEventの例である。これは、オプションを使用しない場合はNGSI-LDと互換性があり、個々のエンティティのコンテキストデータを返します。    
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
マグニチュード単位の扱い方については、[FAQ 10](https://smartdatamodels.org/index.php/faqs/)を参照のこと。    
<!-- /95-Units -->    
<!-- 97-LastFooter -->    
---    
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->    
