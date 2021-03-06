# The Modern JavaScript Tutorial in <%=langInfo.name%>

This repository hosts the translation of <https://javascript.info> in <%=langInfo.name%>.

**That's how you can contribute:**

- See the [<%=langInfo.name%> Translate Progress](https://github.com/javascript-tutorial/<%=langInfo.code%>.javascript.info/issues/<%=progressIssue.number%>) issue.
- Choose an unchecked article you'd like to translate.
- Add a comment to that issue to inform the maintainer that you're translating it.
- Fork the repository, translate and send a PR when done.

**Let others know what you're translating, in message boards or chats in your language. Invite them to join!**

🎉 Thank you!

<% if (langInfo.published) { -%>
Your name and the contribution size will appear in the contributors list at <https://<%=langInfo.code%>.javascript.info/about#contributors> when PR is accepted.
<% } else { -%>
Your name and the contribution size will appear in the "About project" page when the translation gets published.
<% } -%>

If you'd like to become a maintainer, have full access to the repository and review translations of others, write us at <https://github.com/javascript-tutorial/translate/issues/new>.

P.S. The full list of languages can be found at <https://github.com/javascript-tutorial/translate>.

## Structure

Every chapter, an article or a task resides in its own folder.

The folder is named `N-url`, where `N` – is the number for sorting (articles are ordered), and `url` is the URL-slug on the site.

The folder has one of files:

- `index.md` for a section,
- `article.md` for an article,
- `task.md` for a task formulation (+`solution.md` with the solution text if any).

A file starts with the `# Title Header`, and then the text in Markdown-like format, editable in a simple text editor. 

Additional resources and examples for the article or the task, are also in the same folder.

## Translation Tips

- The translation doesn't have to be word-by-word precise. It should be technically correct and explain well.
- If you see that the English version can be improved – great, please send a PR to it.

**Please keep line breaks and paragraphs "as is": don't add newlines and don't remove existing ones.** Makes it easy to merge future changes from the English version into the translation. 

### Glossary

Agree on translations of terms like `resolved promise`, `slash`, `regexp`, etc. Look a good glossary, maybe there's one for your language already?
Or create it, for all translators to use the same terms. 

### Text in Code Blocks

- Translate comments.
- Translate user-messages and example strings.
- Don't translate variables, classes, identifiers.
- Ensure that the code works after the translation :)

Example:

```js
// Example
const text = "Hello, world";
document.querySelector('.hello').innerHTML = text;
```

✅ DO (translate comment):

```js
// Ejemplo
const text = 'Hola mundo';
document.querySelector('.hello').innerHTML = text;
```

❌ DON'T (translate class):

```js
// Ejemplo
const text = 'Hola mundo';
// ".hello" is a class
// DO NOT TRANSLATE
document.querySelector('.hola').innerHTML = text;
```

### External Links

If an external link is to Wikipedia, e.g. `https://en.wikipedia.org/wiki/JavaScript`, and a version of that article exists in your language that is of decent quality, link to that version instead.

Example:

```md
[JavaScript](https://en.wikipedia.org/wiki/JavaScript) is a programming language.
```

✅ OK (en -> es):

```md
[JavaScript](https://es.wikipedia.org/wiki/JavaScript) es un lenguaje de programación.
```

For links to MDN, that are only partially translated, also use the language-specific version.

If a linked article has no translated version, leave the link "as is".

### Metadata

Some files, usually tasks, have YAML metadata at the top, delimited by `---`:

```md
importance: 5

---
...
```

Please don't translate "importance" (and other top metadata).

## Running locally

You can run the tutorial locally, to immediately see the changes on-site.

The server is at <https://github.com/javascript-tutorial/server>. 
