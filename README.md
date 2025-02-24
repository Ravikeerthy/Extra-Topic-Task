### Semantic vs. Non-Semantic Tags in HTML

### Key Differences

| Feature        | Semantic Tags | Non-Semantic Tags |
|--------------|--------------|------------------|
| **Meaning**  | Clearly define their purpose | Do not indicate meaning |
| **Readability** | Easier for developers and search engines | Less meaningful without CSS |
| **SEO** | Helps in SEO optimization | Does not contribute to SEO |
| **Accessibility** | Better for screen readers | Requires additional ARIA attributes |

## When to Use What?
- Use **semantic tags** for better **SEO, accessibility, and readability**.
- Use **non-semantic tags** when **styling or grouping elements** where no specific meaning is required.

---

## Typography Properties in CSS

| Property        | Description |
|---------------|------------|
| `font-family`  | Specifies the typeface (e.g., Arial, Times New Roman) |
|`font-size`|  Defines the size of the text|
|`font-weight`|  Sets the thickness of the font (e.g., normal, bold)|
|`font-style`|   Defines the style (e.g., normal, italic, oblique)|
|`text-align`|  Aligns text (e.g., left, center, right)|
|`text-transform`|  Converts text to uppercase, lowercase, or capitalize|
|`letter-spacing`|   Controls the space between characters |
|`line-height`|   Sets the space between lines of text|
|`text-decoration`|   Adds effects like underline, overline, and line-through|
|`word-spacing`|   word-spacing|
| `font-variant`  | Controls small caps or normal text formatting |
| `text-indent`  | Specifies the indentation of the first line in a block of text |
| `text-overflow`  | Defines how overflowing text is handled (e.g., ellipsis) |
| `text-shadow`  | Adds shadow effects to text |
| `white-space`  | Specifies how white spaces inside an element are handled |
| `word-break`  | Defines how words should break when they exceed container width |



# CSS Box Model

## Box Model Diagram
```
+-------------------------------------+
|           Margin (Outside)          |
|  +-----------------------------+   |
|  |        Border (Edge)        |   |
|  |  +-----------------------+  |   |
|  |  |     Padding           |  |   |
|  |  |  +---------------+   |  |   |
|  |  |  |   Content    |   |  |   |
|  |  |  +---------------+   |  |   |
|  |  +-----------------------+  |   |
|  +-----------------------------+   |
+-------------------------------------+
```

## Definition
The **CSS Box Model** is a fundamental concept that defines how elements are displayed and spaced on a webpage. It consists of the following parts:

1. **Content** – The actual content inside the box (text, images, etc.).
2. **Padding** – Space between the content and the border.
3. **Border** – A boundary around the padding and content.
4. **Margin** – Space outside the border, separating the element from other elements.

Each part of the box model affects the total size of the element and how it interacts with other elements on the page.


---

# CSS Position Property

## Definition
The `position` property in CSS specifies how an element is positioned in a document. It has the following values:

1. **static** – Default position; elements are placed in the normal document flow.
2. **relative** – Positioned relative to its normal position.
3. **absolute** – Positioned relative to the nearest positioned (non-static) ancestor.
4. **fixed** – Positioned relative to the viewport, staying in the same place even when scrolling.
5. **sticky** – Toggles between `relative` and `fixed` depending on scroll position.

# CSS Flexbox

## Definition
Flexbox is a layout model that allows items in a container to be dynamically arranged, aligned, and distributed efficiently, even when their size is unknown or when the container size is changing.

---

## Flex Container Properties

These are the properties used to configure the behavior and layout of the flex container:

- `display`
- `flex-direction`
- `flex-wrap`
- `flex-flow`
- `justify-content`
- `align-items`
- `align-content`

---

### **1. `display` Property**
Defines the element as a flex container.

- **`display: flex`**: Enables the flex context for the container.
- **`display: inline-flex`**: Behaves like `display: flex` but the container is inline-level.

---

### **2. `flex-direction` Property**
Specifies the display direction of flex items in the flex container. It defines the primary axis of the layout.

- **`row`** (default): Items are arranged horizontally (left to right).
- **`column`**: Items are arranged vertically (top to bottom).
- **`row-reverse`**: Items are arranged horizontally (right to left).
- **`column-reverse`**: Items are arranged vertically (bottom to top).

---

### **3. `flex-wrap` Property**
Specifies whether flex items should wrap onto new lines if there's not enough room in the container on a single line.

- **`nowrap`** (default): Items will not wrap and will be placed in a single line.
- **`wrap`**: Items will wrap onto multiple lines when necessary.
- **`wrap-reverse`**: Items will wrap onto multiple lines in reverse order.

---

