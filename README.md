# Readme.js
[Readme.js](http://readme.knight.io/) is a jQuery Plugin that embeds the Readme of a Github Repo into any website.

Demo & Examples: [http://readme.knight.io/](http://readme.knight.io/)

### How to Use
You have two options when using Readme.js:
  - Using HTML Data-Attributes
    ```html
      <div class='readme_js' data-owner='thomasklemm' data-repo='Readme.js'></div>

      Note: Readme.js will automatically instantiate elements with a class of 'readme_js'
    ```
  - Using Javascript
    ```html
      <div id='Readme'></div>

      <!-- Note: jQuery and Readme.js have to be loaded -->
      <script>
        $('#Readme').readme({
          'owner': 'thomasklemm',
          'repo':  'Readme.js'
        });
      </script>
    ```
That's it. The Readme will be pulled from Github's respective API and inserted along with some basic styles.

### Step-by-Step
1. Include jQuery and `readme.js` files in your HTML
  ```html
    <script src="PATH/TO/jquery.js"><script>
    <script src="PATH/TO/readme.js"><script>
  ```
2. Create an element for the Readme
  ```html
    <div id='Readme'></div>
  ```
3. Instantiate Readme.js
  ```html
    <script>
      $('#Readme').readme({
        'owner': 'thomasklemm',
        'repo':  'Readme.js'
      });
    </script>
```
4. You are all set up!

### How does it work?
Some jaw-dropping kind of Yedi-Style Magic :-D

Nah - that would be nice. 

However, Readme.js actually just requests a Github Repo's Readme at the [corresponding Github API](http://developer.github.com/v3/repos/contents/) and inserts the html into the elements you specify. It also ships with some styles extracted from the Github homepage (Note: As for permission) so that proper Syntax Highlighting can happen as well.

### FAQs & Common Error Messages

#### What does "XMLHttpRequest cannot load https://api.github.com/repos/sinatra/sinatra/readme. Origin http://mysite.com is not allowed by Access-Control-Allow-Origin." mean?

The most common error to occur is related to Ajax Cross-Site Requests. I'll refer to the Github API Manual for you to read up on [how to enable Ajax Cross-Site Requests to Github from your Domain](http://developer.github.com/v3/#cross-origin-resource-sharing). You will be able to get it working in a few minutes.

### Requirements & Testing
Readme.js requires jQuery 1.4+ and should work in all current browsers.

### Is it any good?
[We'll see.](http://news.ycombinator.com/item?id=3067434)

### License
MIT