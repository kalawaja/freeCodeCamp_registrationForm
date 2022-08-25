# Learn HTML Forms by Building a Registration Form, Completed

> - You can use HTML forms to collect information from people who visit your webpage.
> - In this course, you'll learn HTML forms by building a signup page. You'll learn how to control what types of data people can type into your form, and some new CSS tools for styling your page.
---

> **Step 1** <br>
Welcome to the Registration Form project! Start by adding the `!DOCTYPE html` declaration at the top of the document so the browser knows what type of document it's reading.

```html
#index.html
<!DOCTYPE html>
```
> **Step 2** <br>
Below the `DOCTYPE`, add an `html` element with a `lang` attribute set to `en`, so that you have a place to start putting some code.

```html
#index.html
<!DOCTYPE html>
<html lang="en">
</html>
```
> **Step 3** <br>
Next, add opening and closing `head` and `body` tags within the `html` element.

```html
#index.html
<!DOCTYPE html>
<html lang="en">
    <head>

    </head>
    <body>

    </body>
</html>
```
> **Step 4** <br>
Add a `title` and a `meta` elements to the `head`. Give your project a title of `Registration Form`, and give a `charset` attribute with a value of `UTF-8` to your `meta` element.

```html
#index.html
  <head>
    <meta charset="UTF-8">
    <title>Registration Form</title>
  </head>
```
> **Step 5** <br>
Nest a self-closing `link` element within the `head` element. Give it a `rel` attribute with value of `stylesheet` and an `href` attribute with a value of `styles.css`.

```html
#index.html
  <head>
    <meta charset="UTF-8">
    <title>Registration Form</title>
    <link rel="stylesheet" href="styles.css">
  </head>
```
> **Step 6** <br>
Within the `body`, provide a heading context for the content, by adding an `h1` with the text `Registration Form`.

```html
#index.html
  <body>
    <h1>Registration Form</h1>
  </body>
```
> **Step 7** <br>
Below the heading, use the following text within a paragraph element to encourage users to register:<br>
> `Please fill out this form with the required information`

```html
#index.html
  <body>
    <h1>Registration Form</h1>
    <p>Please fill out this form with the required information</p>
  </body>
```
> **Step 8** <br>
To spruce the project up, let us add some CSS. Begin by giving the `body` a `width` of `100%`, and a `height` of `100vh`.

```css
#styles.css
body {
  width: 100%;
  height: 100vh;
}
```
> **Step 9** <br>
Now, get rid of the horizontal scroll-bar, by setting the `body` default `margin` added by some browsers to `0`.

```css
#styles.css
body {
  width: 100%;
  height: 100vh;
  margin: 0;
}
```
> **Step 10** <br>
That is better. Now, make the background easy on the eyes, by changing the `body` `background-color` to `#1b1b32`. Then, to see the text, change the `color` to `#f5f6f7`.

```css
#styles.css
body {
  width: 100%;
  height: 100vh;
  margin: 0;
  background-color: #1b1b32;
  color: #f5f6f7;
}
```
> **Step 11** <br>
As suggested by the title, you are creating a form. So, after the `p` element, insert a `form` with an `action` attribute targeting `https://register-demo.freecodecamp.org`.

```html
#index.html
  <body>
    <h1>Registration Form</h1>
    <p>Please fill out this form with the required information</p>
    <form action="https://register-demo.freecodecamp.org">
    </form>
  </body>
```
> **Step 12** <br>
As the form will have three distinct sections, add three `fieldset` elements within the `form` element.

```html
#index.html
  <body>
    <h1>Registration Form</h1>
    <p>Please fill out this form with the required information</p>
    <form action='https://register-demo.freecodecamp.org'>
    <fieldset></fieldset>
    <fieldset></fieldset>
    <fieldset></fieldset>
    </form>
  </body>
```
> **Step 13** <br>
The first `fieldset` will hold name, email, and password fields. Start by adding four `label` elements to the first `fieldset`.

```html
#index.html
    <form action='https://register-demo.freecodecamp.org'>
      <fieldset>
        <label></label>
        <label></label>
        <label></label>
        <label></label>
      </fieldset>
      <fieldset></fieldset>
      <fieldset></fieldset>
    </form>
```
> **Step 14** <br>
Add the following text to the `label` elements:
> <br>
> - `Enter Your First Name:`
> - `Enter Your Last Name:`
> - `Enter Your Email:`
> - `Create a New Password:`

