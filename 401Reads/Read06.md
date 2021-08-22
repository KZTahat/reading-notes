# Read 06
## Authentication

1. Explain what a “Singleton” is (in Computer Science terms)<br />
    In software engineering, the singleton pattern is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system. The term comes from the mathematical concept of a singleton.<br />

2. Explain how the Singleton pattern can be used with Node modules, specifically with classes<br />

    we can use singletone in classess by refactoring our class to have:
    - hidden (private)constructor.
    - public getInstance method that returns instance of the class.

    ```
    class PrivateSingleton {
        constructor() {
            this.message = 'I am an instance';
        }
    }

    class Singleton {
        constructor() {
            throw new Error('Use Singleton.getInstance()');
        }

        static getInstance() {
            if (!Singleton.instance) {
                Singleton.instance = new PrivateSingleton();
            }
            return Singleton.instance;
        }
    }

    module.exports = Singleton;

    ```
    As we can see we actually created two classes `PrivateSingleton` and `Singleton`. This is a trick to hide (create pseudo-private) constructor in ``Singleton`` class.<br />

    This way if we call `const object = new Singleton()` we will get an error: `Use Singleton.getInstance()`. However, if we call `Singleton.getInstance()` we will get the instance as expected. If there is no instance yet, we will call “private” constructor of `PrivateSingleton` class and return the instance. Otherwise, if the instance is already there, we simply return it.<br />

    We also export just `Singleton` so if we require it in another file, `PrivateSingleton` won’t be available.<br />
    `resource` : [Medium](https://medium.com/swlh/node-js-and-singleton-pattern-7b08d11c726a)

3. If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?<br />

    well I think it's better to start bulding from the very root of the application, so in this case we have index.js that will be the only js file that won't export any functionality, as well it's better to start bulding the UML step by step in order to organize the work, haviing seperate directories for each se of related js files will help in understanding how the application rwally works.



<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)