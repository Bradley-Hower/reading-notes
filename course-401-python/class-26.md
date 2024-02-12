# *Course 401 Python, Entry 26: Django

**What are the key components of the Django framework, and how do they contribute to building a web application?**

- Defined models, which allows for SQL creation if needed.
- Clean URLS creation. Unlike PHP for example, it allows for clean URL mapping with different renderings.
- A template language which is easy to use due to its similarities to HTML. Additionally, extendible in functionality.
- Forms which cleanly integrate with Python.

---

- Full-featured authentication: permissions and cookie-based sessions.
- Automatic admin interface. Allows for content creators to plug in. Built off of metadata in models.

**Explain the role of Django’s MTV (Model-View-Template) architecture and how it handles a typical web request-response cycle.**

![domainmodel](assets/domainmodel.png)

- The HTTP request comes in and is handled by the URL mapper.
- The mapper then directs the request to the appropriate View.
- The View (a request handler function) handles the request.
- The data required to fulfill the request is met via the appopriate model.
- Content is returned via the appropriate template (HTML, JSON, etc.).

**What is the purpose of Tailwind CSS, and how does it differ from Bootstrap CSS?**

It is a framework for quickly writing web code without using custom CSS. Tailwind uses utility classes. This allows for a lot of CSS to be pumped into a HTML tag via a class attribute. The difference is that unlike Bootstrap where components are used, in Tailwind, pre-build CSS classes are used instead which then can be further tweaked. This vastly reduced CSS. It also allows for more flexibility. Outcome, a more unique site appearance.

Summary: Tailwind is Bootstrap, but more flexible.

## Things I want to know more about

What are the limits of Views. Can this be used to plug into other APIs or networks?

Source: picture via [https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Introduction](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Introduction)