```html
#index.html
      <fieldset>
        <label>Enter Your First Name:</label>
        <label>Enter Your Last Name:</label>
        <label>Enter Your Email:</label>
        <label>Create a New Password:</label>
      </fieldset>
```
> **Step 15** <br>
As `label` elements are inline by default, they are all displayed side by side on the same line, making their text hard to read. To make them appear on separate lines, add `display: block` to the `label` element, and add a `margin` of `0.5rem 0`, to separate them from each other.

```css
#styles.css
label {
  display: block;
  margin: 0.5rem 0;
}
```
> **Step 16** <br>
Nest an `input` element within each `label`. Be sure to add each `input` after the `label` text, and include a space after the colon.

```html
#index.html
      <fieldset>
        <label>Enter Your First Name: <input />
        </label>
        <label>Enter Your Last Name: <input />
        </label>
        <label>Enter Your Email: <input />
        </label>
        <label>Create a New Password: <input />
        </label>
      </fieldset>
```
> **Step 17** <br>
Specifying the `type` attribute of a form element is important for the browser to know what kind of data it should expect. If the `type` is not specified, the browser will default to text.<br>
Give the first two `input` elements a `type` attribute of `text`, the third a `type` attribute of `email`, and the fourth a `type` attribute of `password`.<br>
The `email` type only allows emails with a ` @ ` and a ` . ` in the domain. The `password` type obscures the input, and warns if the site does not use HTTPS.

```html
#index.html
      <fieldset>
        <label>Enter Your First Name: <input type="text"/></label>
        <label>Enter Your Last Name: <input type="text"/></label>
        <label>Enter Your Email: <input type="email"/></label>
        <label>Create a New Password: <input type="password"/></label>
      </fieldset>
```
> **Step 18** <br>
The first `input` element with a `type` of `submit` is automatically set to submit its nearest parent `form` element.<br>
To handle the form submission, after the last `fieldset` element add an `input` element with the `type` attribute set to `submit` and the `value` attribute set to `Submit`.

```html
#index.html
      <fieldset>
        <label>Enter Your First Name: <input type="text" /></label>
        <label>Enter Your Last Name: <input type="text" /></label>
        <label>Enter Your Email: <input type="email" /></label>
        <label>Create a New Password: <input type="password" /></label>
      </fieldset>

      <fieldset></fieldset>

      <fieldset></fieldset>

      <input type="submit" value="Submit"/>
```
> **Step 19** <br>
At this point, you should be able to submit the form. However, you might notice not much happens.<br>
To make the form more interactive, add the `required` attribute to the `input` elements in the first `fieldset`.<br>
Now, if you try to submit the form without filling in the required fields, you will see an error message.

```html
#index.html
      <fieldset>
        <label>Enter Your First Name: <input type="text" required /></label>
        <label>Enter Your Last Name: <input type="text" required /></label>
        <label>Enter Your Email: <input type="email" required /></label>
        <label>Create a New Password: <input type="password" required /></label>
      </fieldset>

      <fieldset></fieldset>

      <fieldset></fieldset>

      <input type="submit" value="Submit" />
```
> **Step 20** <br>
Certain `type` attribute values come with built-in form validation. For example, `type="email"` requires that the value be a valid email address.<br>
Add custom validation to the password `input` element, by adding a `minlength` attribute with a value of `8`. Doing so prevents inputs of less than 8 characters being submitted.

```html
#index.html
      <fieldset>
        <label>Enter Your First Name: <input type="text" required /></label>
        <label>Enter Your Last Name: <input type="text" required /></label>
        <label>Enter Your Email: <input type="email" required /></label>
        <label>Create a New Password: <input type="password" minlength="8" required /></label>
      </fieldset>

      <fieldset></fieldset>

      <fieldset></fieldset>

      <input type="submit" value="Submit" />
```
> **Step 21** <br>
With `type="password"` you can use the `pattern` attribute to define a regular expression that the password must match to be considered valid.<br>
Add a `pattern` attribute to the password `input` element to require the input match: `[a-z0-5]{8,}`<br>
The above is a regular expression which matches eight or more lowercase letters or the digits `0` to `5`. Then, remove the `minlength` attribute, and try it out.

