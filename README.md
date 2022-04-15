# Shortly - URL Shortening API Project

## Table Of Contents

- [Overview](#overview)
  - [The Challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [The Process](#the-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The Challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- Shorten any valid URL
- See a list of their shortened links, even after refreshing the browser
- Copy the shortened link to their clipboard in a single click
- Receive an error message when the `form` is submitted if:
  - The `input` field is empty

## Screenshots

### Desktop Version

<img src="./screenshots/desktop.png" width="200" />

### Mobile Version

<img src="./screenshots/mobile.png" width="200" />

### Links

- Live Site URL: [Netlify]()

## The Process

### Built with

- React JS
- Tailwind CSS
- Flexbox
- Mobile-first workflow
- Axios
- Local Storage

### What I learned

On this project I learned about collaborating with another developer. We established a `git` workflow and broke the project down into `feature-branches` based on the `React Components`.

I also learned about making `async await` API calls using `Axios`. I learned about handling `Promises` with `.then`.

```js
export const getShortenedURL = async (submittedURL) => {
  try {
    const {data} = await axios.get(URLBase + `${submittedURL}`, options);
    return data;
  } catch (error) {
    console.log(error);
  }
};
```

```js
const shortenedURL = (submittedValue) => {
    getShortenedURL(submittedValue).then((data) => {
      }
```

### Useful resources

- [Axios Getting Started](https://axios-http.com/docs/intro) - The workflow that we used on this project.
- [Git Merging vs. Rebasing](https://www.atlassian.com/git/tutorials/merging-vs-rebasing) - This article was a huge help while collaborating.

## Author

- Author - [Tyrell Curry](https://tyrellcurry.io)

## Acknowledgments

Much appreciation to [Rod Garland](https://github.com/zencoder24) for collaborating with me on this project.