### **4. `flex-flow` Property**
A shorthand property for setting both `flex-direction` and `flex-wrap` properties.

- Example: `flex-flow: row wrap;` — This is equivalent to `flex-direction: row; flex-wrap: wrap;`.

---

### **5. `justify-content` Property**
Aligns the flex items along the main axis (horizontally by default).

- **`flex-start`** (default): Items are aligned at the start of the container.
- **`flex-end`**: Items are aligned at the end of the container.
- **`center`**: Items are centered within the container.
- **`space-between`**: Items are evenly spaced with no space at the start or end.
- **`space-around`**: Items are evenly spaced with equal space around them.
- **`space-evenly`**: Items are evenly spaced with equal space between them.

---

### **6. `align-items` Property**
Aligns items along the cross-axis (vertically by default).

- **`flex-start`**: Items are aligned to the top of the container.
- **`flex-end`**: Items are aligned to the bottom of the container.
- **`center`**: Items are aligned at the center of the container.
- **`baseline`**: Items are aligned based on their baseline.
- **`stretch`** (default): Items stretch to fill the container.

---

### **7. `align-content` Property**
Aligns the entire flex container's lines within the container when there is extra space on the cross-axis.

- **`flex-start`**: Lines are aligned at the top.
- **`flex-end`**: Lines are aligned at the bottom.
- **`center`**: Lines are aligned at the center.
- **`space-between`**: Lines are evenly distributed with no space at the start or end.
- **`space-around`**: Lines are evenly distributed with equal space around them.
- **`stretch`** (default): Lines stretch to fill the container.

---

## Flex Item Properties

These properties are used to control the layout and behavior of flex items within the flex container.

- `order`
- `flex-grow`
- `flex-shrink`
- `flex-basis`
- `flex`
- `align-self`

---

### **1. `order` Property**
Specifies the order in which a flex item appears within the flex container.

- **`order: 0`** (default): The default order value.
- **`order: 1`** (or any other number): Flex items are displayed in the specified order, with lower numbers appearing first.

---

### **2. `flex-grow` Property**
Defines the ability of a flex item to grow if necessary. It's a unitless value.

- **`flex-grow: 1`**: The item can grow and takes up remaining space.
- **`flex-grow: 0`** (default): The item does not grow.

---

### **3. `flex-shrink` Property**
Defines the ability of a flex item to shrink if necessary. It's a unitless value.

- **`flex-shrink: 1`**: The item can shrink to fit in the container.
- **`flex-shrink: 0`**: The item does not shrink.

---

### **4. `flex-basis` Property**
Specifies the initial size of a flex item before it is adjusted by `flex-grow` or `flex-shrink`.

- **`flex-basis: 100px`**: The item will start with a size of 100px.
- **`flex-basis: auto`** (default): The item will start with its natural size.

---

### **5. `flex` Property**
A shorthand property for setting `flex-grow`, `flex-shrink`, and `flex-basis` all at once.

- Example: `flex: 1 1 100px;` — This is equivalent to `flex-grow: 1; flex-shrink: 1; flex-basis: 100px;`.

---

### **6. `align-self` Property**
Allows individual flex items to override the `align-items` property and align themselves along the cross-axis.

- **`align-self: auto`** (default): Inherits alignment from `align-items`.
- **`align-self: flex-start`**: Aligns the item to the top.
- **`align-self: flex-end`**: Aligns the item to the bottom.
- **`align-self: center`**: Aligns the item at the center.
- **`align-self: baseline`**: Aligns the item based on its baseline.
- **`align-self: stretch`**: Stretches the item to fill the container.


# CSS Grid

## Definition
CSS Grid Layout is a powerful two-dimensional layout system for the web. It allows you to design complex web layouts with rows and columns, making it easier to place elements into a grid structure.

---

## Grid Container Properties

These properties are used to configure the behavior and layout of the grid container.

- `display`
- `grid-template-columns`
- `grid-template-rows`
- `grid-template-areas`
- `grid-gap`
- `grid-column-gap`
- `grid-row-gap`
- `justify-items`
- `align-items`
- `justify-content`
- `align-content`

---


### **CSS Animations**


# CSS Animations

## Definition
CSS animations allow you to create smooth transitions between different states of an element over a specified period.

---

## Animation Properties

These are the properties used to control the animation behavior.

- `@keyframes`
- `animation`
- `animation-name`
- `animation-duration`
- `animation-timing-function`
- `animation-delay`
- `animation-iteration-count`
- `animation-direction`
- `animation-fill-mode`
- `animation-play-state`

---


### **CSS Media Queries**

## Definition
Media Queries allow you to apply different styles depending on the conditions like the screen size, device type, or resolution.

---






