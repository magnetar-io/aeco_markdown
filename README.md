# AECO Markdown
Nothing real yet, but AECO markdown would be an Extention on existing Markdown to hold AECO specific datasets and allow them to live next to documentation, instructions etc.

## Example Usage

### Project Location Capture in GeoJson  (View me in Github)

```geojson
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": {},
      "geometry": {
        "coordinates": [
          [
            [
              -74.02114659009447,
              40.68635139741832
            ],
            [
              -74.02196289915616,
              40.685885908758536
            ],
            [
              -74.02114985533024,
              40.685138148893
            ],
            [
              -74.02024865012578,
              40.685566502425104
            ],
            [
              -74.02114659009447,
              40.68635139741832
            ]
          ]
        ],
        "type": "Polygon"
      }
    }
  ]
}
```
### Project Details to Extract when setting up web services

```json
// ProjectData
{
  "Name": "Project Alpha",
  "Number": 12345,
  "ShortName": "PA",
  "ThreeWordCode": "AlphaBetaGamma",
  "GUID": "123e4567-e89b-12d3-a456-426614174000"
}
```

### What ACC/360 Template Should be used when setting up the project

And even a narrative about why this content should be used.  Maybe even a link to help documents and videos

```json
// Template_ACC
{
  "Template": //TemplateName
}
```

### Which Revit Template or Project File should be the basis of the project

```json
// Template_Revit
{
  "Content": "MyRevitTemplate.rvt"
}
```

### Content that should be loaded into the project

```json
// ContentPackages
{
  "Content": ["Content1", "Content2"]
}
```

### Which Companies are responsible for which disciplines

```json
// Company_Dicipline
{
  "DisciplineByCompany": [
    {
      "Company": "Company1",
      "Discipline": "Architecture"
    },
    {
      "Company": "Company2",
      "Discipline": ["Structure", "MEP"]
    }
  ]
}
```

### Revit Workset Rules
```json
// Revit_Workset_Rules
{
  "worksetMapping": {
    "Architectural": {
      "categories": [
        "Walls",
        "Floors",
        "Ceilings",
        "Doors",
        "Windows",
        "Furniture",
        "Curtain Walls",
        "Curtain Panels",
        "Curtain Wall Mullions",
        "Stairs",
        "Railings",
        "Ramps",
        "Casework"
      ]
    },
    "Structural": {
      "categories": [
        "Columns",
        "Structural Framing",
        "Structural Foundations",
        "Structural Columns",
        "Structural Beams",
        "Structural Braces",
        "Structural Connections"
      ]
    },
    "MEP": {
      "categories": [
        "Plumbing Fixtures",
        "Lighting Fixtures",
        "Air Terminals",
        "Ducts",
        "Pipes",
        "Electrical Equipment"
      ]
    },
    "Landscape": {
      "categories": [
        "Planting",
        "Parking",
        "Roads",
        "Site",
        "Topography"
      ]
    },
    "Specialty_Equipment": {
      "categories": [
        "Specialty Equipment"
      ]
    },
    "Revit_Links": {
      "pattern": "<name> Link"
    }
  }
}
```

### Standard Room Names in Revit
```json
// Category:Room:Names
{
  "hospitalRooms": [
    {
      "name": "Patient Room",
      "description": "A private or semi-private room for patient care and recovery."
    },
    {
      "name": "Operating Room",
      "description": "A sterile environment equipped for surgical procedures."
    },
    {
      "name": "Intensive Care Unit (ICU)",
      "description": "A specialized department for critically ill patients requiring intensive care and monitoring."
    },
    {
      "name": "Emergency Department",
      "description": "A department equipped to handle urgent and emergency medical situations."
    },
    {
      "name": "Radiology Department",
      "description": "A department for imaging services such as X-rays, MRIs, and CT scans."
    },
    {
      "name": "Laboratory",
      "description": "A department for medical testing and analysis."
    },
    {
      "name": "Pharmacy",
      "description": "A department for dispensing and managing medications."
    },
    {
      "name": "Maternity Ward",
      "description": "A specialized ward for childbirth and newborn care."
    },
    {
      "name": "Pediatric Ward",
      "description": "A ward dedicated to the care of children and adolescents."
    },
    {
      "name": "Rehabilitation Unit",
      "description": "A unit specialized in physical, occupational, and speech therapy."
    },
    {
      "name": "Psychiatric Ward",
      "description": "A ward for patients with mental health conditions."
    },
    {
      "name": "Cafeteria",
      "description": "A dining area for patients, staff, and visitors."
    },
    {
      "name": "Waiting Room",
      "description": "An area for patients and visitors to wait for appointments or information."
    },
    {
      "name": "Staff Lounge",
      "description": "A relaxation area for hospital staff."
    },
    {
      "name": "Conference Room",
      "description": "A room for meetings and educational sessions."
    }
  ]
}
```