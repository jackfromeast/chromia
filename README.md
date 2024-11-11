# ![Logo](chrome/app/theme/chromium/product_logo_64.png) Chromia - with Lookup Integrity 

`Chromia` is an enhanced version of `Chromium` that incorporates lookup integrity enforcement to protect against code-reuse attacks, such as DOM Clobbering and Prototype Pollution, on the web. This security feature provides fine-grained runtime checks to ensure that lookups are conducted safely.

### Branches

+ Branch `main`
  + An untouched base version of `Chromium`
  + Commit: `1f195406385bd2d75ddd167bb6ae5d6cb5fbc420`
  + Fri Dec 1 22:35:56 2023 +0000

+ Branch `chrome-clobber`
  + The branch has been used to measure both legitimate usage and vulnerable lookups
  + Used with the `gr8@chrome-clobber` that supports logging all the lookups on document and root prototype (sources of these attacks).

+ Branch `sig-inference`
  + Short for `signature-inference` branch
  + This branch automatically generates signatures for values loaded at each lookup site.
  + Currenlty, it records the DOM nodes’ append locations to track where each node is appended within the DOM tree.

