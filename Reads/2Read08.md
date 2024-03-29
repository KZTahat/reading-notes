# More CSS Layout
<!-- HTML/CSS book, Ch. 15, “Layout” (again; repeat of Class 4 reading) -->
# Layout
We are going to look at how to control where each element sits on a page and how to create attractive page layouts.<br />
- **Building Blocks**:
    CSS treats each HTML element as if it is in its own box. This box will either be a block-level box where it will *start on a new line* or an inline box where it will flow in between surrounding text.
    Block-level boxes start on a new line and act as the main building blocks of any layout, while inline boxes flow between surrounding text. You can control how much space each box takes up by setting the width of the boxes (and sometimes the height, too). To separate boxes, you can use borders, margins, padding, and background colors. <br />
    - **Contaning elemants**:
        If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element. It is common to group a number of elements together inside a ```<div>``` (or other block-level) element. For example, you might group together all of the elements that form the header of a site (such as the logo and the main navigation). The ```<div>``` element that contains this group of elements is then referred to as the containing element.<br />
    - **Controlling the Position of Elements**:
        CSS has the following positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning. You specify the positioning scheme using the positionproperty in CSS. You can also float elements using the float property.<br />
        - **Normal flow**:
            Every block-level element appears on a new line, causing each item to appear lower down the page than the previous one. Even if you specify the width of the boxes and there is space for two elements to sit side-byside, they will not appear next to each other. This is the default behavior (unless you tell the browser to do something else).<br />
        - **Relative Positioning**:
            This moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been placed. This does not affect the position of surrounding elements; they stay in the position they would be in in normal flow.<br />
        - **Absolute positioning**:
            This positions the element in relation to its containing element. It is taken out of normal flow, meaning that it does not affect the position of any surrounding elements (as they simply ignore the space it would have taken up). Absolutely positioned elements move as users scroll up and down the page.<br />

            ***TO BE CONTINUED***

<br />
<br />
[Home]( https://kztahat.github.io/reading-notes/)