```html
#index.html
      <fieldset>
        <label>Enter Your First Name: <input type="text" required /></label>
        <label>Enter Your Last Name: <input type="text" required /></label>
        <label>Enter Your Email: <input type="email" required /></label>
        <label>Create a New Password: <input type="password" pattern="[a-z0-5]{8,}" required /></label>
      </fieldset>
```
> **Step 22** <br>
Let us go to the next part of the registration form. This section will ask for the type of account the user is opening, and will confirm the user has read the terms and conditions.<br>
Start by adding three `label` elements to the second `fieldset`.

```html
#index.html
      <fieldset>
        <label></label>
        <label></label>
        <label></label>
      </fieldset>
```
> **Step 23** <br>
Users will be allowed to choose either a `Personal Account` or `Business Account`.<br>
To do this, within each of the first two `label` elements, add one `input` element with `type="radio"`.

```html
#index.html
      <fieldset>
        <label><input type="radio" /></label>
        <label><input type="radio" /></label>
        <label></label>
      </fieldset>
```
> **Step 24** <br>
For the terms and conditions, add an `input` with a `type` of `checkbox` to the third `label` element. Also, as we do not want users to sign up, without having read the terms and conditions, make it `required`.

```html
#index.html
      <fieldset>
        <label><input type="radio" /></label>
        <label><input type="radio" /></label>
        <label><input type="checkbox" required /></label>
      </fieldset>
```
> **Step 25** <br>
Within each corresponding `label` element, and immediately after the `input` element, add a space and add the following text:<br>
> `Personal Account` <br>
> `Business Account` <br>
> `I accept the terms and conditions`

```html
#index.html
      <fieldset>
        <label><input type="radio" /> Personal Account</label>
        <label><input type="radio" /> Business Account</label>
        <label><input type="checkbox" required /> I accept the terms and conditions</label>
      </fieldset>
```
> **Step 26** <br>
You only want one radio input to be selectable at a time. However, the form does not know the radio inputs are related.<br>
To relate the radio inputs, give them the same `name` attribute with a value of `account-type`. Now, it is not possible to select both radio inputs at the same time.

```html
#index.html
      <fieldset>
        <label><input type="radio" name="account-type" /> Personal Account</label>
        <label><input type="radio" name="account-type" /> Business Account</label>
        <label><input type="checkbox" required /> I accept the terms and conditions</label>
      </fieldset>
```
> **Step 27** <br>
To finish this `fieldset` off, link the text `terms and conditions` in the third `label` to the following location:<br>
> `https://www.freecodecamp.org/news/terms-of-service/`

```html
#index.html
      <fieldset>
        <label><input type="radio" name="account-type" /> Personal Account</label>
        <label><input type="radio" name="account-type" /> Business Account</label>
        <label><input type="checkbox" required /> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</label>
      </fieldset>
```
> **Step 28** <br>
Moving on to the final `fieldset`. What if you wanted to allow a user to upload a profile picture?<br>
Well, the `input` type `file` allows just that. Add a `label` with the text `Upload a profile picture: `, and add an `input` accepting a file upload.

```html
#index.html
      <fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
      </fieldset>
```
> **Step 29** <br>
Add another `label` after the first, with the text `Input your age (years): `. Then, nest an `input` with the `type` of `number`.<br>
As we do not want users under the age of 13 to register, add a `min` attribute to the `input` with a value of `13`. Also, we can probably assume users over the age of 120 will not register; add a `max` attribute with a value of `120`.<br>
Now, if someone tries to submit the form with values outside of the range, a warning will appear, and the form will not submit. Give it a try.

```html
#index.html
      <fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label>Input your age (years): <input type="number" min="13" max="120" /></label>
      </fieldset>
```
> **Step 30** <br>
Adding a dropdown to the form is easy with the `select` element. The `select` element is a container for a group of `option` elements, and the `option` element acts as a label for each dropdown option. Both elements require closing tags.<br>
Start, by adding a `select` element below the two `label` elements. Then, nest 5 `option` elements within the `select` element.

```html
#index.html
      <fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label>Input your age (years): <input type="number" min="13" max="120" />
        </label>

        <select>
          <option></option>
          <option></option>
          <option></option>
          <option></option>
          <option></option>
        </select>

      </fieldset>
```
> **Step 31** <br>
Nest the `select` element (with its `option` elements) within a `label` element with the text `How did you hear about us?`. The text should come before the `select` element.

