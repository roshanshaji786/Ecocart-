# Prompt: browse the live ecocart.co.in from your PC

This cloud session can't open ecocart.co.in. To check the real site:

1. Open the Claude app on your PC, or Claude Code on your PC.
2. Start a new session and paste everything in the box below.
3. When it finishes, copy its report and paste it into this session. The report may also arrive here by itself.

```text
You are helping the owner of ecocart.co.in (a WordPress + WooCommerce store in Thiruvananthapuram, Kerala) relaunch the store on Shopify.

READ-ONLY TASK. Do not log in, submit forms, add to cart, place orders, install software, or create/modify/delete files. Only fetch public pages and public JSON endpoints (WebFetch, or `curl.exe -sL <url>` printed to the terminal).

Collect:
1. Homepage https://ecocart.co.in/ : menu, announcement bar, hero text, every section in order, products shown with prices, footer text, copyright year, phone/email/WhatsApp numbers, social links.
2. Every product from https://ecocart.co.in/wp-json/wc/store/v1/products?per_page=100&page=1 (then page=2, 3... until empty): name, permalink, regular price, sale price, categories, stock status, number of images, review count and rating. If the API is disabled, crawl https://ecocart.co.in/shop/ and its pages instead.
3. Categories: https://ecocart.co.in/wp-json/wc/store/v1/products/categories (name, slug, count).
4. Pages and posts: https://ecocart.co.in/wp-json/wp/v2/pages?per_page=100&_fields=id,link,title,modified and https://ecocart.co.in/wp-json/wp/v2/posts?per_page=100&_fields=id,link,title,date
5. About, Contact, Shipping, Refund/Returns, Privacy, Terms, Cart, Checkout (just load it), My Account: what each says about shipping fees, free-shipping threshold, COD, return window, delivery time, payment methods. List missing policy pages.
6. SEO/tech: robots.txt; sitemap (/wp-sitemap.xml or /sitemap_index.xml); homepage title, meta description and H1; Open Graph tags; Google Analytics/Tag Manager/Meta Pixel present (search the HTML for gtag, googletagmanager, fbq); theme name (/wp-content/themes/<name>/); main plugins (/wp-content/plugins/<name>/); HTTPS and www redirects.
7. Speed: https://www.googleapis.com/pagespeedonline/v5/runPagespeed?url=https://ecocart.co.in/&strategy=mobile (and strategy=desktop): performance score, LCP, CLS, TBT.
8. Problems: 404s/broken links, template or demo text ($ prices, "Lorem", "Home 2", demo categories), contradictions between pages, products with no price or image, odd product titles.

Output ONE markdown report with compact tables (split into parts 1/N, 2/N if very long). If the send_message tool (claude-code-remote) is available, also send the report to session session_01ATks1cP8RhdsfaZpV129xU.
```
