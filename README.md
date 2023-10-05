# WEB_DEVELOPEMENT_INTERVIEW_QUESTIONS

# HTML

1. what is HTML ?
# HTML stands for Hyper Text Markup Language. it is a standard language for creating web pages.
# mark up language is a language which uses tags to define something.

2. what are tags ?
# HTML tags are used to mark or define elements within an HTML document. They provide structure and formatting instructions for web browsers to display content correctly.
  
3. What is the purpose of the <!DOCTYPE> declaration in an HTML document?
# The <!DOCTYPE> declaration specifies the document type and version of HTML used in a web page. It helps the browser render the page correctly by defining the rules and syntax for the document.

4. What is the difference between HTML and HTML5?
# HTML5 is the latest version of HTML. It introduced new elements (e.g., <video>, <audio>, <canvas>) and APIs, improved support for multimedia, and enhanced semantic markup for better document structure.

5. Explain the difference between inline and block-level elements?
# Inline elements do not start on a new line and only take up as much width as necessary. Examples include <a>, <span>, and <strong>. Block-level elements, on the other hand, start on a new line and take up the full width of their parent container.

6. How do you create a hyperlink in HTML?
# You can create a hyperlink using the a (anchor) element. Example: <a href="https://www.example.com">Visit Example</a>.

7. What is the purpose of the <meta> tag in HTML?
# The <meta> tag is used to provide metadata about the web page, such as character encoding, viewport settings for responsive design, and page description for search engines.


## CSS

1. what is css ?
  # css stands for cascading style sheet.it is used for decorating or presenting the html pages.

2. what are ways to include the css in our web page?
# there are 3 ways to include css in web page.
## inline : when we directly apply the css or style to the html element then it is inline way of applying css.
## internal : Embedding CSS within <style> tags in the HTML <head> section.
## External: Linking to an external CSS file using the <link> element.

3. What is the difference between display: none; and visibility: hidden;?
# display: none; completely removes an element from the document flow, making it invisible and not taking up any space.
# visibility: hidden; makes an element invisible, but it still occupies space in the layout.

4. What is the difference between class and ID selectors in CSS?
# Class selectors are preceded by a period (.) and can be used to apply styles to multiple elements on a page.
# ID selectors are preceded by a hash symbol (#) and are used to select and style a single unique element on a page.

5. What is the default value of the position property in CSS?
# The default value of the position property is static.

6. How can you center an element horizontally using CSS?
# You can center an element horizontally by using margin: 0 auto; if it has a specified width.

7. What is the difference between display: block; and display: inline;?
# display: block; makes an element a block-level element, causing it to take up the full width available and start on a new line.
# display: inline; makes an element an inline-level element, allowing it to flow within the content and not start on a new line

8. what is cascading styles in css ?
  # Cascading order in css determines how conflicting or overlapping rules are applied for html elements.

  eg : 
  <style>  
    p{
      color:red;
    }

      .text{
        color:blue;
      }

    #content{
      color:pink
    }
    
  </style>
  
  <p class="text" id="content"> text in p tag </p>


  here p will be of pink color because id selector has the highest specificity.

  order of specificity is :
  
  1. Inline styles
  2. id selector
  3. class selector
  4. inheritance.
     
9. 

