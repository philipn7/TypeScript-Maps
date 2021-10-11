# Maps Application with TypeScript
Map application that generates random users and company locations to be displayed on a browser page map. As part of the 'Typescript: The Complete Developer's guide' course.

## Parcel-bundle
This app uses parcel to compile ts into html. Browsers don't run typescript so parcel is an easy way to bridge that gap.

`parcel index.html` will parse the TypeScript file into JavaScript and inject it script into index.html

## Generate Fake User Data
faker.js is an API used to randomly generate a multitude of user data.


## Google Maps Implementation
- Generate Google Maps API key and insert into index.ts above the typescript injection:
`<script src="https://maps.googleapis.com/maps/api/js?key=AIzaSyDt4-oslXPl_FhghuEIsqIXrW2RULCgu7E"></script>
<script src="./src/index.ts"></script>`
- There is a global variable called 'google' but we can't access it until we give typescript its definition. `npm install @types/google.maps`
- The first line in index.ts should have this directive: `/// <reference types="@types/google.maps" />`

## Hiding Functionality
Now that we have the 'google' object, another person working on this project can call any google map method. This can break our app so how do we hide these extra methods?

Create a custom map object with only the things we need exposed. Google map object is set to private. Access / modifier methods created as needed.

## Interfaces in Patterns
Interfaces definitions are a large part of TypeScript. If a method needs to receive an object type to work correctly we define that type with interfaces. The object we pass can also `implements` the interface so typescript and other developers know our intentions.