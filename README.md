# EventSub
EventSub is a toolkit to understand, document and implement sending of data to any event-based analytics.

# Core concepts
The main idea of EventSub is to develop an universal instrument for developers, product managers and analytics. It's like Swagger™ or WSDL for an event-based analytics.

## Module
Module is logical parts of your application. A name of each event inside a module will be prefixed with a name of the module.

A name of a module is usually a noun.

Examples: `Checkout`, `Signup`, `Onboarding_Step_1`, `Product_Card`.

### Module properties
Each module has it's own set of module properties and each event inside the module must contain all of the required module properties and may contain any of the optional module properties. Module properties can be required or optional.

If a module property is required any event within module can't be sent without the property.

Examples: `Source_Module`, `Cart_Price`.

## Events
Events are used to show actions of your users.

A name of an event is usually a verb.

Examples: `Clicked`, `Purchased`, `Appeared`.

### Event properties
Event properties are attributes of events and reflect the state at which the event was triggered. Use these if you want to better understand characteristics of a given event. Event properties can be required or optional.

If an event property is required the event can't be sent without the property.

Examples: `Product_Type`, `Is_First_Item_In_Cart`.

## User properties
User Properties are attributes of users and reflect the current state of the user. Use these if you want to segment your users based on these properties. All of users properties is optional because they can be sent at any time in user lifecycle.

Examples: `User_Type`, `Is_Registered`, `Marketting_Channel`.

## Properties
Properties are attributes of events or users.

Each property must have its own type from the list below:
- `String` ("Ivan", "Marketing Channel")
- `Integer` (10, 12, 44)
- `Decimal` (10.00, 11.2029, 33.222)
- `Enum` - you can specify list of possible values for this type (`dog`, `cat`, `bird`) 

# Architecture
EventSub has two main parts:
1. Visual viwer and editor to build an `esjson` file describing all modules, events and properties withing your app
2. Codegen tool to create analytics layer code for developers

# Supported platforms
We have only the readme now :)
