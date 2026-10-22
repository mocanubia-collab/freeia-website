# FREEIA — Your inner light

Prima versiune de prezentare a site-ului Freeia, pregătită pentru Cloudflare Pages.

## Ce include
- Pagină principală responsive cu imaginea de prezentare
- Catalog demonstrativ cu filtre și listă de produse preferate
- Secțiuni SMART Candle, poveste și contact
- Fără checkout sau procesare plăți; produsele sunt exemple și nu sunt disponibile pentru comandă

## Publicare prin GitHub și Cloudflare Pages
1. Încarcă **conținutul** acestui folder în rădăcina repository-ului `freeia-website` (nu folderul ca subfolder).
2. Cloudflare Dashboard → Workers & Pages → Create application → Pages → Connect to Git.
3. Selectează repository-ul `freeia-website`.
4. Framework preset: **None**; Build command: **gol**; Build output directory: **/** (sau setarea implicită pentru site static, dacă Cloudflare o acceptă).
5. Deploy. Numele `freeia.pages.dev` depinde de disponibilitate.

## Modificarea produselor
Deschide `products.json` în GitHub și apasă pictograma creion (Edit). Poți adăuga obiecte noi respectând structura celor existente. Câmpuri:
- `id`: unic, fără spații
- `name`: nume
- `category`: `Lumânări`, `SMART Candle` sau `Wax melts`
- `description`: descriere
- `price`: număr în lei sau `null` dacă nu există preț
- `image`: calea imaginii, ex. `assets/lumanare-noua.jpg`
- `available`: rezervat pentru activarea comenzilor viitoare
- `smart`: `true` / `false`

## Adăugarea fotografiilor
GitHub → folderul `assets` → Add file → Upload files → încarcă fotografia → Commit changes. Actualizează apoi câmpul `image` din `products.json`. Cloudflare va republica automat după commit dacă proiectul este conectat la GitHub.

## De reținut
Aceasta este o primă versiune statică, **nu** un magazin funcțional și **nu** include încă un panou vizual de administrare. Pentru un panou ușor de folosit, fără editarea JSON, va trebui configurat separat un CMS cu autentificare. Nu încărca date personale, chei API sau parole în repository-ul public.

Fotografia hero este un concept vizual generat; înlocuiește-o cu fotografia finală a produsului înainte de lansarea comercială.
