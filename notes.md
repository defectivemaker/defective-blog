Adding Katex

use this: https://mertbakir.gitlab.io/hugo/math-typesetting-in-hugo/

Add things to layouts/partials/extend-head.html instead of just head.html


The theme allows for inserting additional code directly into the <head> and <footer> sections of the template. These can be useful for providing scripts or other logic that isn’t part of the theme.

Simply create either layouts/partials/extend-head.html or layouts/partials/extend-footer.html and these will automatically be included in your website build. Both partials are injected as the last items in <head> and <footer> so they can be used to override theme defaults.

(I commented out the single quote $ to Latex because I think it's silly)

To add mermaid.js compatibility

Follow this https://gohugo.io/content-management/diagrams/#mermaid-diagrams

But add the snippet for content template into extend-head.html