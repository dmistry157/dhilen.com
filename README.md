# dhilen.com

Static files served by GitHub Pages (deploy from `main`, root). There is no build step.

- `/` (`index.html`) redirects to LinkedIn.
- `/freefood/` (`freefood/index.html`) redirects to https://calfreefood.com, the Berkeley Free Food map.
- `CNAME` tells Pages to answer for `dhilen.com`. GoDaddy DNS points dhilen.com at GitHub Pages
  (A records 185.199.108-111.153, `www` CNAME to dmistry157.github.io).

GitHub Pages can't send server-side redirects, so each page redirects with a meta refresh,
a canonical link and `location.replace()`.
