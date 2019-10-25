# Tol107G-Hopverkefni-1

# Project Details / Lýsing á verkefni


## How To Run
1) Install package needed node modules. Run 'npm init' to download neccesary packages. This refers to the package-lock.json file in the root.

2) Generate css.
* Run 'npm run scss' then edit and save the relevant scss files to generate the .css files needed into the '/css' folder.
* Similarly running 'npm run dev' will start a web sever and also monitor changes to the scss files and generate css files into the '/css' folder.

3) Start the website.
* Navigate to the root of the project tree with you console terminal.
* Run 'npm run start' in the command line. This starts the website using a local host.

## Project Overview
### File Tree Description
* / , contains the index page, package.json, readme, and other configuration files.
* /css, contains css files converted from scss files. These are the actual stylesheet that the website relies on.
* /scss, contains scss files that are converted to be converted to css files.
* /img, contains all the images in the project.
* /pages, contains the html files for the 4 sub-pages of the project.

### Technologies Used
Htlm, .SCSS (translated into .CSS before running with script), node package manager for command line scripts, scripts written in package.json in the root.

### Scripts
* "scss": "node-sass --watch scss -o css",

* "lint-a": "stylelint scss/card-animation.scss --syntax scss",
* "lint-c": "stylelint scss/config.scss --syntax scss",
* "lint-g": "stylelint scss/site-grid.scss --syntax scss",
* "lint-s": "stylelint scss/styles.scss --syntax scss",    

* "browser-sync": "browser-sync start --server --files index.html styles.css",    
* "dev": "npm-run-all --parallel scss browser-sync",
* "start": "npm-run-all --parallel browser-sync"

### SCSS Organization Breakdown
All SCSS files are placed in the '/scss' folder. 
* card-animation.scss, handles the animation of the staff members on the staff page
* config.scss, contains variables that are accessed throughout the scss.
* style.scss, is the main stylesheet for the whole website.
* site-grid.scss, is the stylesheet containing the scss for the grid used for the pages layout.

## Project Members / Upplýsingar um alla sem unnu verkefnið
### Group / Hópur 33		
* Member / Meðlimur 1	Styrmir Þórarinsson	sth315@hi.is
* Member / Meðlimur 2	Ólöf Svafarsdóttir	ols32@hi.is
* Member / Meðlimur 3	Hrafnhildur Hafsteinsdóttir	hlh11@hi.is




# Hópverkefni 1

Verkefnið felst í því að smíða vef eftir forskrift.

Gefnar eru [fyrirmyndir](utlit/) í `500px`, `800px` og `1500px` með grind ásamt `1500px` án grindar og yfirliti yfir virkni vefs í `utlit/video.mp4`.

## Síður

Gögn fyrir síður eru í viðeigandi textaskrám (t.d. forsida.txt) undir `efni/`. Myndir fyrir síður eru gefnar undir `img/`. Afrita þarf öll gögn á milli síðna, ekki er krafa um að setja upp sameiginlegan haus/fót á síðum með einhverju kerfi eða forritun.

Efni síðu skal ekki vera breiðara en `1200px`. Litir í haus og fæti skulu fylla út í allt lárétt pláss.

Síður hafa allar sama haus og sama fót. Vöruflokkar í fæti skulu allir vísa á `pages/products.html`. Námskeið í fæti skulu vís á `pages/course.html`

Grunn leturstærð er 16px og fylgja allar aðrar leturgerðir eftirfarandi skala: `12 14 16 18 21 24 36 48 60`.

Litapalletta fyrir vef er `#000000`, `#fffcf2`, `#ff5000` og `#00b7ff`.

Letur fyrir meginmál er Open Sans eða helvetica, arial eða sans-serif letur.
Letur fyrir fyrirsagnir er Oswald, Verdana eða serif letur.

Flest allt er sett upp í 12 dálka grind með `20px` gutter.

