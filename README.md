# BookList
 JS simple project for beginners

## Inspiration
This app is based on courses by Brad Traversy from Udemy

## What I Did To Make The Project Even Better


## What I learned
* method: insertBefore, getItem, JSON.parse, JSON.stringify, setItem, spline

- JSON.parse : method parses a JSON string, constructing the JavaScript value or object described by the string.
- JSON.stringify : method converts a JavaScript object or value to a JSON string
- setItem(keyName, keyValue) : when passed a key Name and value, will <strong>add</strong> that key to the given storage object
- getItem() : when passed a key name, will <strong>return</strong> that key's value in the given Storage object
- spline : method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place


## How to build
<strong> [ Step 1. Add Book To List ] </strong>

1. set Book constructor
- define function Book

2. add event listeners
- id:book-form, after submit load function
- define variable title, author, isbn : value
- Instantiate book : define variable book

- Instantiate UI : define variable UI

- Add book to list(ui) using function addBookToList

- clear fields in list(ui)

- Blocking default click handling

3. UI Constructor
- define function UI
- Add book to List -prototype /addBookToList (prototypical Inheritance)
 : define function(addBookToList) :argument:book
   - define variable id: book-list
   - define variable : create tr element
   - Insert columns tags
     : td, book.title/bookauthor/book.isbn, add delete button
   - append to list
- Clear fields - prototype / clearFields (prototypical Inheritance)
  : define function(clearFields)
   - clear value of title, author, isbn  

<strong> [ Step 2.Validation & Alert] </strong>

1. show Error - IF statement
* if title is nothing or author is nothing or isbn is nothing
- then, to ui, load function showAlert 'Please fill in all fields', 
call class 'error'

2. Show Alert - prototypical Inheritance
to UI prototype call showAlert
define function, argument are message, className
- define div and create div at DOM
- add classes at div
  : alert className
- add text 
 create text node : message at DOM 
 append text to div
-get parent
 define container, class:container
define form, id:book-form
-insert alert
insert div before form at container

-timeout after 3 sec and its function is
call function remove class:alert in DOM

3. Show success
to ui call showAlert 'Book Added!, call class 'success'

<strong>[ step3. DeleteBook From List]<strong>

1. local Storage Class
* construct Store
- define static function getBooks / displayBooks / addBook /removeBook
* declare static function getBooks
initialize variable books
add IF statement : if localStorage get  nothing item 'books'
then, books' array is empty
otherwise, books is that localStorage get item 'books' parses a JSON string
finally it returns books

* declare static function addBooks
define books, and declare books is getBooks in class Store
to books, push book
add 'books' which is converted to a JSON string into localStorage 

* declare static function displayBooks
define books, and declare books is getBooks in class Store

loop through books, and it will call function;argument is book
- variable ui instantiate UI 
- Add book to UI 

* declare static function removeBook
- call it to remove from localstrage
call function removeBook in class Store
argument is that the event target is added text in previousElementSibling in
parent element
-declare removeBook
argument is isbn
define books, and declare books is getBooks in class Store
-loop through books, and it will call function;argument is book
 declare function
-if isbn in book is same with isbn
 then,  changes the contents of an array by removing : remove one in index


* DOM load Event
after DOMContentLoaded, load function displayBooks in class Store


2. add to LocalStorage
to class Store, call function addBook
 
  




