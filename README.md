# Valdo Nõlvaku portfoolio

Staatiline ühe lehe portfoolio (HTML + CSS, välised sõltuvused puuduvad). Sobib otse GitHub Pagesi või Cloudflare Pagesi jaoks.

## Struktuur

```
index.html          – kogu leht (Avaleht, CV, Enesetäiendamine, Koolitused, Õppematerjalid, Valdkonna arendus, Hobid)
assets/profiil.jpg  – profiilifoto (lisa ise; kui fail puudub, näidatakse initsiaale "VN")
```

## Avaldamine GitHub Pagesis

1. Loo GitHubis uus avalik repo, näiteks `valdonolvak.github.io` (siis on aadress `https://valdonolvak.github.io`) või mõni muu nimi (siis on aadress `https://<kasutaja>.github.io/<repo>`).
2. Laadi failid üles:
   ```bash
   git init
   git add .
   git commit -m "Portfoolio esimene versioon"
   git branch -M main
   git remote add origin https://github.com/<kasutaja>/<repo>.git
   git push -u origin main
   ```
3. Ava repos **Settings → Pages → Build and deployment**, vali **Source: Deploy from a branch**, haru `main` ja kaust `/ (root)`, ning salvesta.
4. Minuti-paari pärast on leht üleval.

## Oma domeen (valikuline)

1. Lisa repo juurkausta fail `CNAME`, mille sisu on ainult domeen, näiteks `valdonolvak.ee`.
2. Lisa domeeni DNS-i:
   - juurdomeeni jaoks A-kirjed `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - või `www` jaoks CNAME `<kasutaja>.github.io`
3. Lülita **Settings → Pages** all sisse **Enforce HTTPS**.

## Profiilifoto

Salvesta oma foto nimega `assets/profiil.jpg` (soovitatavalt ruudukujuline, umbes 400×400 px).