```html
#index.html
      <fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label>Input your age (years): <input type="number" min="13" max="120" />
        </label>

        <label>How did you hear about us?
          <select>
            <option></option>
            <option></option>
            <option></option>
            <option></option>
            <option></option>
          </select>
        </label>
      </fieldset>
```
> **Step 32** <br>
The dropdown options are currently empty. To give them content, add the following text to each subsequent `option` element:<br>
> `(select one)`<br>
> `freeCodeCamp News`<br>
> `freeCodeCamp YouTube Channel`<br>
> `freeCodeCamp Forum`<br>
> `Other`

```html
#index.html
      <fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label>Input your age (years): <input type="number" min="13" max="120" />
        </label>

        <label>How did you hear about us?
          <select>
            <option>(select one)</option>
            <option>freeCodeCamp News</option>
            <option>freeCodeCamp YouTube Channel</option>
            <option>freeCodeCamp Forum</option>
            <option>Other</option>
          </select>
        </label>

      </fieldset>
```
> **Step 33** <br>
Submitting the form with an option selected would not send a useful value to the server. As such, each `option` needs to be given a `value` attribute. Without which, the text content of the `option` will be submitted to the server.<br>
Give the first `option` a `value` of ` "" `, and the subsequent `option` elements `value` attributes from `1` to `4`.

```html
#index.html
      <fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label>Input your age (years): <input type="number" min="13" max="120" />
        </label>

        <label>How did you hear about us?
          <select>
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>

      </fieldset>
```
> **Step 34** <br>
The `textarea` element acts like an `input` element of type `text`, but comes with the added benefit of being able to receive multi-line text, and an initial number of text rows and columns.<br>
Users will be able to register with a bio. Add a `label` with the text `Provide a bio:` at the end of the `fieldset`. Add a `textarea` element inside the `label` element. Note that the `textarea` requires a closing tag.

```html
#index.html
      <fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label>Input your age (years): <input type="number" min="13" max="120" />
        </label>
        <label>How did you hear about us?
          <select>
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>

        <label>Provide a bio:
          <textarea></textarea>
        </label>

      </fieldset>
```
> **Step 35** <br>
The `textarea` appears too small. To give it an initial size, you can add the `rows` and `cols` attributes.<br>
Add an initial size of `3` rows and `30` columns.

```html
#index.html
      <fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label>Input your age (years): <input type="number" min="13" max="120" />
        </label>
        <label>How did you hear about us?
          <select>
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>

        <label>Provide a bio:
          <textarea rows="3" cols="30"></textarea>
        </label>

      </fieldset>
```
> **Step 36** <br>
To give Campers an idea of what to put in their bio, the `placeholder` attribute is used. The `placeholder` accepts a text value, which is displayed until the user starts typing.<br>
Give the `textarea` a `placeholder` of `I like coding on the beach...`.

```html
#index.html
      <fieldset>
        <label>Upload a profile picture: <input type="file" /></label>
        <label>Input your age (years): <input type="number" min="13" max="120" />
        </label>
        <label>How did you hear about us?
          <select>
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>

        <label>Provide a bio:
          <textarea rows="3" cols="30" placeholder="I like coding on the beach..."></textarea>
        </label>

      </fieldset>
```
> **Step 37** <br>
With form submissions, it is useful, and good practice, to provide each submittable element with a `name` attribute. This attribute is used to identify the element in the form submission.<br>
Give each submittable element a unique `name` attribute of your choosing, except for the two `radio` inputs.

```html
#index.html
      <fieldset>
        <label>Enter Your First Name: <input name="first-name" type="text" required /></label>
        <label>Enter Your Last Name: <input name="last-name" type="text" required /></label>
        <label>Enter Your Email: <input name="email" type="email" required /></label>
        <label>Create a New Password: <input name="password" type="password" pattern="[a-z0-5]{8,}" required /></label>
      </fieldset>
      <fieldset>
        <label><input type="radio" name="account-type" /> Personal Account</label>
        <label><input type="radio" name="account-type" /> Business Account</label>
        <label>
          <input name="checkbox" type="checkbox" required /> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
        </label>
      </fieldset>
      <fieldset>
        <label>Upload a profile picture: <input name="picture" type="file" /></label>
        <label>Input your age (years): <input name="age" type="number" min="13" max="120" />
        </label>
        <label>How did you hear about us?
          <select name="referrer">
            <option value="">(select one)</option>
            <option value="1">freeCodeCamp News</option>
            <option value="2">freeCodeCamp YouTube Channel</option>
            <option value="3">freeCodeCamp Forum</option>
            <option value="4">Other</option>
          </select>
        </label>
        <label>Provide a bio:
          <textarea name="bio" rows="3" cols="30" placeholder="I like coding on the beach..."></textarea>
        </label>
      </fieldset>
```
> **Step 38** <br>
The HTML for the registration form is finished. Now, you can spruce it up a bit.<br>
Start by changing the font to `Tahoma`, and the font size to `16px` in the `body`.

