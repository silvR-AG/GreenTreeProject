# Technical Paper - HTML-CSS


## HTML:
    Hyper Text Markup Language or HTML is a standard markup language used for creating the structure of a webpage. A markup language is a computer language that consists of easily understood keywords, names, or tags that help format the overall view of a page and the data it contains.

### Features of HTML:
   1. Elements
   2. Tags
   3. Page Structure

##### 1.Elements:
    Anything and everything on an HTML document, that form the basic buulding block of a webpage is an element. From tags to the text on the page, or the details that tell us about the page. They can all be considered an element.
##### 2. Tags:
    Tags can be considered as the building blocks used to construct a page. Everything that is put on an HTML file, has to be defined within a tage in order for the page to dislpay it. For example, the body tag <body>. Each tag, once opened must be closed.
    For example, <body> Body description </body>

    Tags are considered elements too.
##### 3. Page Structure:
    Page structure is created using the elements of HTML. Generally, a page structure consists of a <header> - <body> -<footer> structure. While a <head> tag is created to give the page its attributes.


# Cascading Style Sheet(CSS):
    While HTML is used to create the basic skeletal structure a page, CSS is where all the fun begins. Cascading Style Sheet or CSS is a tool used to style and create a well-defined structure of a webpage. While HTML can give a skeletal structure, CSS can add multitude of details to that structure. Basically what makes a page beautiful and aesthetic to the eyes is CSS.

    There are multiple ways to add details to a page like:
   1. Inline styling, i.e., adding styles like font color, while creating HTML tags. For example,
            <p font-color: purple>
   2. Using <style> tag in the <head> tag.  
        <head><style>CSS Description</style></head>
   3. Creating external style sheet, then adding the given file to <head> tag.
        <head><link rel="stylesheet" href="style.css"></head>

# Introduction:
    Now that we are done with the basic introduction of HTML and CSS, Let us look into what we will be discussing about in this paper. In this paper we will be having a brief view of the following topics relating to CSS.
    1. Box Model
    2. Inline versus Block Elements
    3. Positioning: Relative/Absolute
    4. Common CSS Structural Classes
    5. CSS Specifity
    6. CSS Responsive Queries
    7. Flexbox/Grid
    8. Common header meta tags
    9.  Miscellaneous topics

### Box Model:
    In an HTML page view, all elements can be considered as boxes. CSS box model is a box that wraps around every element of the HTML page layout. For example, if an element is created using the <div> tag, it will take up space on the page based on the dimensions of the <div> element defined in the CSS document.

    The CSS box model consists of the following features/attributes (From outside to inside):
    1. Margin
    2. Border
    3. Padding
    4. Content
    
    While Margin and Border are considered as external and structural attributes. Padding and content are considered as internal and styling attributes. This is because, Margins and Borders define the structure of the box with respect to the parent structure(be it page or another parent structure). While Padding and Content define everything that goes within the box.

### Inline versus Block elements:
    Now that we know about the box model, let us look into the two types of elements, namely, the inline elements and the block elements. These are based on the display value of the HTML elements, each of which has a default display value.

    1. Block Elements: A block-level element always starts on a new line, and the browsers automatically add some space (a margin) before and after the element. And it always takes all the width available i.e., it stretches as far as possible to both the left and the right sides.

    An example of the block element is the <p> element. When creating this element, if we look into it, we can see that this elements takes all the available space.

    2. Inline Elements: An inline element does not start on a new line. Also, it only takes the necessary space. An example of the inline element is the anchor <a> element. It should be noted, an inline element cannot contain a block element. While the opposite is possible. 
   
### Positioning: Relative/Absolute:
    In an HTML structured page, every element has a certain position affixed to it. The element takes up the necessary space on that certain position. The starting position on an HTML page is top: 0 / left: 0. There are multiple ways to define an elements position. Two of the common ones are: Relative and Absolute positioning.

    1. Relative positioning: A element with relative positioning is placed at a position relative to the normal position. Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.
    
    The CSS script for relatively positioned structure is something like this:
        div {
                position: relative;
                left: 30px;
                border: 3px solid #73AD21;
            }

    2. Absolute positioning: An element with absolute positioning is positioned relative to the nearest positioned ancestor.However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling. Absolute elements are removed from the flow and can be overlapped on other elements.

    The CSS script for an absolutely positioned structure is somethig like this:
        div{
                position: absolute;
                top: 80px;
                right: 0;
                width: 200px;
                height: 100px;
                border: 3px solid #73AD21;
            }

