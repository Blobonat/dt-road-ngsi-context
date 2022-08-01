# Road

Diese Entität enthält eine vereinheitlichte geografische und kontextuelle Beschreibung einer Straße.
-  `address`: Die Postadresse
   -  Attribute type: **Property**. [address](https://schema.org/address)
   -  Optional
-  `id`: Eindeutiger Bezeichner der Entität
   -  Attribute type: **Property**. 
   -  Required
-  `name`: Name der Entität
   -  Attribute type: **Property**. 
   -  Required
-  `refRoadSegment`: Straßensegmente, die diese Straße definieren. Liste der Referenzen auf Entitäten des Typs RoadSegment
   -  Attribute type: **Relationship**. [URL](https://schema.org/URL)
   -  Optional
   -  Meta Data: 
       -  `datasetId`: Eindeutiger Bezeichner des Datasets
           -  Attribute type: **Property**. 
-  `roadClass`: Staßenklassifizierung. Enum:'motorway, primary, residential, secondary, service, tertiary, trunk, unclassified'.  Erlaubte Werte: Werte gemäß [OpenStreetMap](http://wiki.openstreetmap.org/wiki/Key:highway).. One of : `motorway`, `primary`, `residential`, `secondary`, `service`, `tertiary`, `trunk`, `unclassified`.
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Required
-  `type`: Typ der NGSI-Entität. Muss 'Road' sein. One of : `Road`.
   -  Attribute type: **Property**. 
   -  Required



# RoadSegment

Diese Entität enthält eine vereinheitlichte geografische und kontextbezogene Beschreibung eines Straßensegments. Eine Menge von Straßensegmenten wird zur Beschreibung einer Straße verwendet.
-  `endPoint`: Geojson-Referenz auf das Element. Kann Point, LineString, Polygon, MultiPoint, MultiLineString oder MultiPolygon sein
   -  Attribute type: **GeoProperty**. 
   -  Required
-  `id`: Eindeutiger Bezeichner der Entität
   -  Attribute type: **Property**. 
   -  Required
-  `name`: Name des Elements.
   -  Attribute type: **Property**. 
   -  Required
-  `refRoad`: Straße, zu der das Straßensegment gehört.
   -  Attribute type: **Relationship**. 
   -  Required
-  `startPoint`: Geojson-Referenz auf das Element. Kann Point, LineString, Polygon, MultiPoint, MultiLineString oder MultiPolygon sein
   -  Attribute type: **GeoProperty**. 
   -  Required
-  `totalLaneNumber`: Gesamtzahl der Fahrspuren des Straßensegments
   -  Attribute type: **Property**. [Number](https://schema.org/Number)
   -  Optional
-  `type`: Typ der NGSI-Entität. Muss 'RoadSegment' sein. One of : `RoadSegment`.
   -  Attribute type: **Property**. 
   -  Required
-  `airTemperature`: Lufttemperatur
   -  Attribute type: **Property**. [Number](https://schema.org/Number)
   -  Optional
   -  Meta Data: 
       -  `isMeasuredByDevice`: Property. Bezeichnungsformat der NGSI-Entität, welche das Gerät ist, welches die Messung zur Verfügung stellt.
           -  Attribute type: **Relationship**. 
       -  `observedAt`: Ein Zeitstempel, welcher angibt, wann der Wert abgelesen wurde.
           -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
       -  `unitCode`: Eine Zeichenfolge, welche die, der Messung entsprechenden, Maßeinheit darstellt. Sie ist unter Verwendung der UN/CEFACT Common Codes for Units of Measurement zu kodieren
           -  Attribute type: **Property**. [Text](https://schema.org/Text)
-  `humidity`: Relative Luftfeuchtigkeit
   -  Attribute type: **Property**. [Number](https://schema.org/Number)
   -  Optional
   -  Meta Data: 
       -  `isMeasuredByDevice`: Property. Bezeichnungsformat der NGSI-Entität, welche das Gerät ist, welches die Messung zur Verfügung stellt.
           -  Attribute type: **Relationship**. 
       -  `observedAt`: Ein Zeitstempel, welcher angibt, wann der Wert abgelesen wurde.
           -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
       -  `unitCode`: Eine Zeichenfolge, welche die, der Messung entsprechenden, Maßeinheit darstellt. Sie ist unter Verwendung der UN/CEFACT Common Codes for Units of Measurement zu kodieren
           -  Attribute type: **Property**. [Text](https://schema.org/Text)
-  `constructionDate`: Date the construction of the road segment was finished.
   -  Attribute type: **Property**. [Date](https://schema.org/Date)
   -  Optional
-  `surfaceTemperature`: Oberflächentemperatur
   -  Attribute type: **Property**. [Number](https://schema.org/Number)
   -  Optional
   -  Meta Data: 
       -  `isMeasuredByDevice`: Property. Bezeichnungsformat der NGSI-Entität, welche das Gerät ist, welches die Messung zur Verfügung stellt.
           -  Attribute type: **Relationship**. 
       -  `observedAt`: Ein Zeitstempel, welcher angibt, wann der Wert abgelesen wurde.
           -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
       -  `unitCode`: Eine Zeichenfolge, welche die, der Messung entsprechenden, Maßeinheit darstellt. Sie ist unter Verwendung der UN/CEFACT Common Codes for Units of Measurement zu kodieren
           -  Attribute type: **Property**. [Text](https://schema.org/Text)
-  `pavementConditionIndex`: The pavement condidition of a road segment according to the pavement condition index (PCI). Enum:'good, satisfactory, fair, poor, veryPoor, serious, failed'.  Allowed values: Those classes described by [Wikipedia](https://en.wikipedia.org/wiki/Pavement_condition_index#Categorization).. One of : `good`, `satisfactory`, `fair`, `poor`, `veryPoor`, `serious`, `failed`.
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Optional
   -  Meta Data: 
       -  `observedAt`: Ein Zeitstempel, welcher angibt, wann der Wert abgelesen wurde.
           -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
-  `roadSurfaceCondition`: Oberflächenzustand einer Straße. Enum:'dry, dampOrWet, frozen'.  Erlaubte Werte: Werte in Anlehnung an [TLS DE-Typ 70 (0, 32, 64)](https://www.bast.de/DE/Publikationen/Regelwerke/Verkehrstechnik/Unterseiten/V5-tls-2012.html).. One of : `dry`, `dampOrWet`, `frozen`.
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Optional
   -  Meta Data: 
       -  `isMeasuredByDevice`: Property. Bezeichnungsformat der NGSI-Entität, welche das Gerät ist, welches die Messung zur Verfügung stellt.
           -  Attribute type: **Relationship**. 
       -  `observedAt`: Ein Zeitstempel, welcher angibt, wann der Wert abgelesen wurde.
           -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
-  `roadSlipperyRisk`: The slippery condition of a road. Enum:'low, moderate, high'.. One of : `low`, `moderate`, `high`.
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Optional
   -  Meta Data: 
       -  `observedAt`: Ein Zeitstempel, welcher angibt, wann der Wert abgelesen wurde.
           -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
-  `structure`: Dieses Attribut kann verwendet werden, um spezifische Parameter zu übermitteln, welche die Dicke und das Material für jede Schicht des Straßenabschnitts beschreiben. Es muss eine Zeichenfolge pro Schicht des Straßenabschnitts enthalten. Das Element 0 des Arrays muss die Angaben zur obersten Schicht enthalten, usw. Das Format der Zeichenkette entspricht: <Schichtdicke in mm>, <Schichtmaterial>
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Optional
   -  Meta Data: 
       -  `observedAt`: Ein Zeitstempel, welcher angibt, wann der Wert abgelesen wurde.
           -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
-  `trafficFlow`: Beobachteter Verkehrsfluss nach Fahrspur und Fahrzeugklassen im Beobachtungsintervall.
   -  Attribute type: **Property**. [Number](https://schema.org/Number)
   -  Optional
   -  Meta Data: 
       -  `observedAt`: Ein Zeitstempel, welcher angibt, wann der Wert abgelesen wurde.
           -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
       -  `vehicleType`: Fahrzeugklasse. Enum:'car-like, truck-like'. Erlaubte Werte: Werte gemäß: [TLS Anhang 2.2](https://www.bast.de/DE/Publikationen/Regelwerke/Verkehrstechnik/Unterseiten/V5-tls-2012.html)
           -  Attribute type: **Property**. [Text](https://schema.org/Text)
       -  `laneId`: Fahrspur-Bezeichner. Die Identifizierung der Fahrspuren erfolgt anhand der Konventionen der RoadSegment-Entität, die auf [OpenStreetMap] (http://wiki.openstreetmap.org/wiki/Forward_%26_backward,_left_%26_right) basieren.
           -  Attribute type: **Property**. [Number](https://schema.org/Number)
       -  `dateObservedFrom`: Datum und Uhrzeit vom Beginns des Beobachtungsintervalls
           -  Attribute type: **Property**. [Datetime](https://schema.org/Datetime)
       -  `dateObservedTo`: Datum und Uhrzeit vom Ende des Beobachtungsintervalls
           -  Attribute type: **Property**. [Datetime](https://schema.org/Datetime)
       -  `isMeasuredByDevice`: Property. Bezeichnungsformat der NGSI-Entität, welche das Gerät ist, welches die Messung zur Verfügung stellt.
           -  Attribute type: **Relationship**. 
       -  `datasetId`: Eindeutiger Bezeichner des Datasets
           -  Attribute type: **Property**. 
-  `isImpactedByRoadWork`: Wartungsmaßnahmen, welche das Straßensegment betreffen. Liste der Referenzen auf Entitäten des Typs RoadWork
   -  Attribute type: **Relationship**. [URL](https://schema.org/URL)
   -  Optional
   -  Meta Data: 
       -  `datasetId`: Eindeutiger Bezeichner des Datasets
           -  Attribute type: **Property**. 



# AirTemperatureSensor

Ein Gerät, das zur Messung der Lufttemperatur verwendet wird.
-  `category`: Sensor: Ein Gerät, das Ereignisse oder Veränderungen in der physikalischen Umgebung wie Licht, Bewegung oder Temperaturveränderungen erkennt und darauf reagiert. https://w3id.org/saref#Sensor. Actuator: Ein Gerät, das für die Bewegung oder Steuerung eines Mechanismus oder Systems verantwortlich ist. https://w3id.org/saref#Actuator
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Optional
-  `id`: Eindeutiger Bezeichner der Entität
   -  Attribute type: **Property**. 
   -  Required
-  `location`: Geojson-Referenz auf das Element. Kann Point, LineString, Polygon, MultiPoint, MultiLineString oderr MultiPolygon sein
   -  Attribute type: **Geoproperty**. 
   -  Optional
-  `controlledProperty`: Alles, was von einem Sensor erfasst, gemessen oder kontrolliert werden kann. Enum:''humidity, trafficFlow, airTemperature, surfaceTemperature, roadSurfaceCondition'
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Required
-  `controlledAsset`: Liste von Asset(s) (Gebäude, Objekt, etc.), welche vom Gerät kontrolliert werden.
   -  Attribute type: **Relationship**. [Text](https://schema.org/Text)
   -  Optional
   -  Meta Data: 
       -  `datasetId`: Eindeutiger Bezeichner des Datasets
           -  Attribute type: **Property**. 
-  `airTemperature`: Lufttemperatur
   -  Attribute type: **Property**. [Number](https://schema.org/Number)
   -  Required
   -  Meta Data: 
       -  `isMeasuredByDevice`: Property. Bezeichnungsformat der NGSI-Entität, welche das Gerät ist, welches die Messung zur Verfügung stellt.
           -  Attribute type: **Relationship**. 
       -  `observedAt`: Ein Zeitstempel, welcher angibt, wann der Wert abgelesen wurde.
           -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
       -  `unitCode`: Eine Zeichenfolge, welche die, der Messung entsprechenden, Maßeinheit darstellt. Sie ist unter Verwendung der UN/CEFACT Common Codes for Units of Measurement zu kodieren
           -  Attribute type: **Property**. [Text](https://schema.org/Text)
-  `type`: Typ der NGSI-Entität. Muss 'AirTemperatureSensor' sein. One of : `AirTemperatureSensor`.
   -  Attribute type: **Property**. 
   -  Required



# SurfaceTemperatureSensor

Ein Gerät zur Messung der Oberflächentemperatur.
-  `category`: Sensor: Ein Gerät, das Ereignisse oder Veränderungen in der physikalischen Umgebung wie Licht, Bewegung oder Temperaturveränderungen erkennt und darauf reagiert. https://w3id.org/saref#Sensor. Actuator: Ein Gerät, das für die Bewegung oder Steuerung eines Mechanismus oder Systems verantwortlich ist. https://w3id.org/saref#Actuator
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Optional
-  `id`: Eindeutiger Bezeichner der Entität
   -  Attribute type: **Property**. 
   -  Required
-  `location`: Geojson-Referenz auf das Element. Kann Point, LineString, Polygon, MultiPoint, MultiLineString oderr MultiPolygon sein
   -  Attribute type: **Geoproperty**. 
   -  Optional
-  `controlledProperty`: Alles, was von einem Sensor erfasst, gemessen oder kontrolliert werden kann. Enum:''humidity, trafficFlow, airTemperature, surfaceTemperature, roadSurfaceCondition'
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Required
-  `controlledAsset`: Liste von Asset(s) (Gebäude, Objekt, etc.), welche vom Gerät kontrolliert werden.
   -  Attribute type: **Relationship**. [Text](https://schema.org/Text)
   -  Optional
   -  Meta Data: 
       -  `datasetId`: Eindeutiger Bezeichner des Datasets
           -  Attribute type: **Property**. 
-  `surfaceTemperature`: Oberflächentemperatur
   -  Attribute type: **Property**. [Number](https://schema.org/Number)
   -  Required
   -  Meta Data: 
       -  `isMeasuredByDevice`: Property. Bezeichnungsformat der NGSI-Entität, welche das Gerät ist, welches die Messung zur Verfügung stellt.
           -  Attribute type: **Relationship**. 
       -  `observedAt`: Ein Zeitstempel, welcher angibt, wann der Wert abgelesen wurde.
           -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
       -  `unitCode`: Eine Zeichenfolge, welche die, der Messung entsprechenden, Maßeinheit darstellt. Sie ist unter Verwendung der UN/CEFACT Common Codes for Units of Measurement zu kodieren
           -  Attribute type: **Property**. [Text](https://schema.org/Text)
-  `type`: Typ der NGSI-Entität. Muss 'SurfaceTemperatureSensor' sein. One of : `SurfaceTemperatureSensor`.
   -  Attribute type: **Property**. 
   -  Required



# HumiditySensor

Ein Gerät zur Messung der relativen Luftfeuchtigkeit.
-  `category`: Sensor: Ein Gerät, das Ereignisse oder Veränderungen in der physikalischen Umgebung wie Licht, Bewegung oder Temperaturveränderungen erkennt und darauf reagiert. https://w3id.org/saref#Sensor. Actuator: Ein Gerät, das für die Bewegung oder Steuerung eines Mechanismus oder Systems verantwortlich ist. https://w3id.org/saref#Actuator
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Optional
-  `id`: Eindeutiger Bezeichner der Entität
   -  Attribute type: **Property**. 
   -  Required
-  `location`: Geojson-Referenz auf das Element. Kann Point, LineString, Polygon, MultiPoint, MultiLineString oderr MultiPolygon sein
   -  Attribute type: **Geoproperty**. 
   -  Optional
-  `controlledProperty`: Alles, was von einem Sensor erfasst, gemessen oder kontrolliert werden kann. Enum:''humidity, trafficFlow, airTemperature, surfaceTemperature, roadSurfaceCondition'
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Required
-  `controlledAsset`: Liste von Asset(s) (Gebäude, Objekt, etc.), welche vom Gerät kontrolliert werden.
   -  Attribute type: **Relationship**. [Text](https://schema.org/Text)
   -  Optional
   -  Meta Data: 
       -  `datasetId`: Eindeutiger Bezeichner des Datasets
           -  Attribute type: **Property**. 
-  `humidity`: Relative Luftfeuchtigkeit
   -  Attribute type: **Property**. [Number](https://schema.org/Number)
   -  Required
   -  Meta Data: 
       -  `isMeasuredByDevice`: Property. Bezeichnungsformat der NGSI-Entität, welche das Gerät ist, welches die Messung zur Verfügung stellt.
           -  Attribute type: **Relationship**. 
       -  `observedAt`: Ein Zeitstempel, welcher angibt, wann der Wert abgelesen wurde.
           -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
       -  `unitCode`: Eine Zeichenfolge, welche die, der Messung entsprechenden, Maßeinheit darstellt. Sie ist unter Verwendung der UN/CEFACT Common Codes for Units of Measurement zu kodieren
           -  Attribute type: **Property**. [Text](https://schema.org/Text)
-  `type`: Typ der NGSI-Entität. Muss 'HumiditySensor' sein. One of : `HumiditySensor`.
   -  Attribute type: **Property**. 
   -  Required



# RoadSurfaceConditionSensor

Ein Gerät, um den Fahrbahnoberflächenzustand zu bestimmen.
-  `category`: Sensor: Ein Gerät, das Ereignisse oder Veränderungen in der physikalischen Umgebung wie Licht, Bewegung oder Temperaturveränderungen erkennt und darauf reagiert. https://w3id.org/saref#Sensor. Actuator: Ein Gerät, das für die Bewegung oder Steuerung eines Mechanismus oder Systems verantwortlich ist. https://w3id.org/saref#Actuator
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Optional
-  `id`: Eindeutiger Bezeichner der Entität
   -  Attribute type: **Property**. 
   -  Required
-  `location`: Geojson-Referenz auf das Element. Kann Point, LineString, Polygon, MultiPoint, MultiLineString oderr MultiPolygon sein
   -  Attribute type: **Geoproperty**. 
   -  Optional
-  `controlledProperty`: Alles, was von einem Sensor erfasst, gemessen oder kontrolliert werden kann. Enum:''humidity, trafficFlow, airTemperature, surfaceTemperature, roadSurfaceCondition'
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Required
-  `controlledAsset`: Liste von Asset(s) (Gebäude, Objekt, etc.), welche vom Gerät kontrolliert werden.
   -  Attribute type: **Relationship**. [Text](https://schema.org/Text)
   -  Optional
   -  Meta Data: 
       -  `datasetId`: Eindeutiger Bezeichner des Datasets
           -  Attribute type: **Property**. 
-  `roadSurfaceCondition`: Oberflächenzustand einer Straße. Enum:'dry, dampOrWet, frozen'.  Erlaubte Werte: Werte in Anlehnung an [TLS DE-Typ 70 (0, 32, 64)](https://www.bast.de/DE/Publikationen/Regelwerke/Verkehrstechnik/Unterseiten/V5-tls-2012.html).. One of : `dry`, `dampOrWet`, `frozen`.
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Required
   -  Meta Data: 
       -  `isMeasuredByDevice`: Property. Bezeichnungsformat der NGSI-Entität, welche das Gerät ist, welches die Messung zur Verfügung stellt.
           -  Attribute type: **Relationship**. 
       -  `observedAt`: Ein Zeitstempel, welcher angibt, wann der Wert abgelesen wurde.
           -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
-  `type`: Typ der NGSI-Entität. Muss 'RoadSurfaceConditionSensor' sein. One of : `RoadSurfaceConditionSensor`.
   -  Attribute type: **Property**. 
   -  Required



# TrafficFlowSensor

Ein Gerät zur Messung des Verkehrsflusses.
-  `category`: Sensor: Ein Gerät, das Ereignisse oder Veränderungen in der physikalischen Umgebung wie Licht, Bewegung oder Temperaturveränderungen erkennt und darauf reagiert. https://w3id.org/saref#Sensor. Actuator: Ein Gerät, das für die Bewegung oder Steuerung eines Mechanismus oder Systems verantwortlich ist. https://w3id.org/saref#Actuator
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Optional
-  `id`: Eindeutiger Bezeichner der Entität
   -  Attribute type: **Property**. 
   -  Required
-  `location`: Geojson-Referenz auf das Element. Kann Point, LineString, Polygon, MultiPoint, MultiLineString oderr MultiPolygon sein
   -  Attribute type: **Geoproperty**. 
   -  Optional
-  `controlledProperty`: Alles, was von einem Sensor erfasst, gemessen oder kontrolliert werden kann. Enum:''humidity, trafficFlow, airTemperature, surfaceTemperature, roadSurfaceCondition'
   -  Attribute type: **Property**. [Text](https://schema.org/Text)
   -  Required
-  `controlledAsset`: Liste von Asset(s) (Gebäude, Objekt, etc.), welche vom Gerät kontrolliert werden.
   -  Attribute type: **Relationship**. [Text](https://schema.org/Text)
   -  Optional
   -  Meta Data: 
       -  `datasetId`: Eindeutiger Bezeichner des Datasets
           -  Attribute type: **Property**. 
-  `trafficFlow`: Beobachteter Verkehrsfluss nach Fahrspur und Fahrzeugklassen im Beobachtungsintervall.
   -  Attribute type: **Property**. [Number](https://schema.org/Number)
   -  Required
   -  Meta Data: 
       -  `observedAt`: Ein Zeitstempel, welcher angibt, wann der Wert abgelesen wurde.
           -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
       -  `vehicleType`: Fahrzeugklasse. Enum:'car-like, truck-like'. Erlaubte Werte: Werte gemäß: [TLS Anhang 2.2](https://www.bast.de/DE/Publikationen/Regelwerke/Verkehrstechnik/Unterseiten/V5-tls-2012.html)
           -  Attribute type: **Property**. [Text](https://schema.org/Text)
       -  `laneId`: Fahrspur-Bezeichner. Die Identifizierung der Fahrspuren erfolgt anhand der Konventionen der RoadSegment-Entität, die auf [OpenStreetMap] (http://wiki.openstreetmap.org/wiki/Forward_%26_backward,_left_%26_right) basieren.
           -  Attribute type: **Property**. [Number](https://schema.org/Number)
       -  `dateObservedFrom`: Datum und Uhrzeit vom Beginns des Beobachtungsintervalls
           -  Attribute type: **Property**. [Datetime](https://schema.org/Datetime)
       -  `dateObservedTo`: Datum und Uhrzeit vom Ende des Beobachtungsintervalls
           -  Attribute type: **Property**. [Datetime](https://schema.org/Datetime)
       -  `isMeasuredByDevice`: Property. Bezeichnungsformat der NGSI-Entität, welche das Gerät ist, welches die Messung zur Verfügung stellt.
           -  Attribute type: **Relationship**. 
       -  `datasetId`: Eindeutiger Bezeichner des Datasets
           -  Attribute type: **Property**. 
-  `updateInterval`: Aktualisierungsintervall der Messwerte
   -  Attribute type: **Property**. 
   -  Optional
-  `type`: Typ der NGSI-Entität. Muss 'TrafficFlowSensor' sein. One of : `TrafficFlowSensor`.
   -  Attribute type: **Property**. 
   -  Required



# RoadWork

Baumaßnahme, welche eine Straße betrifft
-  `endDate`: Enddatum und -uhrzeit der Arbeiten im ISO8601 UTC-Format. Das Attribut kann zusätzlich zum Attribut `workDate` verwendet werden, wenn es einem hervorzuhebenden Zeitintervall entspricht
   -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
   -  Optional
-  `startDate`: Datum und Uhrzeit des Beginns der Arbeiten im Format ISO8601 UTC. Das Attribut kann zusätzlich zum Attribut `workDate` verwendet werden, wenn es einem hervorzuhebenden Zeitintervall entspricht
   -  Attribute type: **Property**. [DateTime](https://schema.org/DateTime)
   -  Optional
-  `location`: Geojson-Referenz auf das Element. Kann Point, LineString, Polygon, MultiPoint, MultiLineString oder MultiPolygon sein
   -  Attribute type: **Geoproperty**. 
   -  Required
-  `impactsRoadSegment`: Straßensegmente, welche von Wartungsmaßnahme betroffen sind. Liste der Referenzen auf Entitäten des Typs RoadSegment
   -  Attribute type: **Relationship**. [URL](https://schema.org/URL)
   -  Optional
   -  Meta Data: 
       -  `datasetId`: Eindeutiger Bezeichner des Datasets
           -  Attribute type: **Property**. 
-  `type`: Typ der NGSI-Entität. Muss 'RoadWork' sein. One of : `RoadWork`.
   -  Attribute type: **Property**. 
   -  Required
-  `workNature`: Grund der Arbeiten. Eine Kombination aus diesen Werten. Enum:'maintenance, rehabilitation, crackSealing, patchPotHoles'
   -  Attribute type: **Property**. 
   -  Optional


