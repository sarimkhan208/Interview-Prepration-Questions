# CSS Interview Questions

## 1) What are CSS selectors?
## 2) What are CSS variables?
## 3) What is Box Model?


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

## 3) What is Box Model?

The box model is a fundamental concept in CSS (Cascading Style Sheets) that describes how elements in a web page are rendered and how their dimensions and spacing are calculated.

According to the box model, every element in HTML is represented as a rectangular box. This box is composed of four main components:

1-> Content: It represents the actual content of the element, such as text, images, or other HTML elements. The content area is defined by the width and height properties.

2-> Padding: It is a transparent area surrounding the content and provides space between the content and the border. The padding area is controlled by the padding property and can be set independently for each side (top, right, bottom, left).

3-> Border: It is a line that surrounds the padding and content area. The border can have a specified width, style, and color, which are defined by the border property.

4-> Margin: It is a transparent area surrounding the padding, border, and content. The margin creates space between the element and adjacent elements or the containing element. The margin area is controlled by the margin property and can also be set independently for each side (top, right, bottom, left).


+-----------------------------------------------------------+
|                           Margin                          |
|                                                           |
|           +-----------------------------------+           |
|           |              Border               |           |
|           |                                   |           |
|           |         +-----------------+       |           |
|           |         |     Padding     |       |           |
|           |         |                 |       |           |
|           |         |                 |       |           |
|           |         +-----------------+       |           |
|           |         |    Content      |       |           |
|           |                                   |           |
|           +-----------------------------------+           |
|                                                           |
|                           Margin                          |
|                                                           |
+-----------------------------------------------------------+
