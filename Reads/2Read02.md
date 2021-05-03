# HTML Text, CSS Introduction, and Basic JavaScript Instructions
# Text
- **Superscript & Subscript** <br />
    ```<sup>```:The ```<sup>``` element is used to contain characters that should be superscript such as the suffixes of dates or mathematical concepts like raising a number to a power such as 2<sup>2</sup>.
    
    ```<sub>```: The ```<sub>``` element is used to contain characters that should be subscript. It is commonly used with foot notes or chemical formulas such as H<sub>2</sub>0

- Line Breaks & Horizontal Rules <br />
    As you have already seen, the 
    browser will automatically show 
    each new paragraph or heading 
    on a new line. But if you wanted 
    to add a line break inside the 
    middle of a paragraph you can 
    use the line break tag ```<br />```.<br />
    ```<hr />``` To create a break between themes — such as a change of topic in a book or a new scene in a play — you can add a horizontal rule between sections using the ```<hr />``` tag, FOr Example:<br />

    ```
    <p>Venus is the only planet that rotates 
    clockwise.</p><hr />
    <p>Jupiter is bigger than all the other planets combined.</p>
    ```
    and the result will look like this:<br />

    <p>Venus is the only planet that rotates 
    clockwise.</p>
    <hr />
    <p>Jupiter is bigger than all the other planets 
    combined.</p><br />

    There are a few elements that do not have any words between an opening and closing tag. They are known as empty elementsand they are written differently. An empty element usually has only one tag. Before the closing angled bracket of an empty element there will often be a space and a forward slash character. Some web page authors miss this out but it is a good habit to get into.

- Semantic Markup<br />
    Browsers often display the contents of thes semantic elements in a different way. For example, the content of the ```<em>``` element is shown in <em>italics<em/>, and a ```<blockquote>``` is usually indented. But you should not use them to change the way that your text looks; their purpose is to describe the content of your web pages more accurately.The reason for using these elements is that other programs, such as screen readers or search engines, can use this extra information. For example, the voice of a screen reader may add emphasis to the words inside the ```<em>``` element, or a search engine might register that your page features a quote if you use the ```<blockquote>``` element.

    ```
    <blockquote cite="http://en.wikipedia.org/wiki/Winnie-the-Pooh">
    <p>Did you ever stop to think, and forget to start again?</p>
    </blockquote>
    <p>As A.A. Milne said, <q>Some people talk to animals. Not many listen though. That's the problem.</q></p>
    ```
    and the result will look like this:<br />

    <blockquote cite="http://en.wikipedia.org/wiki/
    Winnie-the-Pooh">
    <p>Did you ever stop to think, and forget to start 
    again?</p>
    </blockquote>
    <p>As A.A. Milne said, <q>Some people talk to 
    animals. Not many listen though. That's the 
    problem.</q></p>

    - bbreviations & Acronyms:<br />
        If you use an abbreviation or an acronym, then the ```<abbr>``` element can be used. A title attribute on the opening tag is used to specify the full term.<br />
        ```
        <p><abbr title="Professor">Prof</abbr> Stephen 
        Hawking is a theoretical physicist and 
        cosmologist.</p>
        <p><acronym title="National Aeronautics and Space 
        Administration">NASA</acronym> do some crazy 
        space stuff.</p>
        ```
        try to hover over the next text to see the result:<br />
        <p><abbr title="Professor">Prof</abbr> Stephen 
        Hawking is a theoretical physicist and 
        cosmologist.</p>
        <p><acronym title="National Aeronautics and Space 
        Administration">NASA</acronym> do some crazy 
        space stuff.</p>


[Home]( https://kztahat.github.io/reading-notes/)