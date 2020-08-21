# BookList
 JS simple project for beginners

## Inspiration
This app is based on courses by Brad Traversy from Udemy

## What I Did To Make The Project Even Better


## What I learned
* method: 
* function: 

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