### Common CSS Structural Classes:
    Structural classes allow access to the child elements present within the hierarchy of parent elements. We can select first-child element, last-child element, alternate elements present within the hierarchy of parent elements.

    The following is the list of structural classes:
    1. :first-child - :first-child represents the element that is prior to its siblings in a tree structure.
    2. nth-child(n) - :nth-child class applies CSS properties to those elements that appear at the position evaluated by the resultant of an expression. The expression evaluates to a value resulting in the position of the element in a tree structure.
    3. :last-child - :last-child pseudo class represents the element that is at the end of its siblings in a tree structure.
    4. :nth-last-child(n) - :nth-last-child(Expression) is the same as :nth-child but the positioning of elements start from the end.
    5. :only-child - :only-child represents the element that is a sole child of the parent element and there is no other sibling.
    6. :first-of-type - There might be more than one type of siblings under a common parent. It selects the first element of the one type of sibling.
    7. :nth-of-type(n) - There may be more than one elements of the same type under a common parent. :nth-of-type represents those elements of the same type at the position evaluated by the Expression. 
    8. :last-of-type - :last-of-type represents the last element in the list of same type of siblings.
    9. :nth-last-of-type(n) -It is the same as :nth-of-type(n) but it starts counting of position from the end instead of start.
### CSS Specifity:
    CSS Specifity means if there are two or more CSS rules that point to the same element, the selector with the highest specificity value will "win", and its style declaration will be applied to that HTML element.Specifity can be considered as a priority order that determines which style declaration are ultimately applied to an element.

    For example:
                 <html>
                    <head>
                        <style>
                            #demo {color: blue;}
    .                       test {color: green;}
                            p {color: red;}
                        </style>
                    </head>
                    <body>
                        <p id="demo" class="test" style="color: pink;">Hello World!</p>
                    </body>
                </html>

    In this example, the text will be pink, because the inline style is given the highest priority.

### CSS Responsive Queries:
    Responsive web design makes your web page look good on all devices. Responsive web design uses only HTML and CSS. Using Responsive web design the web pages can be viewed using many different devices: desktops, tablets, and phones. Your web page should look good, and be easy to use, regardless of the device. It is called responsive web design when you use CSS and HTML to resize, hide, shrink, enlarge, or move the content to make it look good on any screen.

    In order to make a web page one of the essential things to do is, add this information using the meta tag:
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    This gives the browser instructions on how to control the page's dimensions and scaling.

    The most common tool used to create a responsive web design is the @media or the media query.
        @media(the condition){
            CSS description
        }
    In the structured portrayed above, the @media tag is used to initiate the query, while the condition part dictates whether the CSS styling inside the query would be applied to the page. Based on the condition, the mentioned CSS style would be applied to the webpage.

### Flexbox/Grid:
    Flexbox and the Grid designing have now become the basics of responsive web designing. This is because, as instead of using defined values for positioning. Flexbox and Grids position the elements based on the positioning attribute present in grids and flexbox.

    Flexbox is a 1-Dimensional positioning/alignment tool. It can position elements with respect to each other in a one-directional alignment. The general structure is as follows:
        div{
            display: flex;
            flex-direction: row;
            justitify-content: space-evenly;
        }
    This syntax will place the elements in a evenly-spaced manner, row-wise.

    Grid on the other hand is a 2-Dimensional positioning/alignment tool. It divides the availabe space into a user defined grid and then positions the element based on that grid.
    The general structure is as follows:
        div{
            display: grid;
            grid-template-columns: 1fr 1fr;
            grid-template-rows: 1fr 1fr;
        }
    This syntax will create a 2x2 grid, which can then be used to position the elements.

### Common header meta tags:
    The <meta> tag defines metadata about an HTML document. Metadata is information about data. <meta> tags always go inside the <head> element, and are typically used to specify character set, page description, keywords, author of the document, and viewport settings.Metadata will not be displayed on the page, but is machine parsable.

    Some common meta tags are:
        1. charset: character_set - Specifies the character encoding for the HTML document.
        2. content: text - Specifies the value associated with the http-equiv or name attribute
        3. http-equiv: content-security-policy content-type default-style refresh - Provides an HTTP header for the information/value of the content attribute.
        4. name: application name or author description generator keywords and viewports - Specifies a name for the metadata.

### Miscellaneous:
    Some things must be kept in mind while making a style sheet for an HTML document. Like:
    - Changing structural aspects (like margins) should be avoided as much as possible.
    - While structuring a document, try to as much divisions as possible based on common attributes or common blocks. It helps to style elements of a common ancestor in a better way.
    - Try to create different style 
    - and structural sheets.
    - Keep common styles in the style sheet.

# Conclusion:
    CSS is a really useful tool, that can help us make a website aesthetic to the yes as well as make it responsive. There are various tools and queries available in CSS that can enable us to do so.

# References:
    - [CSS-HTML tutorials](https://www.w3schools.com/default.asp)
    - [CSS tutorials](https://css-tricks.com/)
