# *Course 201, Entry 13: Introduction to Persistence with Local Storage*

By principle, HTTP is **stateless**. Meaning, unlike applications, once closed, that's it, it can be cleared.

Local storage has great advantages. It allows the user to avoid needing to log in. All the data needed is right there. Secondly, it can also be used to stay under data pull caps on API services.

## Methods

Cookies are the traditional form of storing locally. However, cookies are data capped at 4 KB. Moreover, many people block them, knowing the security risk they can hold.

However, in HTML5, local storage can store any type of data. This is accomplished by converting all to a string via JSON and pulling it back, outside of the string in.

### HTML5

To store data, the `localstorage` object can be used. Using `setItem()`, `getItem()`, and `removeItem()` methods, data strings can be stored, retrieved, and deleted. Data is stored as key-value pairs, separated by a comma. To store only temporarily, the `sessionStorage` object can be used instead. To clear all of local storage, the empty `clear()` method can be used.

To stringify data, use `JSON.stringify()` as a wrapper for the value for the set, and `JSON.parse()` as a total wrapper for the get.

Example:

```
localStorage.setItem( 'cat', JSON.stringify(catdata) );
JSON.parse( localStorage.getItem( 'cat' ) ) ;
```

## Summary

No critical data for functionality should be stored locally, as this can not be relied on. Users can at any time clear their local data or decide to only browse in private mode. 

## Things I want to know more about

How many of these techniques still work? How well have isolate tabs features stopped tracking? What percentage of users browse in private mode? Can this be exploited by big companies to reduce their running costs by storing locally on users' computers?