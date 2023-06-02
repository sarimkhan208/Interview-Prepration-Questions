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


## 2) What are the features of HTML5?

HTML5 introduced several new features and enhancements over its predecessor, HTML4. Here are some of the key features of HTML5:

1-> Semantic Elements: HTML5 introduced new semantic elements like <header>, <footer>, <nav>, <article>, <section>, etc. These elements provide a clearer structure to web documents and improve accessibility and search engine optimization.

2-> Multimedia Support: HTML5 provides native support for multimedia elements without the need for third-party plugins. The <audio> and <video> elements allow embedding and controlling audio and video content directly within web pages.

3-> Canvas: HTML5 introduced the <canvas> element, which provides a drawing surface on which you can use JavaScript to render graphics, animations, charts, and other visualizations dynamically.

4-> Geolocation: HTML5 includes the Geolocation API, which enables web applications to retrieve the user's geographical location information (with the user's permission). This feature enables location-aware services and applications.

5-> Offline Web Applications: HTML5 introduced the concept of offline web applications through the Application Cache API. This allows web pages to be cached locally and accessed offline, providing a better user experience in situations with limited or no internet connectivity.

6-> Web Storage: HTML5 provides two mechanisms for client-side storage: localStorage and sessionStorage. These APIs allow web applications to store data locally on the user's device, providing a way to persist data beyond a single session or page reload.

7-> Web Workers: HTML5 introduced Web Workers, which allow running scripts in the background without affecting the user interface responsiveness. Web Workers enable parallel processing and can handle complex tasks without blocking the main execution thread.

8-> Form Enhancements: HTML5 introduced several new input types (e.g., date, email, number, range, search, etc.) and attributes to enhance form handling and validation. It also introduced the <datalist> element, which provides a list of predefined options for input fields.

9-> Drag and Drop: HTML5 introduced native support for drag and drop interactions. Developers can use the Drag and Drop API to allow users to drag elements and drop them in specific locations or targets within the web page.

10-> Improved Accessibility: HTML5 includes new features and attributes that improve accessibility, such as the <figure> and <figcaption> elements for providing captions and descriptions to multimedia content, the alt attribute for better image descriptions, and the aria-* attributes for defining roles and properties for accessibility purposes.

These are just some of the prominent features introduced in HTML5. The specification also brought other improvements like enhanced CSS support, better error handling, new APIs, and more.

## 3) What are the different types of storage in HTML5? 

HTML5 provides several types of storage options for web applications. Here are the different types of storage available in HTML5:

1-> Local Storage: Local Storage, also known as Web Storage or DOM Storage, allows web applications to store data persistently on the user's device. It provides a simple key-value storage mechanism that can be accessed by JavaScript. The data stored in Local Storage remains available even after the user closes the browser or restarts the device. The data limit for Local Storage is typically around 5MB per domain.

2-> Session Storage: Session Storage is similar to Local Storage, but the data stored in Session Storage is specific to a particular session or tab. Each tab or window within a browser has its own session storage, and the data is accessible only within that session. When the user closes the tab or window, the data stored in Session Storage is cleared. Session Storage is useful for maintaining session-specific data or temporary information.

3-> IndexedDB: IndexedDB is a powerful client-side database provided by HTML5. It allows web applications to store and retrieve structured data using a JavaScript API. IndexedDB provides a more advanced and flexible storage mechanism compared to Local Storage or Session Storage. It supports indexes for efficient data retrieval, transactions for handling data updates, and complex queries. IndexedDB is suitable for applications that require more robust data storage capabilities.

4-> Web SQL Database: Web SQL Database is a deprecated storage mechanism that provides a SQL database interface within the web browser. It allows web applications to store and retrieve data using SQL queries. Although it is no longer being actively developed, some browsers still support Web SQL Database.

5-> Cookies: Cookies are a traditional form of storage in web development. They are small text files stored on the user's device by the web browser. Cookies can be used to store small amounts of data that are sent back to the server with each request. They have limitations on data size (usually up to 4KB) and are primarily used for maintaining user sessions, remembering user preferences, and tracking user activities.

It's important to note that each type of storage has its own characteristics, limitations, and suitable use cases. Developers can choose the appropriate storage option based on the specific requirements of their web application.