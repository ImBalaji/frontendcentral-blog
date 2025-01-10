---
title: 'Level Up Your Forms With Essential HTML Form Attributes for a User-Friendly Experience'
date: 2024-06-17T10:30:03+00:00
description: 
keywords: [HTML form attributes, form usability, autocomplete attribute, novalidate attribute, formnovalidate attribute, formenctype attribute, inputmode attribute, user experience, web forms]
tags: ["HTML5", "Web Design", "UX Design", "Web Forms"]
author: ["Balaji"]
draft: false
# images: 
# weight: 1   #Post can be pinned/ displayed top on the list by adding a weight=<num> var to page-variables
# aliases: ["/first"]
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
---

The HTML `<form>` element is an **essential feature** for websites, enabling interaction and information gathering from users. However, the `<form>` element alone is merely a structural component; it becomes truly powerful and functional through the use of various attributes. These attributes enhance the form's usability, accessibility, and overall user experience.

_Understanding and effectively utilizing **form attributes** can greatly improve how users interact with your website._ From providing autofill suggestions to ensuring data security, these attributes play a crucial role in modern web development. In this blog post, we will explore some of the most interesting and useful HTML form attributes, demonstrating how they can transform a basic form into a sophisticated and user-friendly interface.


## HTML5 Form Attributes and Their Applications

## `autocomplete`: 
  ### What is `autocomplete` attribute?
  Imagine encountering login forms on social media or during e-commerce checkout processes where the browser remembering and automatically fills in your username and password, expediting access and transactions.  
  
  The `autocomplete` attribute in HTML forms plays a crucial role in enhancing user experience(UX) by leveraging stored data to swiftly populate fields, reducing the time and potential for errors when filling out forms.

  **Syntax:**
  ```html{linenos=table}
    <input type="text" autocomplete="on">
    <input type="text" autocomplete="off">
  ```
  ### `autocomplete` attribute values:
  `on`: The browser fetches stored data and may automatically complete entries.  

  `off`: The browser may not automatically complete entries.   

  `Field-specific values`: Specify the type of <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/autocomplete#token-list" target="_blank" rel="noopener noreferrer" title="MDN document on autofill detail tokens">data expected</a> (e.g., name, email, address-line1, postal-code).
  
  ### Example:

  ```html{linenos=table}
  <form action="/submit" method="post" autocomplete="on">

    <label for="name">Name:</label>
    <input type="text" id="name" name="name" autocomplete="name"><br>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" autocomplete="email"><br>
    
    <label for="address">Address:</label>
    <input type="text" id="address" name="address" autocomplete="address-line1"><br>
    
    <label for="city">City:</label>
    <input type="text" id="city" name="city" autocomplete="address-level2"><br>
    
    <label for="state">State:</label>
    <input type="text" id="state" name="state" autocomplete="address-level1"><br>
    
    <label for="zip">Zip Code:</label>
    <input type="text" id="zip" name="zip" autocomplete="postal-code"><br>
    
    <label for="phone">Phone Number:</label>
    <input type="tel" id="phone" name="phone" autocomplete="tel"><br>
    
    <input type="submit" value="Submit">
  </form>
  ``` 

<div class="did-you-know">
<h3>Did You Know</h3>
<ol>
<li><strong>Security Considerations</strong>
 <p>Use <code><strong><span style="text-transform: lowercase">autocomplete="off"</span></strong></code> for sensitive fields like credit card information or password fields to prevent unauthorized autofill.</p></li>

<li><strong>Uniform User Experience</strong>
 <p>Ensure autocomplete attributes are consistently used across your forms to provide a uniform user experience.</p></li>
</ol>
</div>

<br>  