```css
#styles.css
body {
  width: 100%;
  height: 100vh;
  margin: 0;
  background-color: #1b1b32;
  color: #f5f6f7;
  font-family: Tahoma;
  font-size: 16px;
}
```
> **Step 39** <br>
Center the `h1` and `p` elements by giving them a `margin` of `1em` `auto`. Then, align their text in the `center` as well.

```css
#styles.css
h1, p {
  margin: 1em auto;
  text-align: center;
}
```
> **Step 40** <br>
Center the `form` element, by giving it a `margin` of `0 auto`. Then, fix its size to a maximum width of `500px`, and a minimum width of `300px`. In between that range, allow it to have a `width` of `60vw`.

```css
#styles.css
form {
  width: 60vw;
  max-width: 500px;
  min-width: 300px;
  margin: 0 auto;
}
```
> **Step 41** <br>
During development, it is useful to see the `fieldset` default borders. However, they make the content appear too separated.<br>
Remove the `border`, and add `2rem` of padding only to the top and bottom of each `fieldset`. Be sure to remove the `padding` from the left and right.

```css
#styles.css
fieldset {
  border: 0;
  padding-top: 2rem;
  padding-bottom: 2rem;
  padding-left: 0;
  padding-right: 0;
}
```
> **Step 42** <br>
To give the `fieldset` elements a bit of separation, select them and give them a `border-bottom` of `3px solid` `#3b3b4f`.

```css
#styles.css
fieldset {
  border: none;
  padding: 2rem 0;
  border-bottom: 3px solid #3b3b4f;
}
```
> **Step 43** <br>
The border of the last `fieldset` element looks a little out of place. You can select the last element of a specific type using the `last-of-type` CSS pseudo-class, like this:<br>
> <br>
> `p:last-of-type { }` <br>
> <br>
That will select the last `p` element. Create a new selector that targets the last `fieldset` element and set its `border-bottom` to `none`.

```css
#styles.css
fieldset:last-of-type {
  border-bottom: none;
}
```
> **Step 44** <br>
It would be nicer to have the `label` text appear above the form elements.<br>
Select all `input`, `textarea`, and `select` elements, and make them take up the full width of their parent elements.<br>
Also, add `10px` of `margin` to the top of the selected elements. Set the other margins to `0`.

```css
#styles.css
input, textarea, select {
  width: 100%;
  margin-top: 10px 0 0 0;
}
```
> **Step 45** <br>
For the second `fieldset`, you want the `input` and `label` text to appear on the same line.<br>
Start, by giving the `input` elements in the second `fieldset` a class of `inline`.

```html
#index.html
      <fieldset>
        <label><input class="inline" type="radio" name="account-type" /> Personal Account</label>
        <label><input class="inline" type="radio" name="account-type" /> Business Account</label>
        <label>
          <input class="inline" type="checkbox" name="terms" required /> I accept the <a href="https://www.freecodecamp.org/news/terms-of-service/">terms and conditions</a>
        </label>
      </fieldset>
```
> **Step 46** <br>
Select only the `.inline` elements, and give them `width` of `unset`. This will remove the earlier rule which set all the `input` elements to `width: 100%`.

```css
#styles.css
.inline {
  width: unset;
}
```
> **Step 47** <br>
Add some space between the `.inline` elements and the `label` text, by giving a right `margin` of `0.5em`. Also, set all the other margin to `0`.

```css
#styles.css
.inline {
  width: unset;
  margin-right: 0.5em;
  margin-left: 0;
  margin-top: 0;
  margin-bottom: 0;
}
```
> **Step 48** <br>
If you look close enough, you will notice the `.inline` elements are too high on the line.<br>
To combat this, set the `vertical-align` property to `middle`.

```css
#styles.css
.inline {
  width: unset;
  margin: 0 0.5em 0 0;
  vertical-align: middle;
}
```
> **Step 49** <br>
To make the `input` and `textarea` elements blend in with the background theme, set their `background-color` to `#0a0a23`. Then, give them a `1px`, `solid` border with a color of `#0a0a23`.

