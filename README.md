# AECO Markdown
Nothing real yet, but AECO markdown would be an Extention on existing Markdown to hold AECO specific datasets and allow them to live next to documentation, instructions etc.

## It would be pared with and editor that made maintaining and using it simple. 

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
### Program Rooms

```topojson
{
  "type": "Topology",
  "objects": {
    "rooms": {
      "type": "GeometryCollection",
      "geometries": [
        {
          "type": "Polygon",
          "properties": {
            "name": "Living Room"
          },
          "coordinates": [[[0, 0], [0, 5], [5, 5], [5, 0], [0, 0]]]
        },
        {
          "type": "Polygon",
          "properties": {
            "name": "Kitchen"
          },
          "coordinates": [[[5, 0], [5, 3], [8, 3], [8, 0], [5, 0]]]
        },
        {
          "type": "Polygon",
          "properties": {
            "name": "Bedroom"
          },
          "coordinates": [[[0, 5], [0, 8], [5, 8], [5, 5], [0, 5]]]
        },
        {
          "type": "Polygon",
          "properties": {
            "name": "Bathroom"
          },
          "coordinates": [[[5, 5], [5, 8], [8, 8], [8, 5], [5, 5]]]
        }
      ]
    }
  }
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
  "Rooms:Hospitals:General": [
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

### Specifications
```html
// Category:Room:Names


<!DOCTYPE html>
<html>
<head>
    <title>Concrete Floors Specification</title>
    <style>
        .section-title {
            font-weight: bold;
            text-decoration: underline;
        }
        .subsection {
            margin-left: 20px;
        }
    </style>
</head>
<body>
    <h1>Concrete Floors Specification</h1>

    <div class="section">
        <div class="section-title">Part 1: General</div>
        <div class="subsection">
            <h2>1.1 Summary</h2>
            <ul>
                <li>This section includes specifications for cast-in-place concrete floors.</li>
                <li>Related Sections:
                    <ul>
                        <li>Section 03300 - Cast-in-Place Concrete.</li>
                        <li>Section 03200 - Concrete Reinforcement.</li>
                    </ul>
                </li>
            </ul>

            <h2>1.2 Submittals</h2>
            <ul>
                <li>Submit mix designs for each type of concrete floor.</li>
                <li>Submit product data for curing compounds, sealers, and other materials.</li>
            </ul>
        </div>
    </div>

    <div class="section">
        <div class="section-title">Part 2: Products</div>
        <div class="subsection">
            <h2>2.1 Materials</h2>
            <ul>
                <li>Cement: Portland cement conforming to ASTM C150, Type <span class="choice">I</span>/<span class="choice">II</span>.</li>
                <li>Aggregates: Coarse and fine aggregates conforming to ASTM C33.</li>
                <li>Water: Clean, potable, and free from deleterious materials.</li>
            </ul>

            <h2>2.2 Admixtures</h2>
            <ul>
                <li>Air-entraining admixture: Conforming to ASTM C260.</li>
                <li>Water-reducing admixture: Conforming to ASTM C494, Type <span class="choice">A</span>.</li>
            </ul>

            <h2>2.3 Finishes</h2>
            <ul>
                <li>Trowel finish for indoor floors.</li>
                <li>Broom finish for outdoor or slip-resistant surfaces.</li>
            </ul>
        </div>
    </div>

    <div class="section">
        <div class="section-title">Part 3: Execution</div>
        <div class="subsection">
            <h2>3.1 Preparation</h2>
            <ul>
                <li>Prepare subgrade according to Section 02200 - Earthwork.</li>
                <li>Install vapor barriers and insulation as specified.</li>
            </ul>

            <h2>3.2 Placement</h2>
            <ul>
                <li>Mix and place concrete according to ASTM C94 and ACI 301.</li>
                <li>Consolidate concrete with mechanical vibrators to eliminate voids.</li>
            </ul>

            <h2>3.3 Finishing</h2>
            <ul>
                <li>Finish surfaces to the specified texture and flatness.</li>
                <li>Cure concrete according to ASTM C curing compounds.</li>
            </ul>

            <h2>3.4 Protection</h2>
            <ul>
                <li>Protect freshly placed concrete from premature drying and excessive cold or heat.</li>
                <li>Restrict traffic on new floors for at least 7 days.</li>
            </ul>
        </div>
    </div>

</body>
</html>

```
### Embed Analysis 

![exmaple Analysis Image](https://github.com/magnetar-io/aeco_markdown/blob/main/Framework.png)


