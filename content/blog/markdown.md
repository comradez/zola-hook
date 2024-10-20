+++
title = "Markdown example"
date = 2021-07-30
+++

This post is a markdown example.

Here is [a link](http://example.com).

Some *italic text* and **bold text** and ~~strikethrough text~~ and `inline code`. [^1]

```rust
// Here is a code block

fn main() {
    println!("Hello world!");
}
```

Unordered list: [^2]
- An unordered,
- bulleted list
- of items

Ordered list:
1. An ordered,
2. numbered list
3. of items

> A quote.
>
> It contains multiple paragraphs.

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

![An example image](https://plchldr.co/i/480x360?bg=EB6361)

![A large image](https://plchldr.co/i/1280x720?bg=3D8EB9)

<div class="doublespace"></div>

{{ collapsible( summary="Collapsible", content="I can eat glass, it does not hurt me." ) }}

LaTeX formula: \\(e^{i\pi} + 1 = 0\\)

$$
\int_{-\infty}^{\infty} \frac{1}{\sqrt{2\pi}\sigma} \exp\left(-\frac{(x - \mu)^2}{2\sigma^2}\right) \text{d} x = 1
$$

[^1]: A footnote. Footnotes can be used for things that could have explanation or extra context, but
for which the explanation is not relevant or otherwise desirable to have inline.

[^2]: Another footnote.
