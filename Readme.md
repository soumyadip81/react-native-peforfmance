These are the 4 different versions along with which folder the code is under:

- Version 1 (Repo Name: oldVer): Same code as original repo in the study with any changes to make sure that code can run on a local device

- Version 2 (Repo Name: oldVerModern): Code for old architecture but with modern coding standards and dependencies

Changes made to version 2:
- Updated coding style and structure
- Split code into different components
- Got rid of classes and modified them to functional components
- State removed in CustomRow function, since there is no need to have states and the props can directly be used instead
- ComponenDidMount() and constructor removed. UseEffect used instead
- Props removed and destructuring used instead

- Version 3 (Repo Name: newArchitecture): Version 2 code, which is in JavaScript, but using the new architecture (the file extension is .tsx but is JavaScript code)

- Version 4(Repo Name: newArchitectureTS): Version 3 code, but in TypeScript

Version 4 is not final yet, because I may not have covered everything needed to migrate JavaScript code into TypeScript. If anyone has any input or suggestions on improving the TypeScript code please let me know or feel free to clone the repo and commit/push any modifications.

This is the link I used as reference to familiarize myself with modifying my JavaScript code to TypeScript, which may be useful to anyone who wants to help with modifying version 4:
https://www.typescriptlang.org/docs/handbook/migrating-from-javascript.html
Essentially, add a type to any variable(similar to how we declare a type in C++). Also for objects, create an interface with the types for the attributes
Example:
C++ -> int age = 18;
TypeScript -> let age:number = 18;
JavaScript -> let age = 18;
In cases of complex code which may have complicated types, use “any” as a temporary type and then come up with the specific type later.

I am not sure if the code will run on someone else’s local computer right away even though the dependency list should be updated in the repo. If the code doesn’t run, use the following links to setup any of your personal devices:
Version 1 and 2: https://reactnative.dev/docs/environment-setup
Version 3 and 4: https://reactnative.dev/docs/the-new-architecture/use-app-template
Skip the “create a new application” section and start from the next section. 

Lastly, some of you make get an error along the lines of “fast image not installed”. If that error is displayed, follow the instruction in https://www.npmjs.com/package/react-native-fast-image
Make sure to use the appropriate command. If you are using npx instead of yarn, use npx. Once the installation is complete, terminate the mobile app and rebuild it(the changes will not show unless you shutdown the app first and restart it — I learnt this the hard away).

