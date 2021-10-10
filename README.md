# Maps Application with TypeScript
Map application that generates random users and company locations to be displayed on a browser page map. As part of the 'Typescript: The Complete Developer's guide' course.

## Parcel-bundle
This app uses parcel to compile ts into html. Browsers don't run typescript so parcel is an easy way to bridge that gap.

`parcel index.html` will parse the ts file into JavaScript and inject the new js script into index.html

## Generate Fake User Data
faker.js is an API used to randomly generate a multitude of user data.


## Google Maps Implementation
- Generate Google Maps API key and insert into index.ts above the typescript injection:
`<script src="https://maps.googleapis.com/maps/api/js?key=AIzaSyDt4-oslXPl_FhghuEIsqIXrW2RULCgu7E"></script>
<script src="./src/index.ts"></script>`
- There is a global variable called 'google' but we can't access it until we give typescript its definition. `npm install @types/google.maps`
- The first line in index.ts should have this directive: `/// <reference types="@types/google.maps" />`



