# Read 04

## Data Modeling

1. Name 3 advantages to Test Driven Development<br />
    - Detailed project documentation.<br />
    - Code flexibility and easier maintenance.<br />
    - stay sure about wether future changes might affect the code or not.<br />
<br />

2. In what case would you need to use beforeEach() or afterEach() in a test suite?<br />
    - When we need to use mock Implementation.<br />
    - If each test in your describe needs a new copy of the structure because each test is modifying the structure then you should use beforeEach to create the structure anew for each test and then afterEach if you need to tear it down cleanly.<br />

3. What is one downside of Test Driven Development<br />
    `Tests got to be maintained when requirements change`
    Probably, the strongest argument against TDD is that the tests need to be maintained because the code has got to. Whenever requirements change, you would like to vary the code and tests. But you’re working with TDD. this suggests that you simply got to change the tests first then make the tests pass. So, actually, this disadvantage is that the same as before when writing code that apparently takes an extended time.y takes a long time.<br />
    `resource` : [GeeksforGeeks](https://www.geeksforgeeks.org/advantages-and-disadvantages-of-test-driven-development-tdd/)


4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?<br />
    ES6 classess ensures that this keyword used by the developer is referring to the object being created by the developer. while in ES5 any function can be used as a function constructor and it primarily focuses on the creation of reusable object creation code.<br />

5. Why REST? <br />
    1. REST is Easy to Understand and Implement<br />
    2. REST Makes your Application More Scalable<br />
        - No State
            As we will see in the next section (Principles of REST), one of the core principles of REST is that it's stateless on the server-side. Therefore each request will be processed independently from the previous ones.<br />
        - Faster Data Interchange Format
            RESTful APIs typically use JSON as the data interchange format. JSON is much more compact and smaller in size compared to XML. It can also be parsed faster than XML.<br />

    3. Caching is Easier with REST<br />
        REST aims to make caching easier. Since the server is stateless and each request can be processed individually, GET requests should usually return the same response regardless of previous ones and the session.<br />
    4. REST is Flexibile<br />
        By flexibility, I mean that it's easy to modify and it's also able to answer many clients who can ask for different data types (XML, JSON, and so on)<br />

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)