## `novalidate`:
  ### What is `novalidate` attribute?
  The `novalidate` attribute disables the browser's default validation behavior when a form is submitted. Normally, browsers validate form fields based on HTML5 attributes such as `required`, `minlength`, `maxlength`, and `type` (e.g., number, email, tel), or patterns defined by regular expressions. By using the `novalidate` attribute, you can bypass this automatic validation, allowing the form to be submitted without the browser checking these constraints.  

  **Syntax:**
  ```html{linenos=table}
    <form action="/action_page.php" novalidate>
      <input type="email" id="email" name="email" required>
      <input type="submit">
    </form>
  ```
    
  ### Scenarios Where Disabling Default Browser-Based Validation is Beneficial    
  - **Custom Validation Logic in JavaScript:**  When your form requires complex validation logic that cannot be achieved using HTML5 attribute, using `novalidate` attribute allows implement these checks with JavaScript.  
  - **Unified Error Handling throughout application:** Custom validation allows for unified error handling approach, ensuring that error messages and styles are consistent user experience throughout the website.  
  - **Integration with JS Libraries and Frameworks:** React, Vue JS frameworks often come with their own validation logic. Using `novalidate` can prevent conflicts between the browser's validation and the framework's validation logic.  
  - **Backend Validation:** When your business logic requires server-side validation to be the primary form of validation, using `novalidate` ensures that the server handles all validation and thus avoid confusing the user by not showing conflicting validation messages.  
  - **Validating Multi-Step Forms:** In multi-step forms, you might want to validate inputs only when the user navigates to the next step. Disabling browser validation prevents it from submitting the form at intermediate steps.  

  ### Example: Custom Validation Logic
  Example of a form that uses novalidate to implement custom JavaScript validation:

  #### HTML:
  ```html{linenos=table}
  <!-- `form` element with `novalidate` attribute -->
  <form action="/submit.php" method="post" novalidate>

    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required><br>
    
    <label for="password">Password:</label>
    <input type="password" id="password" name="password"><br>
    
    <input type="submit" value="Login" onclick="validateForm(event)">
  </form>
  ```
  #### JavaScript:  
  ```javascript{linenos=table}
  <script>
    function validateForm(event) {
      event.preventDefault(); // Prevent the default form submission
      
      var email = document.getElementById('email').value;
      var password = document.getElementById('password').value;
      var errorMessage = '';

      // Custom validation logic
      if (!email) {
        errorMessage += 'Please enter your email.\n';
      } else if (!validateEmail(email)) {
        errorMessage += 'Please enter a valid email address.\n';
      }

      if (!password) {
        errorMessage += 'Please enter your password.\n';
      } else if (password.length < 6) {
        errorMessage += 'Password must be at least 6 characters long.\n';
      }

      if (errorMessage) {
        alert(errorMessage);
        return false;
      }
      // If validation passes, submit the form
      document.querySelector('form').submit();
    }

    function validateEmail(email) {
      var re = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      return re.test(email);
    }
  </script>
  ```  
<br>

## `formnovalidate`:
  ### What is `formnovalidate` attribute?
  The `formnovalidate` attribute in HTML is used to **disable form validation for a specific input element** within a form. This attribute provides granular control, allowing you to decide which submit actions trigger validation and which do not, without disabling validation for the entire form.  

  The `formnovalidate` attribute can be applied to `<button>`, `<input type="submit">`, or `<input type="image">` elements within a form.
    
  **Syntax:**
  ```html
  <input type="submit" formnovalidate>
  ```  
  <br>

  ### Key Difference between `novalidate` and  `formnovalidate` attributes:

<figure>

|                  | `novalidate` Attribute | `formnovalidate` Attribute |
|--------------------------|------------------------|----------------------------|
| **Applied To**           | `<form>` element         | `<button>`, `<input type="submit">`, or `<input type="image">` elements within a form. |
| **Effect**                | Disables browser validation for the entire form. | Disables browser validation for the specific form element (e.g., submit button). |
| **Overrides `novalidate`** | Not Applicable                     | Yes. If `formnovalidate` is present on a submit button within a form with `novalidate`, the submit button will be validated despite the form-level `novalidate`. |
| **Use Case**              | <ul> <li>Custom validation logic</li> <li>Multi-step forms</li><li>Server-Side Validation</li></ul>  | <ul> <li>Submitting incomplete data (e.g., draft forms)</li><li>Disabling validation for specific elements</li></ul> |  

<figcaption >Table outlining the difference between `novalidate` and `formnovalidate`:</figcaption>
</figure>  

 ### Example with `formnovalidate` attribute
 Consider an event registration form where users can either submit the form for validation or save their progress:

```html{linenos=table}
<form action="/registerForm.php" method="post">
  <label for="firstname">First Name:</label>
  <input type="text" id="firstname" name="firstname" required><br>
  
  <label for="lastname">Last Name:</label>
  <input type="text" id="lastname" name="lastname" required><br>
  
  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required><br>
  
  <label for="phone">Phone Number:</label>
  <input type="tel" id="phone" name="phone"><br>
  
  <!-- Submit the form -->
  <button type="submit">Submit Registration</button>

  <!-- Save and Continue with `formnovalidate` attribute -->
  <button type="submit" formnovalidate>Save and Continue Later</button>
</form>
```
<br>

