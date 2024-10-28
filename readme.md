# Media Library

This project is a simple media library implemented in JavaScript. It allows you to manage books and movies, including checking out items and rating them.

## Classes

### Media

The `Media` class is the base class for all media items. It includes properties and methods common to all media types.

- **Properties:**
  - `_title`: The title of the media item.
  - `_isCheckedOut`: A boolean indicating whether the item is checked out.
  - `_ratings`: An array of ratings for the item.

- **Methods:**
  - `get title()`: Returns the title of the media item.
  - `get isCheckedOut()`: Returns whether the item is checked out.
  - `get ratings()`: Returns the ratings of the item.
  - `set isCheckedOut(value)`: Sets the checked-out status of the item.
  - `toggleCheckOutStatus()`: Toggles the checked-out status of the item.
  - `addRating(value)`: Adds a rating to the item.
  - `getAverageRating()`: Returns the average rating of the item.

### Book

The `Book` class extends the `Media` class and includes additional properties specific to books.

- **Properties:**
  - `_author`: The author of the book.
  - `_pages`: The number of pages in the book.

- **Methods:**
  - `get author()`: Returns the author of the book.
  - `get pages()`: Returns the number of pages in the book.

### Movie

The `Movie` class extends the `Media` class and includes additional properties specific to movies.

- **Properties:**
  - `_director`: The director of the movie.
  - `_runTime`: The runtime of the movie in minutes.

- **Methods:**
  - `get director()`: Returns the director of the movie.
  - `get runTime()`: Returns the runtime of the movie.

## Usage

Here is an example of how to use the classes:

```javascript
const historyOfEverything = new Book(
  "Bill Bryson",
  "A Short History of Nearly Everything",
  544
);
historyOfEverything.toggleCheckOutStatus();
console.log(historyOfEverything.isCheckedOut); // true
historyOfEverything.addRating(4);
historyOfEverything.addRating(5);
historyOfEverything.addRating(5);
console.log(historyOfEverything.getAverageRating()); // 4.67

const speed = new Movie("Jan de Bont", "Speed", 116);
speed.toggleCheckOutStatus();
console.log(speed.isCheckedOut); // true
speed.addRating(1);
speed.addRating(1);
speed.addRating(5);
console.log(speed.getAverageRating()); // 2.33