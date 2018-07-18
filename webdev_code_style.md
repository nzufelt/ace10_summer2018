# Code Styling for Web Development

The following guideline shows you exactly how your HTML, CSS, and JavaScript should be styled.  If you adhere to this guide, you won't lose any points on code styling, guaranteed.

### General rules:
* Blank lines should be placed intentionally, to section off large areas of code from each other.  
* There should _never_ be more than one blank line in a row.

### HTML
HTML is a hierarchical language, and as such, the indentation should reflect the nesting of elements.

* Individual elements should be styled as either single-line elements:
  ```
  <p> Here is my paragraph! </p>
  ```
  or as a nested hierarchy:
  ```
  <p>
    Here is the paragraph's content.  Notice, the content is indented two spaces relative to the tags!
  </p>    
  ```
  This applies to all elements, even ones with tons of content in them! You should prefer the second option to the first, except for elements with small amounts of content in them (like a `<h1>` tag).  There should not be any blank lines, except to break up large chunks of HTML, at the end of a large `<div>`.  Here are some bad examples:
  ```
  <p> Don't do this!
  </p>

  <p>
    Or this!
    </p>

  <p>
    Or this! (Notice the blank line...)

  </p>
  ```

* If you follow the first rule _exactly_, it should be the only rule you need.  This creates the visual hierarchy:
  ```
  <div>
    <h1> This is appropriately styled HTML </h1>
    <div class="content-box">
      <p>
        Here is <a href="https://www.google.com">a link to Google</a>.
      </p>
    </div>
  </div>

  <h3> Note the blank line above </h3>
  <p> It's okay because it separates big chunks from each other. </p>
  ```

### CSS
CSS code should either be in its own CSS file, or in the `<style>` tags of your HTML document.  Ideally, it's in its own file (as an [external stylesheet](https://www.w3schools.com/css/css_howto.asp)), but it's okay either way.
* [CSS code](https://www.w3schools.com/css/css_syntax.asp) is written with a selector, followed by a space and a brace `{`, followed by a single property-value pair on each line indented _two spaces_.  This is ended by a line containing an unindented closing brace `}`, followed by a blank line:
  ```
  p {
    width: 300px;
    margin: 0 auto;
    color: rgb(0, 100, 50);
  }

  .link:visited {
    color: rgb(200, 0, 0);
  }
  ```
* Here are some bad examples.  
  * Make sure only the selector and the open brace `{` are on their line.  Don't do:
      ```
      p {width: 300px;}
      ```
  * Make sure to line up the closing brace `}` appropriately, as well as the next selector.  Don't do:
    ```
    p {
      width: 300px;
      }

      div {
    ```
  * Make sure there's a blank line between each selector.  Don't do:
    ```
    p {
      width: 300px;
    }
    div {
      width: 300px;
    }
    ```

### JavaScript
* End every line of JavaScript that isn't a block-beginning (`{`) or block-ending line (`}`) with a semi-colon:

    ```
    // Good!
    var x = 0;

    // Good!
    function double(y) {
      return y * 2;
    }

    // Bad!
    var x = 4

    // Bad!
    function double {;
      return y * 2;
    };
    ```
* Every time you enter a new pair of braces (_i.e._ every time you enter a new _block_), indent two additional spaces.  This is good:
    ```
    // not indented
    var x = 0;

    function multiply(a, b) {
      // two spaces indented
      var output = 0;
      for (var i = 0; i < b; i++) {
        // two more spaces (four total) indented
        output = output + a;
      }
      // back to two spaces indented
      return output;
    }

    // back to no indentation
    ```
* Place a blank line immediately before and after defining a function.  The exception here is if you use a comment right before the function to describe the function
    ```
    // Good: blank line, then comment, then function

    // this function multiplies the two inputs, returning the result
    function multiply(a, b) {
      ...

    // Bad: this function doesn't have a blank line between it and the next one:

    function simple(a) {
      return a + 2;
    }
    function oops(b) {
      ...
    ```

#### Good luck, and ask me questions as you have them!
