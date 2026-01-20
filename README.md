# Web Page Code Explanation

This document provides a line-by-line explanation of `index.html` and `styles.css`, including full forms for all abbreviations and technical terms.

---

## 📄 index.html (HyperText Markup Language)

HTML stands for **HyperText Markup Language**. It is the standard markup language for documents designed to be displayed in a web browser.

### Line-by-Line Breakdown

1. `<!DOCTYPE html>`
   - **Full Form:** DOCTYPE = Document Type.
   - **Explanation:** Tells the web browser that this is an **HTML5** document.

2. `<html lang="en">`
   - **Full Form:** lang = Language, en = English.
   - **Explanation:** The root element. The `lang="en"` attribute specifies that the content is in English for SEO and accessibility.

3. `<head>`
   - **Explanation:** A container for metadata (data about the HTML document) that isn't displayed on the page.

4. `<meta charset="UTF-8" />`
   - **Full Form:** meta = Metadata, charset = Character Set, UTF-8 = 8-bit Unicode Transformation Format.
   - **Explanation:** Sets the character encoding to UTF-8, which supports almost all characters and symbols in the world.

5. `<meta name="viewport" content="width=device-width, initial-scale=1.0" />`
   - **Explanation:** Configures the **viewport** (the visible area of a web page). `width=device-width` sets the width to follow the screen-width of the device, and `initial-scale=1.0` sets the initial zoom level.

6. `<title>Simple Form</title>`
   - **Explanation:** Sets the title of the web page shown on the browser tab.

8. `<link rel="stylesheet" href="styles.css" />`
   - **Full Form:** rel = Relationship, href = Hypertext Reference.
   - **Explanation:** Links the external CSS file (`styles.css`) to this HTML file.

10. `<style>`
    - **Explanation:** Starts an internal CSS block to style elements directly inside HTML.

11-13. `input { border-radius: 6px; }`
    - **Explanation:** targets `<input>` elements and gives them rounded corners of 6 pixels. The comment notes it overrides the external stylesheet.

14. `</style>`
    - **Explanation:** Closes the internal style block.

15. `</head>`
    - **Explanation:** Closes the head section.

17. `<body>`
    - **Explanation:** Contains the visible content of the web page.

18. `<h1 style="margin-top: 0">User Registration</h1>`
    - **Full Form:** h1 = Heading Level 1.
    - **Explanation:** A main heading. Inline CSS is used to remove the top margin.

20. `<form action="#">`
    - **Explanation:** Creates a form. `action="#"` is a placeholder for where the data should be sent (currently nowhere).

21. `<div class="input-group">`
    - **Full Form:** div = Division.
    - **Explanation:** A container used to group the label, input, and error message together.

22. `<label for="name">Name:</label>`
    - **Explanation:** Provides a label for the input field. The `for` attribute links it to the input with `id="name"`.

23-30. `<input type="text" id="name" name="name" ... required />`
    - **Full Form:** id = Identifier.
    - **Attributes:**
      - `type="text"`: Standard text input.
      - `placeholder`: Text displayed inside the field before the user types.
      - `pattern`: A regular expression (Regex) that restricts input to letters and spaces (2-50 characters).
      - `required`: Makes the field mandatory.

31-33. `<span class="error-message" data-error="name">...</span>`
    - **Explanation:** A container for the error message that shows up if the input is invalid.

36-50. **Age Input Group**
    - `type="number"`: Restricts input to numbers.
    - `min="18"` / `max="120"`: Sets the allowed range for the age.

52-64. **Email Input Group**
    - `type="email"`: Ensures the input follows a standard email format (e.g., name@domain.com).

66-72. `<button type="submit" ...>Submit</button>`
    - **Explanation:** A button that sends (submits) the form data. Inline styles change its color.

73. `<button type="reset" class="btn">Reset</button>`
    - **Explanation:** A button that clears all fields in the form back to their default values.

74. `</form>`
    - **Explanation:** Closes the form.

75. `</body>`
    - **Explanation:** Closes the body.

76. `</html>`
    - **Explanation:** Closes the HTML document.

---

## 🎨 styles.css (Cascading Style Sheets)

CSS stands for **Cascading Style Sheets**. It is used to describe the presentation (look and formatting) of the HTML document.

### Line-by-Line Breakdown

1-3. `h1 { text-decoration: underline; }`
   - **Explanation:** Underlines all `<h1>` headings.

6-11. `body { ... }`
   - **font-family: sans-serif**: Uses a clean font without small "feet" (serifs) on the letters.
   - **padding: 40px**: Adds space inside the border (40 pixels).
   - **max-width: 400px**: Limits the width of the content to 400 pixels.
   - **margin: auto**: Centers the content horizontally on the screen.

13-17. `form { ... }`
   - **display: flex**: Uses Flexbox (Flexible Box Layout) to arrange items.
   - **flex-direction: column**: Stacks form items on top of each other.
   - **gap: 15px**: Adds 15 pixels of space between each item in the form.

20-24. `.input-group { ... }`
   - **Explanation:** Stacks labels and inputs vertically with a 5px gap.

26-31. `input { ... }`
   - **padding: 8px**: Space inside the input box.
   - **font-size: 16px**: Size of the text.
   - **border: 2px solid #aaaaaa**: A gray border, 2 pixels thick.
   - **border-radius: 10px**: Rounds the corners of the input box by 10 pixels.

34-38. `.error-message { ... }`
   - **color: #f44336**: A shade of red for errors.
   - **display: none**: Hides the error message by default.

41-43. `input:invalid ~ .error-message { display: block; }`
   - **Explanation:** If an input is invalid (e.g., name is too short), find the next(`.error-message`) and show it (`display: block`).

46-48. `input:invalid { border-color: red; }`
   - **Explanation:** Changes the border to red if the input data is incorrect.

50-52. `input:valid { border-color: green; }`
   - **Explanation:** Changes the border to green if the input data is correct.

55-62. `.btn { ... }` (Common button styles)
   - **cursor: pointer**: Changes the mouse cursor to a hand icon when hovering.
   - **border: none**: Removes the default browser border.

65-67. `button[type="submit"] { background-color: blue; }`
   - **Explanation:** Specifically styles the submit button with a blue background.

70-73. `button[type="reset"] { background-color: red; }`
   - **Explanation:** Specifically styles the reset button with a red background.

75-77. `.btn:hover { opacity: 0.8; }`
   - **Explanation:** Makes the button slightly transparent (80%) when the mouse hovers over it, giving feedback to the user.

---

## 📚 Glossary of Terms

| Term/Abbreviation | Full Form | Meaning |
| :--- | :--- | :--- |
| **HTML** | HyperText Markup Language | The structure of the web page. |
| **CSS** | Cascading Style Sheets | The design/style of the web page. |
| **UTF-8** | 8-bit Unicode Transformation Format | Character encoding for text. |
| **PX** | Pixel | A tiny dot on the screen, used for measuring size. |
| **ID** | Identifier | A unique name given to an element. |
| **H1** | Heading Level 1 | The most important heading on a page. |
| **REL** | Relationship | Defines the relationship between the linked file and the HTML. |
| **HREF** | Hypertext Reference | The address/path to a file (like a link). |
| **META** | Metadata | Data that describes other data. |
| **DIV** | Division | A generic container for grouping elements. |
| **HEX** | Hexadecimal | A color code starting with `#` (e.g., `#aaaaaa`). |
