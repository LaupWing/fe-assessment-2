# Frontend Development 2

## Table of contents
* [Hoisting, Scope, Closure, and Context]()
* [Progressive Enhancement](#progressive-enhancement)
    * [Without CSS and Javascript](#without-css-and-javascript)
        * [Summary Without CSS and Javascript](#summary-without-css-and-javascript)
    * [With CSS](#with-css)
        * [Summarry With CSS](#summary-with-css)
    * [With CSS and Javascript](#with-css-and-javascript)
        * [Summarry With Javascript](#summary-with-javascript)

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


**_Without CSS and Javscript_**
![without css and Javscript](https://github.com/LaupWing/fe-assessment-2/blob/master/docs/no_css_js.gif)

#### Summary Without CSS and Javascript
*   Works, users can post account
*   Hard to find stuff
*   Very ugly

### With CSS
When adding css the website looks a lot better and its more comprehensive, because you can give some visual hierarchie by making the importnat stuff bigger and less important smaller.
I also hide some parts of the form with the use of css, so that users doesnt feel overwhelmed of the information that he/she has to fill in.

The only thing is that users cant switch to other parts of the form, because the buttons doesnt have an click event attached to it. This has to be done with javascript. 
The posssible solution for this is to add checkboxes to toggle visiblity in the form.
```css
.field{
    opacity: 0;
}
.checkbox:checked ~ .field{
    opacity: 1;
}
``` 

**_Added CSS_**
![with css](https://github.com/LaupWing/fe-assessment-2/blob/master/docs/css_on.gif)

#### Summary With CSS
*   Visual Hierarchy
*   More comprehensive
*   Lighter on the eyes
*   Less Effort to navigate
*   Buttons and functional doenst work

### With CSS and Javascript
By adding Javascript to the mix, the user can navigate to diffrent sections of the `form` by using the next and back buttons. Also there is an realtime check on the bottom to see which fields has to be filled in to maken an account. This also can be clicked to see what the error is or what the current state is.  

**_Navigate through form_**
![with css](https://github.com/LaupWing/fe-assessment-2/blob/master/docs/navigate.gif)

**_See Error_**
![with css](https://github.com/LaupWing/Project-Tech/blob/master/READMEImages/signup_more_info.gif)

#### Summary With Javscript
*   More functional
*   Buttons become clickable
*   Move through form with buttons
*   Show error info
*   Show Progress

### Summary All
I began with a bare minimum html, which works, because it is  just a simple form which sends data to the backed. By adding css the sites looks better and you give it a visual hierarchie which helps with the comprehension of the site. CSS also allows me to stack the form fields on top of each other to even improve the comprehension of the signup even more. By adding javascript the user can click on certian components of the site to see the more info and use the buttons to navigate through the form fields. 
Without CSS & JS             |  With CSS               |  With CSS & JS
:-------------------------:|:-------------------------:|:-------------------------:
![](https://github.com/LaupWing/fe-assessment-2/blob/master/docs/no_css_js.gif)  |  ![](https://github.com/LaupWing/fe-assessment-2/blob/master/docs/css_on.gif) |  ![](https://github.com/LaupWing/fe-assessment-2/blob/master/docs/navigate.gif)
