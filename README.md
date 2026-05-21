# Quotes App

A simple JavaScript DOM project that fetches quotes from a public API and displays them dynamically in a list. Users can also add their own quotes and remove them by clicking on them.

## Features

- Fetches quotes from a public API
- Dynamically renders quotes in the DOM
- Add custom quotes
- Remove quotes by clicking on them
- Responsive UI using Tailwind CSS

## Technologies Used

- HTML
- CSS
- JavaScript (Vanilla JS)
- Fetch API
- Tailwind CSS

## Project Structure

```
project/
│
├── index.html
├── style.css
└── README.md
```

## How It Works

### Fetching Quotes

The application sends a GET request to a public quotes API:

```javascript
fetch('https://api.freeapi.app/api/v1/public/quotes?page=1&limit=10&query=human')
```

The response is converted from JSON into a JavaScript object:

```javascript
response.json()
```

Each quote is then rendered as a new `<li>` element and appended to the list.

### Adding Quotes

Users can type a quote into the input field and click the Create button.

A new list item is created dynamically:

```javascript
const li = document.createElement('li');
```

The quote is inserted into the element:

```javascript
li.innerText = value;
```

The element is added to the DOM:

```javascript
ulRef.appendChild(li);
```

### Removing Quotes

Each created quote receives a click event listener:

```javascript
li.addEventListener('click', function(){
    li.remove();
});
```

Clicking a quote removes it from the DOM.

---

# DOM Concepts Learned

## DOM Selection

Selecting existing elements from the page:

```javascript
document.getElementById()
```

Used for:

- Input field
- Button
- List container

---

## Event Handling

Listening for user interactions:

```javascript
element.addEventListener()
```

Used for:

- Button clicks
- Quote item clicks

---

## Reading User Input

Getting values entered by users:

```javascript
input.value
```

---

## Creating Elements Dynamically

Creating new HTML elements using JavaScript:

```javascript
document.createElement()
```

Used for generating quote items.

---

## Updating Element Content

Inserting text into DOM elements:

```javascript
element.innerText
```

---

## Inserting Elements Into The DOM

Adding new elements to existing containers:

```javascript
element.appendChild()
```

---

## Removing Elements

Deleting elements from the DOM:

```javascript
element.remove()
```

---

# JavaScript Concepts Practiced

## Fetch API

Making HTTP requests:

```javascript
fetch()
```

---

## Promises

Handling asynchronous operations:

```javascript
.then()
```

---

## JSON Parsing

Converting JSON responses into JavaScript objects:

```javascript
response.json()
```

---

## Async Functions (IIFE)

Immediately executing asynchronous code:

```javascript
(async () => {
   ...
})();
```

---

## Iterating Through Arrays

Looping over API response data:

```javascript
for...of
```

---

# DOM Methods Used In This Project

```javascript
=>methods
document.getElementById()

document.createElement()

element.appendChild()

element.remove()

element.addEventListener()

=> property
element.innerText  

input.value=
```

# API Used

FreeAPI Quotes Endpoint:

https://api.freeapi.app/api/v1/public/quotes

# Future Improvements

- Search quotes
- Filter quotes
- Pagination
- Random quote generator
- Copy quote button
- Dark/Light mode
- Quote categories
