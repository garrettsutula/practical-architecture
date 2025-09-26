# practical-architecture
Minimalistic set of diagrams &amp; documentation to understand a software system. Examples and succinct explanation of why they are important/helpful.

# Use Case Diagram
The point of this diagram is to understand the things that users can do in the application.

This should only contain information from the user's perspective, never technical details.

![](./out/diagrams/Use%20Case%20Diagram.svg)

# Logical Component Diagram
The point of this diagram is to understand all the individual components that make a system work, including any dependencies (internal and 3rd party).

![](./out/diagrams/Logical%20Diagram.svg)

# Deployment Diagram
The point of this diagram is to understand how the components in the logical component diagram are deployed into the environment (e.g. datacenter, cloud provider) and how those infrastructure resources work together.

![](./out/diagrams/Deployment%20Diagram.svg)

## Data Model
The point of this diagram is to understand the logical data structure and the data types/entities, and the relationships between different data types that are stored in the database.

This data model **SHOULD NOT** document the structure of the database, instead it should describe the higher level data types in the database.

![](./out/diagrams/Data%20Model.svg)

## Data Schemas
The point of this documentation is to understand exactly what data is stored for each data type.

With this information, you could plan to export the data into a different system (e.g. for reporting) or how you may integrate another application to create (or import) data into this system.

There are many different ways this can be expressed but at the least the documentation **must contain the name of eveny data element and its type**. Length, formatting, and other constraints are helpful. Examples are helpful.

[JSON Schema](https://json-schema.org) is a great format for this information.

```
class Customer {
  firstName: string;
  lastName: string;
  emailAddress: string;
  phoneNumber: string;
  address1: string;
  address2: string;
  city: string;
  state: string;
  postalCode: string;
}
```

# API Specification
For applciations that provide APIs called by one or more client apps or third parties, the API specification in a standardized format (e.g. OpenAPI, WSDL, SDL, Protobuf, etc.)

[API Spec Example](https://petstore3.swagger.io)