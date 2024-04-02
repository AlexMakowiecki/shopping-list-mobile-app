# Shopping List Mobile App
## What is it? 
It's a website that let you add shopping products to a list, that is connected to a Firebase database. This website also use app manifest to look like an app on phones. 
It's also the seventh project, part of the Scrimba Course, that I've uploaded to Github. This project is part of module 3, where they teach you how to use Javascript.
## What did I use?
I used HTML, CSS, Javascript, Firebase, manifest.json, and multiple types of images.
## Concepts learned for this project and practiced during it
- **import** statement, to import function into your code.
  - ```Javascript
      import { functionName } from "route"
    ```
- **__FireBase__**: A service provided by Google to create and manage databases in a more friendly way.
  - **initializeApp()** to get started with FireBase. Connect with a URL passed as an argument.
    - ```Javascript
        initializeApp( { databaseURL: "databaseURL" } )
      ```
  - **getDatabase()** to connect with the database. You have to pass the variable where you stored de initializeApp() result.
    - ```Javascript
        getDatabase( initializeAppObject )
      ```
  - **ref()** to reference (connect to) a value inside the database. You have to pass the variable where you stored the getDatabase() result and the name of the reference.
    - ```Javascript
        ref( getDatabaseObject, "referenceName" )
      ```
  - **push()** to send a value to store in the database. You have to pass the variable where you stored the ref() result and the value.
    - ```Javascript
        push( refObject, value )
      ```
  - **onValue()** to listen to changes in the database, and call a function when the changes occur. You have to pass the variable where you stored the ref() result and the function, with a parameter, that will be called.
    - ```Javascript
        onValue( refObject, function( parameter ){ console.log( parameter ) }) 
      ```
  - **snapshot:** the parameter of the onValue() function, and the information that the database sends to us.
    - `snapshot.val():` the content of the reference, stored as an object. Here are stored the values and the IDs associated with them. 
    - `snapshot.exist():` to know if a reference exists (has values stored inside) or not
  - **ID:** a random string sequence associated with the values stored in the database
  - **remove()** to remove elements of the database. You have to pass the exact location of the element 
    - ```Javascript
        remove( ref( getDatabaseObject, "containerName/itemID") )
      ```
  
## Preview 
<img style="text-align:center" src="https://github.com/AlexMakowiecki/unit-converter/assets/122258496/b850091f-3650-4658-aeff-b1c18d2847a7" width="500"/> 

## About Scrimba

At Scrimba our goal is to create the best possible coding school at the cost of a gym membership! 💜
If we succeed with this, it will give anyone who wants to become a software developer a realistic shot at succeeding, regardless of where they live and the size of their wallets 🎉
The Frontend Developer Career Path aims to teach you everything you need to become a Junior Developer, or you could take a deep-dive with one of our advanced courses 🚀

- [Our courses](https://scrimba.com/allcourses)
- [The Frontend Career Path](https://scrimba.com/learn/frontend)
- [Become a Scrimba Pro member](https://scrimba.com/pricing)

Happy Coding!
