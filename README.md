## UAS Data Specification

The following provides the fields for the UAS data types. All data needs to be in JSON with location data encoded in [GEOJSON](http://geojson.org/). 

### UAS Data Types
The fields marked with an asterisk are already populated when you create the data source for your drone in stae. 

| Field | Data type | Description | Validation
| ---   | --- 		| ---         | ---
|id*    | Text      | Represents an unmanned aircraft system (UAV/UAS/Drone). | Not empty
|name*  | Text      | Descriptive name given to the UAS by the operator. | Not empty
|type   | Text      | Categorization of the UAS. |  Not empty, max character length: 2048
|notes* | Text 		| Description or further notes about the UAS. | Not empty
|manufacturer| Text | Make/manufacturer of the UAS | Not empty, max character length: 2048 
|model  | Text 		| Model of the UAS. | Not empty, max character length: 2048
|color  | Text 		| Color of the UAS exterior. | Not empty, max character length: 2048
|operators| Array 	| List of agencies of people responsible for the UAS. | Not empty, max character length: 2048
|active | Boolean 	| True/false if the UAS is currently in service. | -
|heading | Number 	| Direction the UAS is pointing | Min: 0, Max: 360
|speed 	| Number (KM/H) | Speed the UAS is currently going. | Min: 0, Max: 1000
|tripId | Text 		| Unique ID for the current trip the UAS is on. | Not empty, max character length: 2048 
|stream | Text 		| URL of the live video feed for the camera. | Not empty, max character length: 2048, stream URL exists
|images | Array 	| List of images related to the UAS | Not empty, max character length: 2048
|location | Point 	| Location where the UAS exists. | GEOJSON format
