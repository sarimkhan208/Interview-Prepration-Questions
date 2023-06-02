# HTML Interview Questions

## 1) How do you add CSS to an HTML webpage?
To add CSS (Cascading Style Sheets) to an HTML webpage, you have several options. Here are the most common ways:

Inline CSS: You can apply CSS directly to HTML elements using the style attribute. For example:
html


<p style="color: red; font-size: 16px;">This is a paragraph with inline CSS.</p>
Internal CSS: You can include CSS within the <style> tags in the <head> section of your HTML document. This allows you to define styles for multiple elements. For example:


<!DOCTYPE html>
<html>
<head>
    <style>
        p {
            color: red;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <p>This is a paragraph with internal CSS.</p>
</body>
</html>
External CSS: You can create a separate CSS file with a .css extension and link it to your HTML document using the <link> tag. This method is useful for maintaining clean and organized code, especially when you have multiple HTML pages that share the same styles. Here's an example:
Create a file named styles.css:


/* styles.css */
p {
    color: red;
    font-size: 16px;
}
Link the external CSS file in your HTML document:


<!DOCTYPE html>
<html>
<head>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
    <p>This is a paragraph with external CSS.</p>
</body>
</html>
Remember to specify the correct path in the href attribute to locate your CSS file correctly relative to your HTML file.

Using any of these methods, you can apply various CSS properties to style your HTML elements.


