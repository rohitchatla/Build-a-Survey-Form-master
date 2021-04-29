<!-- Link to the working pen right [here](). -->

## The task 

> Build a survey form in which visitors can leave feedback on a certain subject.
>
> Project part of the FreeCodeCamp Beta curriculum: Applied Responsive Web Design Projects.

The purpose of this repository is to fulfill a challenge for the [Beta Curriculum](beta.freecodecamp.org) on FreeCodeCamp, namely building a **Survey Form** in which visitors can fill in their own information.

<!-- A project resembling [this one](https://codepen.io/freeCodeCamp/full/VPaoNP). A project fulfilling multiple conditions. -->

In particular, there ought to exist:

1. a title in between `h1` tags with `id="title"`;
2. a short explanation in between `p` tags with `id="description"`;
3. a `form` tag with `id="survey-form"`, which nests multiple elements.

  Multiple items among which:

  - a name field with `id="name"`
  - an email field with `id="email"` (accepting valid email addresses)
  - a number field with `id="number"` (accepting only numbers, in a range)

    For all input fields, there should be also a `label`, describing the respective elements. Each label should also have an appropriate id(s): `"name-label"`, `"email-label"`, `"number-label"`.

    Moreover, all input elements should contain `placeholder` text, hinting at the respectively accepted values.

  - a dropdown input with `id="dropdown"`
  - a menu consisting of `radio` buttons, with the same `name` attribute;
  - a menu consisting of `checkbox`es, with the same `name` attribute;
  - a `textarea` element, for additional comments;
  - a submit `button` with `id="submit"`.


There is not much space left for imagination in the creation of the project, but it is something which can be accepted for the nature of the task itself. A survey form should mostly retain standard practices to fulfill its purpose with the least amount of friction. Functionality overwhelms aesthetics and imaginative designs in this regard.

That being said, stylistic choices are still required for a readable font and color palette.

<!-- # Lessons learned 

## HTML

- input fields can be made mandatory with the **required**  attribute, directly declared in the input element itself:

  ```HTML
  <input ... required>
  ```

- input elements accept different **types** modifying the type of data to be accepted; in the project the following are used:

  - `text`; default value accepting all keystrokes;
  - `email`; forcing the email format *somebody@gmail.com*;
  - `number`; namely accepting numbers instead of string characters;
  - `checkbox`; prompting the checkbox interface;
  - `radio`; for radio buttons.

- labels paired to each input ought to have a **for** attribute matching the **id** of the respective input:

  ```HTML
  <label for="name">Name</label>
  <input id="name">
  ```

  The same is true in the fieldset element and in the dropdown menu, where labels match the select elements.

- in the dropdown menu it is possible to pre-select one of the options with the **selected** attribute:

  ```HTML
  <option selected></option>
  ```

- as the input + label elements in the fieldset are not nested in a block element, the radio buttons and checkboxes would be displayed inline; to avoid this issue introduce a line break **`<br>`** after each pair:


- for the dropdown menu and the fieldset alike, the input elements have the attributes of **name** and **value**. The former is used to identify the elemnt at a later stage (perhaps even in Javascript), while the latter is used to set the value associated with each option. Together they are used to identify which option was selected once the form is submitted.

- input of type text and numbers, as well as the textarea, have a placeholder attribute hinting at the type of data to be submitted. This is styled to be slightly transparent, by default.


## SCSS 

For several selectors, property-value pairs often repeat themselves. For instance, the following lines are repeated for input, select and even the textarea elements:

```SCSS
font-size: 1.1rem;
font-family: $font-family-text;
padding: 0.5rem;
border: none;
border-bottom: 1px solid darken($darker-color, 10%);
outline: none;
```

This is where **extend** can be used, defining the properties once and extending them on the required element. 

The challenge is to include properties that are connected together, such as font-family and font-size, in a single extend. This to avoid extremely specific extend values, applicable to only one custom scenario and to create extend statements with understandable purposes.

It is a minor specification for the small-scale project, but something of which to be aware when scaling up to larger files. For instance, the following two extends are declared atop the SCSS document:

```SCSS
%field-reset {
  border: none;
  outline: none;
}
%field-style {
  font-size: 1.1rem;
  font-family: $font-family-text;
  padding: 0.5rem;
  border-bottom: 1px solid darken($darker-color, 10%);
}
```

While they are applied together on multiple selectors, they are not merged in a single extend statement, exactly to fulfill the explained logic. One extend is used to reset some values, the other to style the elements. Each has its own purpose and reason for being.
 -->
