# TextMate Rules for Markdown Color-Coding

NOTE: This is a section of our full *User Settings* document. That document is hundreds of thousands of tokens long and cannot be edited by AI. We must *make changes here* and then be sure to *copy this section to overwrite the same section* in the full User Settings Document.

```JSONC
    // Editor token color customizations
    // Overrides editor syntax colors and font style from the currently selected color theme.
    "editor.tokenColorCustomizations": {
        "textMateRules": [
            {
                // HEADINGS: All heading levels (# Heading 1, ## Heading 2, etc.)
                // This includes both the heading text and the # symbols
                "scope": [
                    "markup.heading",
                    "entity.name.section",
                    "heading.1.markdown",
                    "heading.2.markdown",
                    "heading.3.markdown",
                    "heading.4.markdown",
                    "heading.5.markdown",
                    "heading.6.markdown",
                    "punctuation.definition.heading.markdown",
                    "markup.heading.markdown",
                    "markup.heading.1.markdown",
                    "markup.heading.2.markdown",
                    "markup.heading.3.markdown",
                    "markup.heading.4.markdown",
                    "markup.heading.5.markdown",
                    "markup.heading.6.markdown",
                    "entity.name.section.markdown",
                    "meta.block-level.markdown heading.markdown"
                ],
                "settings": {
                    "foreground": "#FF9D00",
                    "fontStyle": "bold"
                }
            },
            {
                // BOLD TEXT: **bold text** or __bold text__
                // This includes both the text and the ** or __ markers
                "scope": [
                    "markup.bold",
                    "punctuation.definition.bold.markdown"
                ],
                "settings": {
                    "foreground": "#FFD866",
                    "fontStyle": "bold"
                }
            },
            {
                // ITALIC TEXT: *italic text* or _italic text_
                // This includes both the text and the * or _ markers
                "scope": [
                    "markup.italic",
                    "punctuation.definition.italic.markdown"
                ],
                "settings": {
                    "foreground": "#8aeefb",
                    "fontStyle": "italic"
                }
            },
            {
                // BLOCKQUOTES: > This is a blockquote
                // This includes both the text and the > symbol
                "scope": [
                    "markup.quote",
                    "markup.quote.markdown",
                    "punctuation.definition.quote.begin.markdown",
                    "meta.block-level.markdown markup.quote",
                    "meta.list.markdown markup.quote",
                    "meta.block-level.markdown markup.quote.markdown",
                    "meta.list.markdown markup.quote.markdown"
                ],
                "settings": {
                    "foreground": "#E6DB74",
                    "fontStyle": "italic"
                }
            },
            {
                // FENCED CODE BLOCKS: ```code blocks``` (not including inline code)
                // This includes the backticks and language identifier
                "scope": [
                    "markup.fenced_code",
                    "punctuation.definition.markdown",
                    "fenced_code.block.language",
                    "markup.fenced_code.block.markdown"
                ],
                "settings": {
                    "foreground": "#6767fc"
                }
            },
            {
                // CODE BLOCK CONTENT: The actual content inside ```code blocks```
                "scope": [
                    "markup.raw.block",
                    "markup.raw.block.markdown",
                    "markup.raw.block.fenced.markdown"
                ],
                "settings": {
                    "foreground": "#8989e3"
                }
            },
            {
                // INLINE CODE: `code` between backticks
                "scope": [
                    "markup.inline.raw",
                    "markup.inline.raw.string.markdown",
                    "markup.inline.raw.markdown",
                    "markup.quote markup.inline.raw",
                    "markup.quote.markdown markup.inline.raw.markdown",
                    "meta.list.markdown markup.inline.raw",
                    "meta.block-level.markdown markup.inline.raw"
                ],
                "settings": {
                    "foreground": "#78de8c",
                    "fontStyle": ""
                }
            },
            {
                // LINKS: [link text](url) - the link text part and brackets
                "scope": [
                    "markup.link",
                    "string.other.link.title.markdown",
                    "string.other.link.description.markdown",
                    "punctuation.definition.string.begin.markdown",
                    "punctuation.definition.string.end.markdown",
                    "punctuation.definition.metadata.markdown"
                ],
                "settings": {
                    "foreground": "#AB9DF2"
                }
            },
            {
                // LINK URLS: The actual URL in [link text](url) or image paths
                "scope": [
                    "meta.link.url.markdown",
                    "string.other.link.destination.markdown",
                    "punctuation.definition.link.destination.markdown",
                    "markup.underline.link.image.markdown"
                ],
                "settings": {
                    "foreground": "#8BE9FD"
                }
            },
            {
                // REFERENCE LINKS: [link text][reference] and [reference]: url
                "scope": [
                    "markup.underline.link.markdown",
                    "constant.other.reference.link.markdown",
                    "meta.link.reference.def.markdown"
                ],
                "settings": {
                    "foreground": "#50FA7B"
                }
            },
            {
                // LINK TITLES AND IMAGE ALT TEXT: [link text](url "title") or ![alt text](image.jpg)
                "scope": [
                    "string.other.link.description.title.markdown",
                    "meta.link.inline.markdown",
                    "meta.image.inline.markdown"
                ],
                "settings": {
                    "foreground": "#AB9DF2"
                }
            },
            {
                // ALL CAPS TEXT: Text that is in all capital letters (like "INQUIRY:")
                // Note: This requires a custom TextMate grammar extension to work fully
                "scope": [
                    "keyword.other.uppercase",
                    "constant.language.uppercase",
                    "entity.name.uppercase"
                ],
                "settings": {
                    "foreground": "#00ffaa",
                    "fontStyle": "bold"
                }
            },
            {
                // QUOTED TEXT: Text within normal double quotes like "quoted text"
                "scope": [
                    "string.quoted.double.markdown",
                    "punctuation.definition.string.begin.markdown",
                    "punctuation.definition.string.end.markdown"
                ],
                "settings": {
                    "foreground": "#c792ea",
                    "fontStyle": ""
                }
            },
            {
                // PARENTHESES TEXT: Text within parentheses like (this text)
                // Excludes link URLs and other special markdown elements
                "scope": [
                    "meta.parens.markdown",
                    "punctuation.definition.parens.begin.markdown",
                    "punctuation.definition.parens.end.markdown"
                ],
                "settings": {
                    "foreground": "#ff9e64",
                    "fontStyle": ""
                }
            },
            {
                // SQUARE BRACKETS TEXT: Text within square brackets like [this text]
                // Excludes link text, reference links, and other special markdown elements
                "scope": [
                    "meta.brackets.markdown",
                    "punctuation.definition.brackets.begin.markdown",
                    "punctuation.definition.brackets.end.markdown"
                ],
                "settings": {
                    "foreground": "#7dcfff",
                    "fontStyle": ""
                }
            },
            {
                // URLS AND PATHS: URLs and file paths outside of special markdown elements
                // This targets URLs and paths that are not part of links or code blocks
                "scope": [
                    "constant.other.reference.url.markdown",
                    "meta.path.url.markdown",
                    "string.unquoted.url.markdown"
                ],
                "settings": {
                    "foreground": "#73daca",
                    "fontStyle": ""
                }
            },
                // FALLBACK FOR ALL LIST CONTENT: General rule for any list content not caught by specific rules
                "scope": [
                    "markup.list"
                ],
                "settings": {
                    "foreground": "#cccccc"
                },
            {
                // BULLET POINT LIST CONTENT: The content of bullet point lists (not the markers)
                "scope": [
                    "markup.list.unnumbered.markdown",
                    "markup.list.unordered.markdown",
                    "meta.paragraph.list.markdown"
                ],
                "settings": {
                    "foreground": "#5feda4"
                }
            },
            {
                // NUMBERED LIST CONTENT: The content of numbered lists (not the markers)
                "scope": [
                    "markup.list.numbered.markdown",
                    "markup.list.ordered.markdown",
                    "meta.paragraph.list.ordered.markdown"
                ],
                "settings": {
                    "foreground": "#f8a5c2"
                }
            },
            {
                // BULLET POINT LIST MARKERS: Just the bullet points (-, *, +) at the start of lists
                // This targets unordered lists specifically, including indented ones
                "scope": [
                    "punctuation.definition.list.begin.markdown",
                    "meta.list.markdown punctuation.definition.list.begin.markdown",
                    "meta.paragraph.list punctuation.definition.list.begin.markdown"
                ],
                "settings": {
                    "foreground": "#dfc532",
                    "fontStyle": "bold"
                }
            },
            {
                // INDENTED BULLET POINTS: Specifically targeting indented bullet points to ensure they keep their color
                "scope": [
                    "markup.list.unnumbered punctuation.definition.list.begin.markdown",
                    "markup.list.unordered punctuation.definition.list.begin.markdown"
                ],
                "settings": {
                    "foreground": "#dfc532",
                    "fontStyle": "bold"
                }
            },
            {
                // BULLET POINTS WITHIN NUMBERED LISTS: Ensuring bullet points in numbered lists keep their color
                "scope": [
                    "markup.list.numbered.markdown markup.list.unnumbered.markdown punctuation.definition.list.begin.markdown",
                    "meta.list.markdown markup.list.numbered markup.list.unnumbered punctuation.definition.list.begin.markdown"
                ],
                "settings": {
                    "foreground": "#dfc532",
                    "fontStyle": "bold"
                }
            },
            {
                // NUMBERED LIST MARKERS: Just the numbers (1., 2., etc.) at the start of ordered lists
                // This targets ordered lists specifically, including indented ones
                "scope": [
                    "punctuation.definition.list.number.markdown",
                    "beginning.punctuation.definition.list.markdown",
                    "markup.list.numbered.markdown punctuation.definition.list.begin.markdown",
                    "meta.list.markdown markup.list.numbered punctuation.definition.list.begin.markdown",
                    "meta.paragraph.list.ordered punctuation.definition.list.begin.markdown"
                ],
                "settings": {
                    "foreground": "#ff6b6b",
                    "fontStyle": "bold"
                }
            },
            {
                // CHECKBOXES: - [ ] or - [x] in task lists
                "scope": [
                    "markup.checkbox.markdown",
                    "punctuation.definition.markdown.checkbox"
                ],
                "settings": {
                    "foreground": "#50faad",
                    "fontStyle": "bold"
                }
            },
            {
                // STRIKETHROUGH: ~~strikethrough text~~
                "scope": [
                    "markup.strikethrough",
                    "punctuation.definition.strikethrough"
                ],
                "settings": {
                    "foreground": "#6272A4",
                    "fontStyle": "strikethrough"
                }
            },
            {
                // TABLES: | table | content |
                "scope": [
                    "markup.table",
                    "punctuation.definition.table.markdown"
                ],
                "settings": {
                    "foreground": "#e2ff79"
                }
            },
            {
                // HORIZONTAL RULES: --- horizontal dividers
                "scope": [
                    "meta.separator.markdown",
                    "meta.separator",
                    "punctuation.definition.thematic-break.markdown"
                ],
                "settings": {
                    "foreground": "#93f9c6"
                }
            },
            {
                // FOOTNOTES: [^1] and the footnote definition
                "scope": [
                    "markup.footnote",
                    "punctuation.definition.footnote.markdown",
                    "constant.other.reference.footnote.markdown"
                ],
                "settings": {
                    "foreground": "#8BE9FD",
                    "fontStyle": "italic"
                }
            },
            {
                // COMMENTS AND IGNORED CONTENT: <!-- comments -->
                "scope": [
                    "markup.ignored.markdown",
                    "markup.disabled.markdown",
                    "meta.diff.header.to-file",
                    "meta.diff.header.from-file"
                ],
                "settings": {
                    "foreground": "#6272A4",
                    "fontStyle": "italic"
                }
            },
            {
                // DIFF ADDITIONS: Added content in diffs
                "scope": [
                    "markup.inserted.markdown",
                    "markup.inserted",
                    "markup.addition"
                ],
                "settings": {
                    "foreground": "#50FA7B"
                }
            },
            {
                // DIFF DELETIONS: Removed content in diffs
                "scope": [
                    "markup.deleted.markdown",
                    "markup.deleted",
                    "markup.deletion"
                ],
                "settings": {
                    "foreground": "#FF5555"
                }
            },
            {
                // DIFF CHANGES: Modified content in diffs
                "scope": [
                    "markup.changed.markdown",
                    "markup.changed",
                    "markup.modification"
                ],
                "settings": {
                    "foreground": "#FFB86C"
                }
            },
            {
                // HTML TAGS: <div> or other HTML in markdown
                "scope": [
                    "meta.embedded.block.html",
                    "punctuation.definition.tag"
                ],
                "settings": {
                    "foreground": "#FF79C6"
                }
            },
            {
                // CODE BLOCK LANGUAGE: The language identifier in ```javascript
                "scope": [
                    "fenced_code.block.language",
                    "entity.name.tag.yaml",
                    "variable.language.fenced.markdown"
                ],
                "settings": {
                    "foreground": "#F1FA8C"
                }
            },
            {
                // YAML FRONT MATTER: The metadata section at the top of markdown files
                "scope": [
                    "meta.embedded.block.frontmatter",
                    "punctuation.definition.frontmatter",
                    "entity.other.attribute-name.frontmatter"
                ],
                "settings": {
                    "foreground": "#BD93F9",
                    "fontStyle": ""
                }
            },
            {
                // ESCAPE CHARACTERS: Backslash escapes like \* or \[
                "scope": [
                    "constant.character.escape.markdown"
                ],
                "settings": {
                    "foreground": "#FF79C6",
                    "fontStyle": ""
                }
            },
            {
                // MATH EXPRESSIONS: $inline math$ or $$block math$$
                "scope": [
                    "text.html.markdown.math",
                    "markup.math.inline",
                    "markup.math.block"
                ],
                "settings": {
                    "foreground": "#8BE9FD",
                    "fontStyle": ""
                }
            },
            {
                // HIGHLIGHTED TEXT: ==highlighted text==
                "scope": [
                    "markup.highlight",
                    "markup.highlight.markdown",
                    "punctuation.definition.highlight"
                ],
                "settings": {
                    "foreground": "#F1FA8C",
                    "background": "#6272A4",
                    "fontStyle": ""
                }
            },
            {
                // EMOJIS AND SPECIAL CHARACTERS: :smile: or HTML entities
                "scope": [
                    "markup.emoji",
                    "constant.character.entity.html",
                    "entity.name.emoji"
                ],
                "settings": {
                    "foreground": "#FFB86C",
                    "fontStyle": ""
                }
            },
            {
                // KEYBOARD KEYS: <kbd>Ctrl</kbd>
                "scope": [
                    "markup.kbd",
                    "meta.tag.inline.kbd",
                    "entity.name.tag.kbd"
                ],
                "settings": {
                    "foreground": "#F8F8F2",
                    "background": "#44475A",
                    "fontStyle": ""
                }
            },
            {
                // DEFINITION LISTS: Term: Definition
                "scope": [
                    "markup.list.definition",
                    "markup.heading.definition",
                    "variable.other.definition"
                ],
                "settings": {
                    "foreground": "#50FA7B",
                    "fontStyle": ""
                }
            },
            {
                // ABBREVIATIONS: *[abbr]: explanation
                "scope": [
                    "meta.abbreviation.markdown",
                    "constant.other.abbreviation.markdown"
                ],
                "settings": {
                    "foreground": "#BD93F9",
                    "fontStyle": ""
                }
            },
            {
                // CRITIC MARKUP: {++addition++}, {--deletion--}, {~~old~>new~~}
                "scope": [
                    "markup.critic.addition",
                    "markup.critic.deletion",
                    "markup.critic.substitution",
                    "markup.critic.comment",
                    "markup.critic.highlight"
                ],
                "settings": {
                    "foreground": "#50FA7B",
                    "fontStyle": ""
                }
            },
            {
                // ADMONITIONS: !!! note, !!! warning, etc.
                "scope": [
                    "markup.admonition",
                    "markup.admonition.header",
                    "entity.name.admonition"
                ],
                "settings": {
                    "foreground": "#FFB86C",
                    "fontStyle": "bold"
                }
            },
            {
                // SUPERSCRIPT AND SUBSCRIPT: X^2 or H~2~O
                "scope": [
                    "markup.superscript",
                    "markup.subscript",
                    "punctuation.definition.superscript",
                    "punctuation.definition.subscript"
                ],
                "settings": {
                    "foreground": "#8BE9FD",
                    "fontStyle": ""
                }
            },
            {
                // MARKDOWN ATTRIBUTES: {#id .class key=value}
                "scope": [
                    "meta.attribute.markdown",
                    "entity.other.attribute-name.markdown",
                    "string.other.attribute-value.markdown",
                    "punctuation.definition.attribute.markdown"
                ],
                "settings": {
                    "foreground": "#FF79C6",
                    "fontStyle": ""
                }
            },
            {
                // MERMAID DIAGRAMS: ```mermaid content ```
                "scope": [
                    "markup.fenced_code.block.mermaid",
                    "source.mermaid"
                ],
                "settings": {
                    "foreground": "#8BE9FD",
                    "fontStyle": ""
                }
            },
            {
                // GRAPHVIZ DIAGRAMS: ```dot content ```
                "scope": [
                    "markup.fenced_code.block.dot",
                    "source.dot"
                ],
                "settings": {
                    "foreground": "#FF79C6",
                    "fontStyle": ""
                }
            },
            {
                // TASK LIST ITEM TEXT: The text part of - [ ] task
                "scope": [
                    "meta.paragraph.list"
                ],
                "settings": {
                    "foreground": "#F8F8F2",
                    "fontStyle": ""
                }
            },
            {
                // CITATION KEYS: [@citation]
                "scope": [
                    "markup.citation",
                    "constant.other.citation"
                ],
                "settings": {
                    "foreground": "#BD93F9",
                    "fontStyle": ""
                }
            },
            {
                // MARKDOWN COMMENTS: <!-- comment -->
                "scope": [
                    "comment.block.html",
                    "punctuation.definition.comment.html"
                ],
                "settings": {
                    "foreground": "#6272A4",
                    "fontStyle": "italic"
                }
            }
        ]
    }
```
