# Building Space and Activity Classification System

## Overview
This classification system provides a standardized way to categorize building spaces based on their activities and functions. It is designed to be used with Building Information Modeling (BIM) and is compatible with the buildingSMART Data Dictionary (bsDD).

🔗 [View on bsDD](https://search.bsdd.buildingsmart.org/uri/abstract/BuildingSpaceActivityClassification)

### Why This Classification System?

The building industry faces several challenges with existing space classification systems:

1. **Country-Specific Limitations**
   - Different countries use their own classification standards (e.g., Uniclass, OmniClass, DIN)
   - This makes international collaboration and comparison difficult
   - Cross-border projects require complex mapping between systems

2. **Need for Abstraction**
   - Existing systems often mix function, form, and construction methods
   - This makes it hard to compare spaces purely based on their purpose
   - Analytics and benchmarking across different building types becomes complicated

3. **Digital Transformation**
   - Modern BIM workflows need classification systems that support:
     - Data-driven design decisions
     - Space programming automation
     - Performance benchmarking
     - AI and machine learning applications

This classification system addresses these challenges by:

- **Providing a Universal Language**: Acts as a neutral, country-independent reference system that can map to local standards
- **Focusing on Activities**: Classifies spaces by their primary function and activities, independent of construction methods
- **Supporting Analysis**: Enables meaningful comparison and benchmarking across different projects, regions, and building types
- **Enabling abstractBIM**: Facilitates early-stage planning and analysis before detailed design decisions are made

### Key Benefits

1. **Cross-Project Comparison**
   - Benchmark spaces across different buildings
   - Compare efficiency metrics internationally
   - Analyze space utilization patterns

2. **Mapping Capabilities**
   - Map local classification systems to a common reference
   - Transform between different standards
   - Maintain compliance with local codes while enabling global collaboration

3. **Abstract Analysis**
   - Perform space programming studies
   - Analyze functional relationships
   - Optimize space utilization
   - Support early-stage decision making

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