# simobarber.ca

One-page website for Simo Haircuts. Every "Book" button goes to his Square booking page.

## Editing

Everything you'd normally change is in one block near the bottom of `index.html`, marked
`EDIT EVERYTHING HERE`:

- `address`, `findMe`, `phone`, `instagram`
- `hours` (24h times, `null` = closed)
- `services` (name, minutes, price, image, short description)
- `bookingUrl` (his Square booking link)

Service images live in `img/`.

## Going live (GitHub Pages + GoDaddy)

1. **GitHub:** in the repo, open Settings → Pages. Set Source to "Deploy from a branch",
   pick branch `main` and folder `/ (root)`, then Save.
   The `CNAME` file already tells GitHub the domain is `simobarber.ca`.
2. **GoDaddy:** open My Products → simobarber.ca → DNS, then:
   - Delete any existing **A** record for `@` (often GoDaddy's "Parked" record).
   - Add four **A** records, Name `@`, pointing to:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Edit the **CNAME** record `www` to point to `YOUR-GITHUB-USERNAME.github.io`
3. Wait a little (usually under an hour, sometimes longer). Then go back to GitHub
   Settings → Pages and tick **Enforce HTTPS** once it becomes available.
