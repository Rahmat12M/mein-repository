Question 1: What are void elements? Give two examples.
anwort :**Void elements** are HTML elements that **do not have any content** and **do not require a closing tag**. They are self-contained and are typically used to insert something into the document, like a line break or an image.

### Two examples of void elements:

1. `<br>` – Inserts a line break in the text.
2. `<img>` – Embeds an image in the HTML page.

These elements are written without a closing tag, like this:

```html
<br>
<img src="image.jpg" alt="Description">
```

Question 2: Does an element inherit the border property from its parent by default?
**No**, an element does **not inherit** the `border` property from its parent by default.

In CSS, the `border` property is **not an inherited property**, which means child elements **do not automatically receive** the border styles of their parent unless it's explicitly specified.

If you want a child element to inherit the border, you can use:

```css
border: inherit;
```

This tells the child element to inherit the `border` from its parent.

Question 3: Is #example a valid CSS class selector?
**No**, `#example` is **not** a valid **CSS class selector** — it is a **CSS ID selector**.

### Explanation:

* `#example` targets an element with the attribute `id="example"`.
* A **class selector** uses a dot (`.`), like `.example`, which targets elements with `class="example"`.

### Examples:

* **ID selector:**

  ```css
  #example {
    color: red;
  }
  ```

  Applies to: `<div id="example">`

* **Class selector:**

  ```css
  .example {
    color: blue;
  }
  ```

  Applies to: `<div class="example">` ✅

So, if you're trying to select a class, you should use `.example`, not `#example`.

Question 4: Explain the difference between block and inline elements.
The main difference between **block** and **inline** elements in HTML lies in how they behave in the layout:

---

### 🔷 **Block Elements**:

* Start on a **new line**.
* Take up the **full width** available by default.
* Can contain **other block or inline elements**.
* Commonly used for **structuring** the layout.

**Examples:**
`<div>`, `<p>`, `<h1>` to `<h6>`, `<section>`, `<article>`

**Example Behavior:**

```html
<p>This is a paragraph.</p>
<p>This is another paragraph.</p>
```

These paragraphs will appear on separate lines.

---

### 🔹 **Inline Elements**:

* Do **not start on a new line**.
* Only take up as much **width as necessary**.
* Can **only contain text or other inline elements** (no block elements inside).
* Commonly used for **formatting** small parts of content.

**Examples:**
`<span>`, `<a>`, `<strong>`, `<em>`, `<img>`

**Example Behavior:**

```html
<p>This is <strong>bold</strong> and <em>italic</em> text.</p>
```

The text remains on the same line.

---

### Summary Table:

| Feature            | Block Elements   | Inline Elements    |
| ------------------ | ---------------- | ------------------ |
| Starts on new line | ✅ Yes            | ❌ No               |
| Takes full width   | ✅ Yes            | ❌ No (only needed) |
| Can contain blocks | ✅ Yes            | ❌ No               |
| Common use         | Layout structure | Text formatting    |



Question 5: What is the color red in hex, RGB, and HSL?
The color **red** can be represented in different color formats as follows:

---

### 🔹 **Hex (Hexadecimal):**

```css
#FF0000
```

* `FF` = 255 (Red)
* `00` = 0 (Green)
* `00` = 0 (Blue)

---

### 🔸 **RGB (Red, Green, Blue):**

```css
rgb(255, 0, 0)
```

* Maximum red, no green, no blue.

---

### 🔸 **HSL (Hue, Saturation, Lightness):**

```css
hsl(0, 100%, 50%)
```

* **Hue**: 0° (Red starts at 0° on the color wheel)
* **Saturation**: 100% (fully saturated)
* **Lightness**: 50% (normal brightness)


Question 6: Explain the box model and its relation to outline.
### ✅ **The CSS Box Model**

The **box model** is a fundamental concept in CSS that describes how elements are structured and spaced on a web page. Every HTML element is treated as a **box**, made up of four main parts:

---

### 🔹 1. **Content**

The actual content (text, image, etc.) inside the element.

### 🔹 2. **Padding**

The space **between** the content and the border. It’s **inside** the element.

### 🔹 3. **Border**

A line that wraps around the padding and content.

### 🔹 4. **Margin**

The space **outside** the border. It separates the element from others.

---

### 📦 **Box Model Diagram:**

```
+---------------------------+
|        Margin             |
|  +---------------------+  |
|  |      Border         |  |
|  |  +---------------+  |  |
|  |  |   Padding     |  |  |
|  |  | +-----------+ |  |  |
|  |  | | Content   | |  |  |
|  |  | +-----------+ |  |  |
|  |  +---------------+  |  |
|  +---------------------+  |
+---------------------------+
```

---

### 🟥 **What is Outline and How Is It Related?**

The **`outline`** is ***not* part of the box model**, but it's a visual effect **similar to the border**.

#### Key Differences Between `border` and `outline`:

| Feature            | `border`                     | `outline`                  |
| ------------------ | ---------------------------- | -------------------------- |
| Part of box model? | ✅ Yes                        | ❌ No                       |
| Affects layout?    | ✅ Yes (takes space)          | ❌ No (does not take space) |
| Can be rounded?    | ✅ Yes (with `border-radius`) | ❌ No                       |
| Position           | Surrounds the padding        | Drawn outside the border   |

---

### 🔸 Example CSS:

```css
.box {
  padding: 20px;
  border: 2px solid blue;
  outline: 3px dashed red;
}
```

This will show:

* A blue border around the padding,
* And a red dashed outline *outside* the border, without affecting layout.


Question 7: Explain border-radius: 1em 1em 3em 1em.
### ✅ `border-radius: 1em 1em 3em 1em` — Explained

This CSS shorthand sets the **rounded corners** of an element, using **4 values** to define the **horizontal radii** (left-to-right curvature) of each corner:

---

### 🔹 Order of Values:

```css
border-radius: top-left top-right bottom-right bottom-left;
```

So this:

```css
border-radius: 1em 1em 3em 1em;
```

Means:

* **Top-left corner:** `1em`
* **Top-right corner:** `1em`
* **Bottom-right corner:** `3em`
* **Bottom-left corner:** `1em`

---

### 🔸 What does `1em` mean?

* `1em` is a **relative unit** based on the element’s font size.
* If the font size is `16px`, then `1em = 16px`.

---

### 🔹 Visual Effect:

* All corners will be slightly rounded **except the bottom-right**, which will be **more rounded** because of the `3em` radius.

---

### 🔍 Bonus: You can also define **elliptical** corners using a slash:

```css
border-radius: 1em 2em 3em 4em / 0.5em 1em 1.5em 2em;
```

This sets **horizontal / vertical** radii for each corner separately.


