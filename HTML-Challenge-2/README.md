# 📄 HTML-Challenge-2:<br>Accessible Planet Data Table

In this challenge, you're provided with raw data about the planets in our solar system. Your goal is to structure this data into a **clean, accessible HTML table** that is easy for students to read and navigate.

This challenge simulates a classroom use case where students are learning about planets and need factual data in a well-organized, semantic format. You'll use semantic HTML elements and accessibility best practices to ensure the table is screen reader-friendly and clearly structured.


---


### 1. ✅ Semantic HTML Table Structure

The table uses proper semantic tags for **structure and accessibility**:

* `<table>`: Defines the entire table.
* `<caption>`: Describes the table's purpose.
* `<thead>`, `<tbody>`: Separate the header and data for logical structure.
* `<th scope="col">`, `<th scope="row">`: Provide accessibility hints for screen readers.

✅ *Why?*
Semantic markup improves accessibility and makes the table easier to parse (both for users and machines).

---

### 2. 🧷 Sticky First Column (`position: sticky`)

To keep the **planet name column visible** during horizontal scrolling, we use:

```css
.sticky {
  position: sticky;
  left: 0;
  background-color: white;
  z-index: 1;
}
```

✅ *Why?*
Sticky positioning pins the column in place relative to the scroll container, allowing better UX on wide tables.

---

### 3. 🧱 First Column Border Styling

To apply a **continuous vertical border** to the sticky "planet name" column, we use:

```css
.sticky {
  border-right: 2px solid black;
}
```

✅ *Why?*
Using `border-right` on each cell (and `border-collapse: collapse` on the table) makes the column appear to have a single solid border.

---

### 4. 🖼️ Caption and Hyperlink Integration

The table includes a `<caption>` with a hyperlink to NASA's data source:

```html
<caption>
  Data about the planets of our solar system (Planetary facts taken from 
  <a href="https://nssdc.gsfc.nasa.gov/planetary/factsheet/">NASA's Planetary Fact Sheet</a>).
</caption>
```

✅ *Why?*
This gives context, attribution, and improves the accessibility of your data.

---

### 5. 🧠 Accessibility Best Practices

* Use of `<caption>` for screen readers.
* Use of `scope="col"` and `scope="row"` on `<th>` elements.
* Clear data hierarchy (groupings like "Terrestrial planets", "Gas giants").

---

### 6. 🔲 CSS Table Styling

The table uses classic layout and spacing styles:

```css
table {
  border-collapse: collapse;
  width: 100%;
}

th, td {
  border: 1px solid #ccc;
  padding: 0.5rem;
}
```

✅ *Why?*

* `border-collapse: collapse` creates seamless borders.
* Padding improves readability.
* Consistent borders create a clean layout.

---
