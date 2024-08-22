# Exercise: Greatest Books of All Time - Array Mastery in JavaScript

## Learning Goals

By completing this exercise, you will be able to:

- Manipulate arrays using various JavaScript methods.
- Work with objects within arrays.
- Implement sorting and filtering logic.
- Calculate averages and perform data transformations.
- Handle edge cases and create robust functions

## Introduction

Welcome to the literary world of JavaScript! In this exercise, you'll explore a dataset of the greatest books of all time. As an aspiring developer, your task is to create functions that analyze and manipulate this treasure trove of literary information.

Picture yourself building the backend for an innovative book recommendation platform. Your code will navigate through centuries of literary genius, unearthing insights and presenting data in fresh, engaging ways. From spotting prolific authors to computing genre ratings, your functions will breathe life into this static data!

Ready to embark on this coding adventure through the annals of literary history? Let's turn the page and dive into the world of JavaScript arrays!

## Getting Started

Follow the instructions below to get started:

1. Go to the Exercise (add link)
2. Fork the Repository
3. Clone the Repository to your computer
4. Open the Repository in VS Code
5. Start the Live Server in VS Code
6. Follow instructions

## The Book Object

Throughout this exercise, you’ll be working with an array of book objects.

Each book is represented as follows:

```json
{
  "title": "Harry Potter and the Philosopher's Stone",
  "year": 1997,
  "author": "J.K. Rowling",
  "genre": "Fantasy",
  "rating": 9.1,
  "pages": "332 pages"
}
```

We will provide you with a sample dataset, which you can use to complete your exercises. But you can also create your own array of your most favourite books if you want to.

## Instructions

Complete the following exercises to practice working with arrays and objects in JavaScript:

### Iteration 1: All Authors

Create a function named `getAllAuthors(...)` that receives an array of books as an argument and returns a new array containing all the authors. Use the map method to achieve this.

### Bonus - Iteration 1.1: Unique Array of Authors

Enhance your `getAllAuthors(...)` function to return an array of unique authors, removing any duplicates.

### Iteration 2: J.K. Rowling, The Best?

Implement a `howManyBooks(...)` function that receives the books array as a parameter and returns the number of 'Fantasy' books written by J.K. Rowling. Use the filter method for this task.

### Iteration 3: All ratings average

Create an `averageRating(...)` function that calculates the average rating of all books. The function should receive the books array as a parameter and return the average rounded to 2 decimal places.

### Iteration 4: Science Fiction Books

Implement a `sciFiBooksRating(...)` function that calculates the average rating of all 'Science Fiction' books. Compare this to the overall average to determine if Science Fiction books are rated higher on average.

### Iteration 5: Order by Year

Create an `orderByYear(...)` function that sorts the books array by publication year in ascending order. If two books have the same year, sort them alphabetically by title. Return a new sorted array.

### Iteration 6: Alphabetical Order

Implement an `orderAlphabetically(...)` function that returns an array of the first 20 book titles in alphabetical order. If the input array has fewer than 20 books, return all titles alphabetically ordered.

### Bonus - Iteration 7: Time Format

Create a `convertPagesToNumber(...)` function that transforms the pages property of each book from a string (e.g., "350 pages") to a number (350). Return the modified array of books.

### Bonus - Iteration 8: Best Yearly Rating Average

Implement a `bestYearAvg(...)` function that determines which year has the best average rating for books published in that year. Return an object containing the year and its average rating.

## **Submission**

When you've completed the exercise:

1. Commit your changes:

```bash
git add .
git commit -m "Completed Greatest Books exercise"
git push origin main
```

2.	Create a Pull Request
3.	Submit the URL of your Pull Request

## **Let's Discuss!**
If you're getting stuck, we got you covered.

<details>
<summary>How can I efficiently remove duplicates from an array?</summary>

Consider using a Set object or the filter method with indexOf. For example:

```js
const uniqueAuthors = [...new Set(authors)];
// or
const uniqueAuthors = authors.filter((author, index, self) => 
  self.indexOf(author) === index
);
```
</details>

<details>
<summary>What's the best way to calculate an average in JavaScript?</summary>

You can use the reduce method to sum up values and then divide by the array length:

```js
const average = array.reduce((sum, value) => sum + value, 0) / array.length;
```
</details>

<details>
<summary>How do I sort an array of objects based on multiple criteria?</summary>

Use the sort method with a comparison function that checks multiple properties:

```js
books.sort((a, b) => {
  if (a.year !== b.year) return a.year - b.year;
  return a.title.localeCompare(b.title);
});
```
</details>
    

Remember, every great coder started with a single line of code. Take it step by step, and don't hesitate to consult documentation or ask for help. Happy coding, literary explorer!