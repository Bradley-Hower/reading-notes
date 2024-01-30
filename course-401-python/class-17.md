# *Course 401 Python, Entry 17: Web Scraping

**What are the key differences between scraping static and dynamic websites?**

The key difference between a dynamic webpage and a static one, which reflects in the scraping is the dynamic content. Anything with dynamicly loaded javascript will not appear in a static scraping.

**Explain at least three techniques or best practices that can be employed to avoid getting blocked while scraping websites.**

- Scrape slower and less often in less predictable ways with different IP addresses.
- Rotate user agents and headers
- Avoid scraping behind a login.

All these come down to the over-use of a website. Humans don't load ever page on a consistent bases and traverse it in predictable ways. These factors all need to be programmed into a scraper to avoid being blocked. Moreover, if you can be identified via fingerprinting or a login, it makes it easier to detect odd behavior.

**What is Playwright, and how does it assist in web scraping tasks? Provide an example of a use case where Playwright would be particularly beneficial.**

Playwright allows for dynamic scraping via by working with a web browser (Chromium, Firefox, or Webkit). Moreover, it has the capacity to save dynamic content. If there is a webpage that updates with JavaScript content on page load via injeciton, this would be especially useful.

**Describe the purpose of using Xpath in web scraping, and provide an example of an Xpath expression to select a specific HTML element from a webpage.**

Xpath allows for identifying content via the tags in an HTML or XML document.

An example for selecting title text:

```
//h1/text() OR //h1/b/text() 
```

## Things I want to know more about

How is AI changing the landscape of human verification requests. 