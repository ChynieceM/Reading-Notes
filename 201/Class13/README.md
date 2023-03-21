1. Why would a developer use local storage for a web application?

The main issue with HTTP as the main transport layer of the Web is that it is **stateless**. So when you open and close an application, it will reset the next time you open it. If you close an application on your desktop and re-open it, its most recent state is restored. 

2. What information should not be stored in local storage?

Personal information, passwords, bank information etc. 


3. Local storage can store what type of data? How would you convert it to that type before storing?

Local storage can only store strings in different keys which means when you have an object, it will not be stored the correct way. 

You can use `JSON.stringify()` and `JSON.parse` methods.

JSON is a way to store data that looks like a JavaScript object. - portable object;interchangable b/w most systems. 