Öll bil eru hálft, heilt, tvöfalt eða þrefalt margfeldi af gutter. Hægt er að nota reglustiku tól (t.d. http://www.arulerforwindows.com/ eða http://www.pascal.com/software/freeruler/) til að finna nákvæmar stærðir en mestu skiptir að lausn svipi til en sé ekki nákvæmlega eins og fyrirmynd.

Allar hreyfingar gerast á `200ms` með `ease-in-out` hröðunarfalli.

Ekki þarf að útfæra neina virkni fyrir takka eða form.

## Hópavinna

Verkefnið skal unnið í hóp með þremur einstaklingum. Skráning í hópa fer fram í [Google sheets](https://docs.google.com/spreadsheets/d/1GwC9OvnpGHIkuX7ArRG7UQ-JV74b_pomegGXOWF1od0/edit?usp=sharing)

Notast skal við Git og GitHub. Engar zip skrár með kóða ættu að ganga á milli í hópavinnu, heldur á að „committa“ allan kóða og vinna gegnum Git.

## Lýsing á verkefni

`README.md` skrá skal vera í rót verkefnis og innihalda:

* Upplýsingar um hvernig keyra skuli verkefnið
* Lýsingu á uppsetningu verkefnis, hvernig því er skipt í möppur, hvernig CSS er skipulagt og fleira sem á við
* Upplýsingar um alla sem unnu verkefnið
* Leyfilegt er að halda eftir þessari verkefnalýsingu en hún skal þá koma _á eftir_ ykkar lýsingu

## Tæki og tól

Setja skal upp Sass og stylelint fyrir verkefnið. Gefin er `styles.scss` skrá með grunn upplýsingum.

Gefin er `.stylelintrc` skrá sem segir til um hvernig lint fyrir `scss` skrár skuli háttað.

Í `.gitignore` er `styles.css` hunsað sem þýðir að það verður _ekki_ checkað inn. Það er gert vegna þess að það er búið til af sass út frá `styles.scss`

## Gefnar skrár

Eftirfarandi er sett upp í verkefni:

* `.stylelintrc` með upplýsingum um hvernig stylelint eigi að haga sér. Setja þarf upp `stylelint-config-primer` pakkann
* `.gitignore` sem hunsar algengar skrár, [sjá nánar](https://help.github.com/ignore-files/)
* `.gitattributes` sem kemur í veg fyrir ósamræmi sem geta komið upp þegar unnið er á milli stýrikerfa
* `.editorconfig` sem samræmir notkun á tabs og spaces, bilum [og fleira](https://editorconfig.org/)
* `index.html` með vísun í `styles.css` og `grid.css` ásamt tómum skrám fyrir `products.html`, `staff.html`, `course.html` og `cart.html` undir `pages/`, halda skal þessu skipulagi
* `grid.css` til að sjá grid sem fyrirmynd er unnin eftir

Setja þarf upp `package.json` og sækja viðeigandi pakka til að tæki og tól sem verkefnið á að nýta virki.

## Mat

* 10% - `README` eftir forskrift, tæki og tól uppsett
* 20% – Snyrtilegt, gilt (skv. stylelint) CSS/Sass, gilt og aðgengilegt HTML
* 30% – Almennt útlit
* 8% – Forsíða
* 8% – Vörur síða
* 8% – Námskeið síða
* 8% – Starfsfólk síða
* 8% – Karfa síða

## Sett fyrir

Verkefni sett fyrir í fyrirlestri mánudaginn 7. október 2019.

## Skil

Einn aðili úr hóp skal skila fyrir hönd allra og skila skal undir „Verkefni og hlutaprófa“ á Uglu í seinasta lagi fyrir lok dags föstudaginn 25. október 2019.

Skil skulu innihalda:

* Nöfn allra í hóp ásamt notendanafni
* Slóð á GitHub repo fyrir verkefni, og öllum dæmatímakennurum skal hafa verið boðið í repo ([sjá leiðbeiningar](https://help.github.com/articles/inviting-collaborators-to-a-personal-repository/)). Notendanöfn þeirra eru `anz1e`, `gunnnnii`, `magdadianaa`, `OlafurjonHI` og `Wolfcoder13` .
* Slóð á verkefnið keyrandi á vefnum.

## Einkunn

Sett verða fyrir tíu minni verkefni þar sem átta bestu gilda 3,5% hvert, samtals 28% af lokaeinkunn.

Sett verða fyrir tvö stærri verkefni þar sem hvort um sig gildir 11%, samtals 22% af lokaeinkunn.

## Myndir

Myndir frá:

* [Innkaupakörfu fengin á iconfinder](https://www.iconfinder.com/icons/216460/cart_icon)
* [Aðrar myndir fengnar frá Unsplash](https://unsplash.com/photos/N4QTBfNQ8Nk)

---

> Útgáfa 0.1