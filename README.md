# Lucie Kolaříková — statická verze k review

Tento repozitář obsahuje sestavený zákaznický web: HTML, CSS, JavaScript, použité obrazové soubory a lokální písma. Neobsahuje vývojový generátor, stažený archiv, interní výzkumné dokumenty, klientské Q&A ani pracovní snímky. Seznam zveřejněných stránek a souborů je v [`manifest.json`](manifest.json).

## Hostování

Web se nasazuje přímo z kořene repozitáře, bez instalačního nebo sestavovacího příkazu. Vstupní soubor je [`index.html`](index.html). Soubor `.nojekyll` vypíná zpracování Jekyllem a odkazy jsou relativní, tedy použitelné také v projektovém podadresáři.

Pro GitHub Pages zvolte **Settings → Pages → Deploy from a branch → main → /(root)**. Tato instrukce popisuje možné zapnutí hostingu, nikoli potvrzení, že je služba už aktivní. Zdroj: [dokumentace GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

**Repozitář je veřejný.** Také případný GitHub Pages náhled bude veřejně dostupný. `noindex`, `nofollow` a `robots.txt` nejsou řízení přístupu ani ochrana heslem. Pro skutečně neveřejné review je potřeba hosting s autentizací. Zdroj: [viditelnost GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site#about-publishing-sources).

## Rozsah review

Jde o návrh prezentace, nikoli o nový funkční e-shop nebo členskou aplikaci. Vyhledávání, filtry, porovnání, průvodce a objednávkový náhled fungují v prohlížeči. Objednávkové okno umí výběr varianty, cenový souhrn, dopravu, období předplatného a kontrolu vyplněných údajů. **Nic neodesílá ani neplatí**; po zavření se vyplněný náhled smaže. Pro zkoušení používejte smyšlené údaje. Koncepty označené **DRAFT** nejsou existující objednatelné služby. Podklad: zveřejněné HTML a [`assets/app.js`](assets/app.js).

Přehled článků odkazuje na původní veřejné texty; nejde o dokončenou migraci blogu. Ceny jsou podložené veřejnými objednávkovými daty nebo výslovně omezeným popisem nabídky. Nejde o potvrzení prodeje, termínů a kapacit; u Buddhy je dostupný formulář pro zpětný kontakt a u meditace Pouštění nefunguje původní nákupní cesta. Čtyři omezené programové osnovy a produkční ceník zůstávají k autorizaci. Nové texty potřebují schválení Lucií; technické předání nenahrazuje potvrzení práv k fotografiím a referencím ani přípravu ostrého provozu. Původní obsah: [luciekolarikova.cz](https://luciekolarikova.cz/) a [mozekjakobuddha.cz](https://mozekjakobuddha.cz/).

Mapa výdejních míst, ověřování slevových kódů, platební brána, fakturace a skutečné předání přístupů nejsou připojené. Výběr doručení pracuje se zachycenými sazbami pro uvedené země, nikoli s živou dostupností dopravce. Ověření DIČ ani zvláštní daňový režim firmy se nesimuluje.

## Média a technické hranice

Fotografie a písma jsou součástí statických souborů. Licence písem jsou přiložené v [`assets/fonts`](assets/fonts); tím se neuděluje nová licence k fotografiím, značce ani referencím. Videa používají vzdálené přehrávače uvedené v `manifest.json` a mohou komunikovat se svými poskytovateli. Zdroje jsou uvedené u příslušných videí; technické vložení je viditelné v HTML.

HTML obsahuje vlastní CSP a referrer policy, takže jeho omezení síťových požadavků a formulářů nezávisí jen na lokálním preview serveru. Ochrana `frame-ancestors` vyžaduje HTTP hlavičku a nelze ji nahradit HTML meta značkou; tuto hlavičku musí případně dodat zvolený hosting. Zdroj: [specifikace CSP pro meta element](https://www.w3.org/TR/CSP3/#meta-element).

## Aktualizace

Jde o generovaný snapshot. Další úpravy se mají provádět ve vývojovém projektu a znovu exportovat, nikoli nahrazením repozitáře celým vývojovým adresářem. Zvlášť nekopírovat `docs`, `archive` ani lokální `review.html`; export je záměrně odděluje od zákaznického webu.
