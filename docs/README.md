# Frontend Development 2

## Table of contents
* [Hoisting, Scope, Closure, and Context]()
* [Progressive Enhancement](#progressive-enhancement)
    * [Without CSS and Javascript](#without-css-and-javascript)
    * [With CSS](#with-css)

## Progressive Enhancement
Progressive Enhancement is gradually enhancing the website you are building. Your website has to work without javascript and css and by using javascript and css you can imporve your website (enhance). You can think of content first with Progressive enhancement.

In this section Im gonna describe how i applied Progressive Enhacement with the use of javascript and css on my job story.

### Without CSS and Javascript
My job story on its pures form, so without javascript and css, is just one big form which posts the info to the server and saves it in the backend. It doesnt required any css and javascript create an account, becuase my job story on its purest form is just an `form`  which sends an post request to an server. Its only without css very ugly.

```html
<form method="POST" action="/signup" enctype="multipart/form-data">
    <!-- Content -->
    <div class="buttons-container">
        <div class="buttons">
            <button class="back" type="button">back</button>
            <button class="next" type="button">next</button>
        </div>
        <button type="submit" disabled="true">submit</button>
    </div>
</form>
```

![without css and html](https://github.com/LaupWing/fe-assessment-2/blob/master/docs/no_css_js.gif)