# *Course 102, Entry 1: Markdown*

Initially created in 2004 by **John Gruber**, Markdown is a Lightweight Markup Language (LML), a simple, easy-to-use text-encoding language which adds formatting and structure to plaintext documents via inserted symbols and statements (jointly, syntax). There are many different Markdown editors available to users, web-based and application, with all major mobile and desktop platforms being supported (Mac, iOS, Windows, Android, and Linux). Some of these options offer a preview pane feature, allowing users to immediately see the results of their edits. However, as an LML, Markdown is meant to be easy enough to use that a basic text editor should suffice, as the syntax of Markdown is designed to be very readable.

## Advantages

+ **Dynamic**. Innumerable use cases. Documentation, presentations, emails, and websites are just a few uses for Markdown.
+ **Compatible**. Being that the output is quite simple, it is easy to integrate with other code.
+ **Embraced**. Supported across multiple operating platforms.
+ **Durable**. Being that it is so simple, it is highly unlikely to break at your next update.
+ **Pervasive**. Implemented in many places, including big-name websites like Reddit, Github, SourceForge, and Stack Exchange.

## Notable Examples:

### Headings

To create a heading in Markdown, simply use `#`, followed by a space before the text to be formatted. The number of times `#` is inserted is inversely related to the size of text. One `#` creates the largest heading, six creates the smallest.

Example:

```
# Super-Duper-Title
###### Super-Duper-Title
```
Output:

![Heading Example](https://github.com/Bradley-Hower/reading-notes/assets/139923955/929eccb6-fd37-4ec7-af8e-2c8f1734431a)

#### Bold

Due to potential compatibility issues, the best practice for applying bold to text is to use `**` immediately before and after the target text.

Example:

```Text **text**.```

Output:

![Bold Example](https://github.com/Bradley-Hower/reading-notes/assets/139923955/f2788fd5-b487-43fa-97c7-1040f7d68718)


### Italic

Likewise, to apply italic to text, it is best practice to to use `*` immediately before and after the target text, rather than underscores.

Example:

```
Text *text*.
```
Output:

![Italic Example](https://github.com/Bradley-Hower/reading-notes/assets/139923955/66e5219d-72d3-407e-914d-b09e30ec1a97)


### Links

To create a link in Markdown, use `[` immediately before the text and `]` immediately after, with the URL following, with `(` and `)` immediately before and after the URL text, respectively. 

Example:

```
For the best open-source code versioning platform, go to [GitHub](https://github.com).
```

Output:

![Links Example](https://github.com/Bradley-Hower/reading-notes/assets/139923955/e98811b3-cb1c-4277-867b-7e82f8b1ed6a)



### Unordered Lists

To create an unordered list, you can use the delimiters `-`, `+`, or `*`, with the elected symbol being followed by a space, preceding the target text. Indents can also be used. Best practice is to not mix and match these delimiters though, else issues could arise. 

Example:

```
+ Apples
+ Oranges
  + Tangerines
+ Grapes
```

Output:

![Unordered Lists Example](https://github.com/Bradley-Hower/reading-notes/assets/139923955/2abe2abd-8970-49c7-90b1-b55ebc14bcd3)
