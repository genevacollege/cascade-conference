<a href="https://geneva.edu/" target="_blank">
  <img src="https://avatars.githubusercontent.com/u/59443670?v=4" alt="Geneva College logo" style="position: absolute; top: 0; right: 0; width: 25%;" />
</a>

# Geneva College's Cascade CMS User Conference Presentation

_Presented by [Michael Duncan](https://www.linkedin.com/in/michaelduncan7) and [Caleb Hyatt](https://calebhyatt.com/)._

## Table of Contents

- [GitHub File Structure](#github-file-structure)
- [Fetching the JSON Data](#fetching-the-json-data)
- [The Main Functions](#the-main-functions)
- [Deep Linking](#deep-linking)

## GitHub File Structure

```
genevacollege/cascade-conference
├── blocks
|   ├── programs-search-filter-html
|   └── programs-search-filter-scripts
├── code-snippets
|   ├── Fetch URL.png
|   ├── Main Functions.png
|   └── URL to Search Function.png
├── formats
|   ├── Academic Programs JSON.vtl
|   └── Program Facts.vtl
└── script.js
```

## Fetching the JSON Data

Use the **_[system-asset]_** tag within the JavaScript file and the **_?raw_** parameter at the end of the route, which ensures that the data returned is in the correct format for Cascade to interpret.

Here's what our code will look like to fetch the JSON data:

![Fetch URL code snippet](https://raw.githubusercontent.com/genevacollege/cascade-conference/main/code-snippets/Fetch%20URL.png)

## The Main Functions

We have the main portion of our code divided into three functions: urlToSearch, init, and search. We run all three after the fetch request is completed in succession.

**_urlToSearch()_** handles deep-linking by updating the values in the input fields from the URL.

**_init()_** is a simple initializing function that preps the page for the search results. It puts the initial results and the “No Results Found” header on the page for later use.

**_search()_** is where the search and filtering take place. The fetch retrieves the JSON output. Results are filtered based on user input.

![Main Functions code snippet](https://raw.githubusercontent.com/genevacollege/cascade-conference/main/code-snippets/Main%20Functions.png)

## Deep Linking

Example URL: [https://www.geneva.edu/academics/programs/?interest=business](https://www.geneva.edu/academics/programs/?interest=business)

**_URLSearchParams_** is used to parse the current URL. Everything after the question mark and ampersand are parsed into an object.

**_getParam()_** checks if a parameter exists, and if not then nothing is executed.

![URL to Search Function code snippet](https://raw.githubusercontent.com/genevacollege/cascade-conference/main/code-snippets/URL%20to%20Search%20Function.png)