```css
#styles.css
input, textarea {
  background-color: #0a0a23;
  border: 1px solid #0a0a23
}
```
> **Step 50** <br>
Currently, if you type in the `input` or `textarea` elements, you will not be able to see the text. Also, their height is too small to be easy to use.<br>
Fix this, by setting the `color` to `#ffffff`, and setting their `min-height` to `2em`.

```css
#styles.css
input, textarea {
  background-color: #0a0a23;
  border: 1px solid #0a0a23;
  color: #ffffff;
  min-height: 2em;
}
```
> **Step 51** <br>
You want the `select` element to remain with a white background, but now it is not getting the same `min-height` as the `input` and `textarea` elements.<br>
Move the `min-height` property and value so that all three element types have the same `min-height` value, and the `select` element still has a white background.

```css
#styles.css
input,
textarea,
select {
  margin: 10px 0 0 0;
  width: 100%;
  min-height: 2em;
}
```
```css
#styles.css
input, textarea {
  background-color: #0a0a23;
  border: 1px solid #0a0a23;
  color: #ffffff;
}
```
> **Step 52** <br>
To style the submit button, you can use an *attribute* selector, which selects an element based on the given attribute value. Here is an example:<br>
> <br>
> `input[name="password"]`<br>
> <br>
> The above selects `input` elements with a `name` attribute value of `password`.<br>
> <br>
> Now, use the attribute selector to style the submit button with a `display` of `block`, and a `width` of `60%`.

```css
#styles.css
input[type="submit"] {
  display: block;
  width: 60%;
}
```
> **Step 53** <br>
With a `display` of `block` the submit button sits flush against the left edge of its parent.<br>
Use the same technique used to center the `form` to center the submit button.

```css
#styles.css
input[type="submit"] {
  display: block;
  width: 60%;
  margin: 0 auto;
}
```
> **Step 54** <br>
To make the submit button look more in line with the rest of the form, give it the same `height` as the other fields (`2em`). Also, increase the `font-size` to `1.1rem`.

```css
#styles.css
input[type="submit"] {
  display: block;
  width: 60%;
  margin: 0 auto;
  height: 2em;
  font-size: 1.1rem;
}
```
> **Step 55** <br>
To make the submit button appear more distinct, give it a `background-color` of `#3b3b4f`, and a `border-color` of `white`.

```css
#styles.css
input[type="submit"] {
  display: block;
  width: 60%;
  margin: 0 auto;
  height: 2em;
  font-size: 1.1rem;
  background-color: #3b3b4f;
  border-color: white;
}
```
> **Step 56** <br>
Lastly, for the submit button, you want to separate it from the `fieldset` above, and adjust its width to never be below `300px`.<br>
Change the `margin` property to include `1em` on the top and bottom, while leaving the right and left margins set to `auto`. Then set the width as described above.

```css
#styles.css
input[type="submit"] {
  display: block;
  width: 60%;
  margin: 0 auto;
  height: 2em;
  font-size: 1.1rem;
  background-color: #3b3b4f;
  border-color: white;
  margin-top: 1em;
  margin-bottom: 1em;
  margin-left: auto;
  margin-right: auto;
  min-width: 300px;
}
```
> **Step 57** <br>
Most browsers inject their own default CSS properties and values for different elements. If you look closely, you might be able to notice the file `input` is smaller than the other text `input` elements. By default, a `padding` of `1px 2px` is given to `input` elements you can type in.<br>
Using another attribute selector, style the `input` with a `type` of `file` to be the same padding as the other `input` elements.

```css
#styles.css
input[type="file"] {
  padding: 1px 2px;
}
```
> **Step 58** <br>
Speaking of `padding`, the submit button is sitting at the bottom of the `form` element. Add `2em` of `padding` only to the bottom of the `form`.

```css
#styles.css
form {
  width: 60vw;
  max-width: 500px;
  min-width: 300px;
  margin: 0 auto;
  padding-bottom: 2em;
}
```
> **Step 59** <br>
Last, but not least, change the text color of the `terms and conditions` link to `#dfdfe2`.<br>
> <br>
> Well done! You have completed the final part of the *Registration Form* practice project.

```css
#styles.css
a {
  color: #dfdfe2;
}
```