# AECO Markdown
Nothing real yet, but AECO markdown would be an Extention on existing Markdown to hold AECO specific datasets and allow them to live next to documentation, instructions etc.

## Example Usage

### Project Location Capture in GeoJson  (View me in Github)

```geojson
// ProjectLocation
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