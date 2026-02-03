## Table of Contents

- [Forms in HTML](#forms-in-html)
  - [Input](#input)
  - [Label](#label)
  - [Placeholder](#placeholder)
- [Types of buttons](#diferent-types-of-buttons)
  - [Button](#button)
  - [Submit](#submit)
  - [Reset](#reset)
  - [Input](#input)
- [Client-side form validation](#client-side-form-validation-in-html)
  - [Required](#required)
  - [min and max length](#minlength-and-maxlength)
- [States in forms](#states-in-forms)
  - [Disable](#disable-state)
  - [Read only](#read-only)
- [Fieldset and legend](#fieldset-and-legend)
- [Name](#name)
- [Select options](#select-options)
- [Checkbox](#checkboxes)
- [Select and option elements](#select-and-options-elements)
- [Text area](#text-area)
- [Tables](#tables)
- [HTML Tools](#html-tools)
  - [HTML Validator](#html-validator)
- [HTML Tables summarize](#html-tables-summarize)


# Forms, Labels and Inputs in HTML

## Forms in HTML

Forms are used to gather information of the users.

```html

<form action="url-goes-here">
  <!-- input elements go here -->
</form>

```

The **action** attribute specifies where the form data will be sent upon submission.

### Input

The input element is used to collect the information.

```html

<form action="">
  <input type="text" />
</form>

```

The **type** element is the type of data which the input is expected for.

### Label

If you click in the text which is set as a label, automatically the cursor is going to focused in the input.

```html

<form action="">
  <label>
    Full Name:
    <input type="text" />
  </label>
</form>

```

When you nested the input inside the label, you have an association implicit between label and the input, but if you want have this association in an explicit way, you can put another attribute call **for**.

```html

<form action="">
  <label for="email"> Email Address: </label>
  <input type="email" id="email" />
</form>

```

### Placeholder

This is used to write something inside the input as an example which will deleted when you click on the input.

```html

<form action="">
  <label for="email"> Email Address: </label>
  <input type="email" id="email" placeholder="example@email.com" />
</form>

```

[⬆ Back to Table of Contents](#table-of-contents)

## Diferent types of buttons 

### Button

The first value for the attribute type is the **button**. Which is the default value.

```html

<button type="button">Show Alert</button>
<script src="index.js"></script>

```

This attribute doesn't do anything by default, just works if you add some JS code in it.

### Submit

```html

<form action="">
  <label for="email">Email address:</label>
  <input type="email" id="email" name="email" />
  <button type="submit">Submit form</button>
</form>

```

When the user click on the button the values that the forms has collected will be send to the server.

### Reset

```html

<form action="">
  <label for="email">Email address:</label>
  <input type="email" id="email" name="email" />
  <button type="reset">Reset form</button>
  <button type="submit">Submit form</button>
</form>

```

The form will be deleted when you click on the button with this value.

### Input

You can also set an input as a button, but is important to know that, is more recomended and brings you more flexibility use the button tag instead. That's because you can put, text, images, incons inside the button element.

```html

<input class="start-btn" type="button" value="Start Game" />
<script src="index.js"></script>

```

[⬆ Back to Table of Contents](#table-of-contents)

## Client side form validation in HTML

First of all, when we talking about client side, we're refering to the user's computer or device, so, there are a lot of ways to validate the correct fill of a form in the client side.

For real security sistems is important add validations to the client side and also give validation in the server side.

### Required

This attribute tells to the user that the fill have to filled before it gets submitted, otherwise even if you click on the button submit the form won't be send.

```html

<form action="">
  <label for="email">Email Address (Required field):</label>
  <input required type="email" name="email" id="email" />
  <button type="submit">Submit Form</button>
</form>

```

Inputs have some basic useful validation, for example if you set the attribute type as "email" you have to include a @ in the text, if you don't do that, an alert will be show tell you that is necessary this letter to send the form.

### Minlength and maxlength

You can set a maximum and a minimum of letters that you need in some gaps, if the user put less or more letters than needing, the form won't be send.

[⬆ Back to Table of Contents](#table-of-contents)

## States in forms

Is important to know the states of the inputs elements in forms, for example the default state is the form in blank, but when you click or tab on the input gap, this gap is going to get a border highlighted around the input, this is called the **focused** state.

```html

<input type="email" name="email" id="email" />

```

### Disable state

This state shows to the user that, it cannot be focused anymore.


```html

<input disabled type="email" name="email" id="email" />

```

### Read only

If you set your input with this attribute as its name says, you only can read the value inside the input. The valu is going to be written using the attribute **value**.

```html

<input
  readonly
  type="email"
  name="email"
  id="email"
  value="example@email.com"
/>

```
[⬆ Back to Table of Contents](#table-of-contents)

## Fieldset and legend

You can gruop inputs inside a fieldset, then you can also give them an name or caption using the tag legend.

```html

<form method="POST" action="https://hotel-feedback.freecodecamp.org">
        <fieldset>
          <legend>Personal Information</legend>
          <label for="full-name">Name (required):</label>
          <input>
        </fieldset>

```

[⬆ Back to Table of Contents](#table-of-contents)

## Name

The attribute name works to identify elements or data afther these have been sended.

```html

<input type="email" name="email">

```

[⬆ Back to Table of Contents](#table-of-contents)

## Select options

There are inputs where the user just have to click on one of them and this value will be send to the server, in this we are going to see one of those options in this case the radio button.

```html

<input type="radio" id="yes" name="first-time">
<label for="yes">Yes</label>
<input type="radio" id="no" name="first-time">
<label for="no">No</label>

```
In the previous example we can see that, both inputs have the same name, this is because you can select one of the two options, yes or not.

[⬆ Back to Table of Contents](#table-of-contents)

## Checkboxes

If you want a user to select multiple options from a list, not just one as we see in the previous type of selector you have to use the checkbox input.

```html

<fieldset>
  <legend>Food Options</legend>
  <input type="checkbox" id="pizza" name="food" value="pizza">
  <label for="pizza">Pizza</label>
  <input checked  type="checkbox" id="burger" name="food" value="burger">
  <label for="burger">Burger</label>
</fieldset>

```

The attribute value is what is going to be send to the server when you submit the form.

If you put the attribute **checked** in the input, the checkbox is going to checked by default.


[⬆ Back to Table of Contents](#table-of-contents)

## Select and options elements

You can use a dropdown if you want users make selections. This can be done using the select and option elements as follow.

```html

<label for="city">Choose a City: </label>
<select id="city" name="city">
  <option value="new-york">New York</option>
  <option value="los-angeles">Los Angeles</option>
  <option selected value="chicago">Chicago</option>
  <option value="miami">Miami</option>
</select>

```
If you want an option selected by default you have to put the attribute **selected** in any option.

[⬆ Back to Table of Contents](#table-of-contents)

## Text area

This input is used to create something like a box of comments or something like this, it allows you put more than one simple line in the input.

```html

<textarea id="comments" name="comments" rows="4" cols="50"></textarea>

```

The rows attribute is used to specify the visible height of the textarea, and the cols attribute is used to specify the visible width of the textarea.

[⬆ Back to Table of Contents](#table-of-contents)

## Tables

This tables aren't so used as before, but it is important to know that they exist and their elements.

```html

<table>
  <caption>Caption of this table</caption>
  <thead>
    <tr>
      <th>The title of this table</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>First Row</th>
      <td>
        First Data Cell
      </td>
    </tr>
    <tr>
      <th>Second Row</th>
      <td>
        Second Data Cell
      </td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>The footer of this table, which might contain date of publication, author credits, or other meta information.</th>
    </tr>
  </tfoot>
</table>

```

If you want to spand the for example two columns one caption, you can use the attribute colspan.

```html

<tr>
  <td colspan="3">Total Points</td>
</tr>

```

[⬆ Back to Table of Contents](#table-of-contents)

## HTML tools

### HTML validator

HTML is a forgiving languaje, elements still render even when you make mistakes as example, when you don't close a tag. This is when a HTML validator is usefull.

In this section we're going to show two fo the most popular HTML validators.

 - [validator.w3.org](https://validator.w3.org/)
 - [jsonformatter.org](https://jsonformatter.org/)

[⬆ Back to Table of Contents](#table-of-contents)

## HTML Tables summarize

In the next link there is a summarize of all the topics saw in this section.
 - [HTML tables summarize](https://www.freecodecamp.org/learn/responsive-web-design-v9/review-html-tables-and-forms/review-html-tables-and-forms)


[⬆ Back to Table of Contents](#table-of-contents)