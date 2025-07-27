# 🍽️ Dynamic Recipe Viewer (PHP)

This is a beginner-friendly **PHP project** that allows users to dynamically select and view recipe content using a dropdown `<select>` form. Recipes are stored in HTML files and dynamically loaded with PHP based on user input.

---

## 📁 Project Structure

.
├── index.php # Main file with dropdown & logic
├── simple.css # Styling for form/UI
├── pages/
│ ├── citrus_salmon.html
│ ├── mediterranian_pasta.html
│ ├── sunset_risotto.html
│ └── tropical_tacos.html


---

## 🧠 Features

- 📜 Dynamic page loading using PHP `file_get_contents()`
- 🔒 Secure input using custom escaping function
- 📄 All recipe content modularly stored in separate `.html` files
- ✅ HTML form `<select>` remembers last selected item
- 🧼 Clean structure for beginners to understand PHP logic & HTML integration

---

## 🧰 PHP Concepts Used

### ✅ Functions:
- `function e($value)`  
  Custom function to **escape user input** using `htmlspecialchars()`, preventing XSS attacks.

### ✅ PHP Superglobals:
- `$_GET`  
  Used to get selected recipe value from the form.

### ✅ Array Handling:
- Associative array `$pages` used to map recipe `keys` to human-readable names.

### ✅ Conditional Logic:
- `if(!empty($_GET['page']))`  
  To check if a recipe has been selected.

- `if(array_key_exists($page, $pages))`  
  Prevents users from accessing unauthorized files.

### ✅ Built-in Functions:
- `htmlspecialchars()`  
  For safe output encoding.
- `file_get_contents()`  
  Reads and displays the content of the selected HTML file.

---

## 🎨 CSS (simple.css)

Basic styling for form and layout (optional – can be customized or replaced).

---

## 🧪 How to Run

1. Make sure you have a PHP server (like XAMPP or built-in `php -S localhost:8000`)
2. Place project in your `htdocs` or navigate to it via terminal
3. Run:
   ```bash
   php -S localhost:8000

---

### 🔥 Bonus Suggestion

If you'd like to **clean up even more**, rename `include.php` to `index.php` (which you already did here) so your form action becomes:

```php
<form method="GET" action="">
