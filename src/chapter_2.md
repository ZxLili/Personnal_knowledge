# Chapter 2

Template de ce que [mdbook gère gratuitement](https://rust-lang.github.io/mdBook/format/markdown.html), sans ajout de plugin

---

> [!NOTE]
> General information or additional context.

> [!TIP] 
> A helpful suggestion or best practice.

> [!IMPORTANT]
> Key information that shouldn't be missed.

> [!WARNING]
> Critical information that highlights a potential risk.

> [!CAUTION]
> Information about potential issues that require caution.

---

- milk
- eggs
- butter

1. carrots
2. celery
3. radishes

liste numeroté automatiquement
: carrots  
 sqddqsqsdqdqdqs
: celery  
 sqdsqkhdksqksqdgiuzflkq
: radishes  
 lsqdjlsqjdllksdlksqj

---

Use [mdBook](https://github.com/rust-lang/mdBook).

Read about [mdBook](mdbook.md).

And now [an mdBook link] that is not inline, unlike the above.

A bare url: <https://www.rust-lang.org>.

[an mdBook link]: https://github.com/rust-lang/mdBook

---

{{#include ./introPages.md}}

{{#playground}}  
$$\frac{1}{3}$$
\\( \int x dx = \frac{x^2}{2} + C \\)
\\[ \mu = \frac{1}{N} \sum_{i=0} x_i \\]

> [!NOTE]
> ca marche parce que dans le toml il ya
>
> ```
> [output.html]
> mathjax-support = true
> ```

---

on peut prendre des images de n'importe ou mais la mieux c'est de les ranger dans assets

![The Rust Logo](images/rust-logo-blk.svg)
![Chat](https://livvet.vet/wp-content/uploads/2025/07/bengal-chat-livvet-fiche-race-chat-teleconseil-veterinaire-home-livvet-veterinaire-min.png)

<p><img src="images/rust-logo-blk.svg" alt="The Rust Logo" /></p>
