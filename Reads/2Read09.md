# Forms and Events
<!-- Chapter 7: “Forms” (p.144-175) && Chapter 14: “Lists, Tables & Forms” (pp.330-357) -->
## Forms
Traditionally, the term 'form' has referred to a printed document that contains spaces for you to fill in information. The best known form on the web is probably the search box that sits right in the middle of Google's homepage. In addition to enabling users to search, forms also allow users to perform other functions online. You will see forms when registering as a member of a website, when shopping online, and when signing up for newsletters or mailing lists.

- **Form Controls**:
    There are several types of form controls that you can use to collect information from visitors to your site.
    - ADDING TEXT:
    Password input: Like a single line text box but it masks the characters entered. Text input (single-line)Used for a single line of text such as email addresses and names.Text area (multi-line)For longer areas of text, such as messages and comments.
    - Making Choices:  Checkboxes: When a user can select and unselect one or more options. Radio buttons: For use when a user must select one of a number of options. Drop-down boxes: When a user must pick one of a number of options from a list.
    - Submitting Forms: Uploading Files: Image buttons Similar to submit buttons but they allow you to use an image.Submit buttonsTo submit data from your form to another web page. File upload Allows users to upload files (e.g. images) to a website.

- **How Forms Work**:
    1. A user fills in a form and then presses a button to submit the information to the server.
    4. The name of each form control is sent to the server along with the value the user enters or selects.
    6. The server processes the information using a programming language such as PHP, C#, VB.net, or Java. It may also store the information in a database.
    10. The server creates a new page to send back to the browser based on the information received.
<br />

- **Form Structure**:<br />
    ```<form>```
    Form controls live inside a ```<form>``` element. This element should always carry the actionattribute and will usually have a method and id attribute too.<br />
    ***action***<br />
    Every ```<form>``` element requires an action attribute. Its valueis the URL for the page on the server that will receive the information in the form when it is submitted.<br />
    ***method***<br />
    Forms can be sent using one of two methods: get or post.<br />

- **Text Input**:<br />
    ```<input>```
    The ```<input>``` element is used to create several different form controls. The value of the typeattribute determines what kind of input they will be creating.type="text"When the type attribute has a value of text, it creates a singleline text input.<br />
    ***name***<br />
    When users enter information into a form, the server needs to know which form control each piece of data was entered into. (For example, in a login form, the server needs to know what has been entered as the username and what has been given as the password.) Therefore, each form control requires a name attribute. The value of this attribute identifies the form control and is sent along with the information they enter to the server.<br />
    ***maxlength***<br />
    You can use the maxlengthattribute to limit the number of characters a user may enter into the text field. Its value is the number of characters they may enter. For example, if you were asking for a year, the maxlengthattribute could have a value of 4.<br />

    - **Password Input**:<br />
        ```<input>```
        ***type="password"***<br />
        When the type attribute has a value of password it creates a text box that acts just like a single-line text input, except the characters are blocked out. They are hidden in this way so that if someone is looking over the user's shoulder, they cannot see sensitive data such as passwords.<br />
        ***name***<br />
        The name attribute indicates the name of the password input, which is sent to the server with the password the user enters.<br />
        ***size, maxlength***<br />
        It can also carry the size and maxlength attributes like the the single-line text input.<br />

    - **Radio Button**:<br />
        ```<input>```***type="radio"***<br />
        Radio buttons allow users to pick just one of a number of options.<br />
        ***name***<br />
        The name attribute is sent to the server with the value of the option the user selects. When a question provides users with options for answers in the form of radio buttons, the value of the name attribute should be the same for all of the radio buttons used to answer that question.<br />
        ***value***<br />
        The value attribute indicates the value that is sent to the server for the selected option. The value of each of the buttons in a group should be different (so that the server knows which option the user has selected).<br />
        ***checked***:<br />
        The checked attribute can be used to indicate which value (if any) should be selected when the page loads. The value of this attribute is checked. Only one radio button in a group should use this attribute.
- **Grouping Form Elements**:
    ```<fieldset>```
    You can group related form controls together inside the ```<fieldset>``` element. This is particularly helpful for longer forms.Most browsers will show the fieldset with a line around the edge to show how they are related. The appearance of these lines can be adjusted using CSS.
    ```<legend>```
    The ```<legend>``` element can come directly after the opening ```<fieldset>``` tag and contains a caption which helps identify the purpose of that group of form controls.
<br />

<!-- Chapter 6: “Events” (pp.243-292) -->
## Events
W hen you browse the web, your browser registers different types of events. It's the browser's way of saying, "Hey, this just happened." Your script can then respond to these events. Scripts often respond to these events by updating the content of the web page (via the Document Object Model) which makes the page feel more interactive.<br />


[Home]( https://kztahat.github.io/reading-notes/)