# CSS Interview Questions

## 1) What are CSS selectors?
## 2) What are CSS variables?


## 1) What are CSS selectors?


CSS selectors are patterns used to select and target specific HTML elements on a webpage. They allow you to apply styles and define rules to specific elements or groups of elements.

Here are some commonly used CSS selectors:

1-> Element Selector: Targets elements based on their HTML tag name. For example, p selects all <p> elements.

2-> Class Selector: Targets elements based on their class attribute. For example, .my-class selects all elements with class="my-class".

3-> ID Selector: Targets a single element based on its id attribute. For example, #my-id selects the element with id="my-id".

4-> Attribute Selector: Targets elements based on their attribute values. For example, [type="text"] selects all elements with type="text".

5-> Descendant Selector: Targets elements that are descendants of another element. For example, div p selects all <p> elements that are descendants of <div> elements.

6-> Child Selector: Targets elements that are direct children of another element. For example, ul > li selects all <li> elements that are direct children of <ul> elements.

7->  Adjacent Sibling Selector: Targets elements that are immediately preceded by another element. For example, h2 + p selects the <p> element immediately following an <h2> element.

8->  General Sibling Selector: Targets elements that are siblings of another element. For example, h2 ~ p selects all <p> elements that are siblings of an <h2> element.

## 2) What are CSS variables?
CSS variables, also known as CSS custom properties, are entities that allow you to store and reuse values in CSS. They provide a way to define reusable values and use them throughout your CSS code.

CSS variables are defined using the -- prefix followed by a name and a value. For example:

css
Copy code
:root {
  --primary-color: #ff0000;
}
In this example, --primary-color is a CSS variable with the value #ff0000, which represents a red color.

CSS variables can be used in any CSS property value by referencing them with the var() function. Here's an example of using the CSS variable in a color property:

css
Copy code
h1 {
  color: var(--primary-color);
}