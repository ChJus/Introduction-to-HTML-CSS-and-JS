# Age calculator app

![](../assets/age-calculator-reference.png)

In this task, you will implement the above design
(from [FrontendMentor](https://www.frontendmentor.io/challenges/age-calculator-app-dF9DFFpj-Q)).

The app should be able to accurately calculate the age of a person from a given input birth date.
You may want to consider error handling — for negative years or invalid months and dates.

Consider:

- Interactivity of components (hover effects, transitions, animations).
- Light/dark mode
- Responsive design — consideration for mobile viewports.
- Typography and color palette
- **Challenge**: add a simple animation when the age updates (e.g., implement a number counter/ticker animation).

Styling:

- Font: Poppins (400-italic, 700, 800-italic);
- Body copy: font size (32px)
- Purple: hsl(259, 100%, 65%)
- Light red: hsl(0, 100%, 67%)
- White: hsl(0, 0%, 100%)
- Darker white: hsl(0, 0%, 94%)
- Light grey: hsl(0, 0%, 86%)
- Smokey grey: hsl(0, 1%, 44%)
- Lighter black: hsl(0, 0%, 8%)

Useful references:

- [Date](https://www.w3schools.com/js/js_dates.asp), [Event listeners](https://www.w3schools.com/js/js_htmldom_eventlistener.asp),
  [Timing](https://www.w3schools.com/js/js_timing.asp)

### Dealing with Dates

JS has a built-in Date class. You can perform operations like `+` and `-` between Date objects to get the time
difference in milliseconds.

To initialize a Date object, follow the format:

```js
// Creates a date object representing current time
let d = new Date();

// Sets date to YYYY-MM-DD.
// Note that month values are from 0-11, so remember to subtract 1.
// Date objects also have a year quirk where if values are between 0-99, 
// they are assumed to refer to years in the 20th century.
d.setFullYear(year, month, date);
```

You may want to use the following function
(from [StackOverflow](https://stackoverflow.com/questions/6950248/javascript-method-to-ensure-that-a-date-is-valid)) to
check whether a Date is valid based on the year, month, and day values.

```js
function isValidDate(year, month, day) {
  let d = new Date(parseInt(year, 10),
    parseInt(month, 10) - 1,
    parseInt(day, 10));
  return d.getFullYear() === year &&
    (d.getMonth() + 1) === month &&
    d.getDate() === day;
}
```