## `formenctype`:
  ### What is `formenctype` attribute?
  The `formenctype` attribute in HTML specifies how the content of form data should be encoded into a specific <a href="https://en.wikipedia.org/wiki/Media_type" title="What is MIME(Multipurpose Internet Mail Extensions) type" target="_blank" rel="noopener noreferrer">MIME type</a> before it is submitted to the server.  

  The `formenctype` attribute can be applied to `<button>`, `<input type="submit">`, or `<input type="image">` elements within a form.

  **Syntax:**
  ```html
  <button type="submit" formenctype="value">
  ```

  ### Possible Values for `formenctype` are: 

  1. **`application/x-www-form-urlencoded`**:
      This is the _default_ encoding type used by HTML forms. When a form is submitted with `application/x-www-form-urlencoded`, the form data is URL-encoded before being sent in the HTTP request body. Here are some key points about this encoding type:  
      
      - **Data Format**: Data is encoded as _**key-value pairs**_ separated by `&` symbols, with keys and values URL-encoded (spaces become `+` and special characters are percent-encoded).
      - **Usage**: Suitable for submitting simple forms and data where the content type is primarily textual.

      **Example**:
      ```HTTP
      name=Balaji+Muralidharan&age=33&city=Chennai
      ```
    
  2. **`multipart/form-data`**:
      This encoding type is used when submitting forms that include files, such as file uploads. It allows for binary data to be sent in addition to textual form data. Key points include:

      - **Data Format**: The request body is divided into parts, each with a content type specified for the type of data it contains (`text/plain`, `image/jpeg`, etc.).
      - **Usage**: Essential for file uploads as it supports binary data and allows for large files to be sent.

      **Example**:
      ```HTTP
      Content-Disposition: form-data; name="name"

      Balaji Muralidharan

      Content-Disposition: form-data; name="avatar"; filename="avatar.jpg"
      Content-Type: image/jpeg

      (binary data for the image file)
      ```
    
  3. **`text/plain`**:
      This encoding type is straightforward and sends the data as plain text. It's less commonly used for form submissions but can be useful in specific scenarios:

      - **Data Format**: The entire body of the HTTP request is treated as plain text.
      - **Usage**: Suitable for sending textual data where no formatting or special handling of form fields is required.
      
      **Example**: 
      ```HTTP
      name=Balaji Muralidharan
      age=33
      city=Chennai
      ```

### Comparison of HTTP Request Encoding Types:

<figure>
  
| Encoding Type                        | Description                                                                                      | Usage                                                                                         | Practical Considerations                                                                                      |
|--------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| `application/x-www-form-urlencoded` | Encodes form data as _**key-value**_ pairs in a URL-encoded format.                                      | Simple forms where textual data is sufficient.                                  | <ul><li>Best for small amounts of data.</li><li>Automatically converts spaces to `+` and encodes special characters.</li><li>Limited by URL length restrictions in GET requests.</li> </ul>                                                                           |
| `multipart/form-data`                | Supports forms that include binary data, such as file uploads.                                      | File uploads and complex forms requiring binary data.                                            | <ul><li>Essential for file uploads.</li><li>Uses multipart boundaries to separate different data parts.</li><li>Slightly more complex to handle on the server-side compared to URL-encoded forms.</li></ul>                          |
| `text/plain`                         | Sends data as plain text without any special formatting or encoding.                                | Basic textual data submissions.                                                                 | <ul><li>No automatic encoding of special characters.</li><li>Less secure as data is sent in raw format.</li><li>Suitable for debugging or simple data transmission where formatting isn't needed.</li></ul>                                          |

<figcaption>Table showing comparison of different HTTP Request Encoding Types</figcaption>
</figure>


## `inputmode`:
  ### What is `inputmode` attribute?
  The `inputmode` attribute is an enumerated attribute that specifies the type of virtual keyboard that should be displayed on touchscreen devices when a user interacts with an input field. This attribute helps browsers optimize the keyboard layout based on the expected input type, improving user experience and input efficiency.

  The `inputmode` attribute is primarily used with `<input>` element.

  **Syntax:**  
  ```html
  <input type="text" inputmode="numeric">
  ```

  ### Possible Values for `inputmode`

The `inputmode` attribute can take several values to specify different types of input methods:

- **`none`**: Indicates that the field should not present any special keyboard layout.
- **`text`**: The default value, suitable for any text input.
- **`tel`**: Optimizes for telephone number input, with a numeric keypad that includes symbols like `+` and `-`.
- **`url`**: Optimizes for entering URLs, including keys like `.`, `/`, and `.com`.
- **`email`**: Optimizes for entering email addresses, including keys like `@` and `.`.
- **`numeric`**: Optimizes for numeric input, typically displaying a numeric keypad.
- **`decimal`**: Optimizes for decimal numeric input, with a decimal point and numeric keypad.
- **`search`**: Optimizes for search input, including keys like `⌘` (Command on macOS) and `↵` (Enter).

### Practical Examples:

1. **Telephone Number Input**: 
    ```html
    <input type="tel" inputmode="tel" placeholder="Enter phone number">
    ```

2. **URL Input**: 
    ```html
    <input type="url" inputmode="url" placeholder="Enter website URL">
    ```

3. **Numeric Input**: 
    ```html
    <input type="number" inputmode="numeric" placeholder="Enter number">
    ```

4. **Email Address Input**: 
    ```html
    <input type="email" inputmode="email" placeholder="Enter email">
    ```

5. **Search Input**: 
    ```html
    <input type="search" inputmode="search" placeholder="Search...">
    ```