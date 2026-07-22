# Nordform VVS & Energi – demowebbplats

En helt statisk, fiktiv demowebbplats. Den innehåller inga uppgifter, bilder eller texter från Grebo El.

## Publicera via GitHub och Cloudflare Pages

1. Skapa ett nytt tomt repository på GitHub.
2. Lägg innehållet i denna mapp i repositoryts rot och pusha till `main`.
3. I Cloudflare: **Workers & Pages → Create → Pages → Connect to Git**.
4. Välj repositoryt. Framework preset: **None**. Build command: lämna tomt. Output directory: `/`.
5. Publicera. Varje push till `main` skapar därefter en ny deployment.

## Viktigt före verklig användning

- Sajten är tydligt märkt som demo och använder fiktiva kontaktuppgifter och projekt.
- Kontaktformuläret är visuellt och skickar inte data. Koppla en riktig formulärtjänst eller Cloudflare Function först när det behövs.
- `_headers` och `robots.txt` blockerar indexering. Ta bort `X-Robots-Tag` och ändra `robots.txt` först när sajten har ett verkligt företag, riktiga uppgifter och ska hittas i Google.
- Byt exempel för certifikat mot verifierade, aktuella behörigheter.

## Lokal förhandsvisning

Kör exempelvis `python3 -m http.server 8080` i mappen och öppna `http://localhost:8080`.
