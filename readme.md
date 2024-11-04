# Building Space and Activity Classification System

## Overview
This classification system provides a standardized way to categorize building spaces based on their activities and functions. It is designed to be used with Building Information Modeling (BIM) and is compatible with the buildingSMART Data Dictionary (bsDD).

🔗 [View on bsDD](https://search.bsdd.buildingsmart.org/uri/abstract/BuildingSpaceActivityClassification)

## Classification Structure

The system is organized into three main categories:

### M - Main Activity Spaces
Primary spaces that serve the building's core functions:
- M-RES: Residential Spaces
- M-WRK: Work Spaces
- M-LRN: Learning Spaces
- M-COM: Commercial Spaces
- M-HEL: Healthcare Spaces
- M-CIR: Main Activity Circulation (e.g., museum galleries, mall concourses)

### S - Support Spaces
Auxiliary spaces that enable building operations:
- S-CIR: Support Circulation (service corridors, fire exits)
- S-TEC: Technical Spaces
- S-PRK: Parking Spaces
- S-VOI: Void Spaces (including multistory voids)

### O - Outdoor Spaces
External spaces associated with the building:
- O-GRN: Green Spaces (recreational, sports, gardens)
- O-CIR: Outdoor Circulation (roads, pedestrian paths)

## Usage

### IFC Integration
The classification system is designed to work with IFC entities:
- Indoor spaces map to `IfcSpace.INTERNAL`
- Outdoor spaces map to `IfcSpace.EXTERNAL`

### Implementation Example
```json
{
  "space": {
    "classificationReference": {
      "system": "abstract/BuildingSpaceActivityClassification",
      "code": "M-WRK"
    }
  }
}
```

## File Structure

- `BuildingSpaceActivityClassification.json` - Main classification file
- Follows bSDD schema format
- Includes class codes, definitions, descriptions, and hierarchical relationships

## Key Features

1. **Hierarchical Organization**
   - Three-level classification system
   - Clear parent-child relationships
   - Logical grouping of related spaces

2. **Comprehensive Coverage**
   - Main functional spaces
   - Support and service areas
   - Circulation spaces at different levels
   - Outdoor and site elements

3. **Flexible Application**
   - Suitable for different building types
   - Adaptable to various project scales
   - Compatible with BIM workflows

## Licence
- License: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

## Contributing

We welcome contributions to improve and expand this classification system. Please:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request with your changes

## License

This work is licensed under Creative Commons Attribution 4.0 International License (CC BY 4.0). You are free to:
- Share: Copy and redistribute the material in any medium or format
- Adapt: Remix, transform, and build upon the material for any purpose

Subject to attribution requirements.