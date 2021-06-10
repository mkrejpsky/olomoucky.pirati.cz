# Návod pro Pirátský web - Pardubicky kraj

Zdrojové kódy webu: **https://github.com/pirati-web/olomoucky.pirati.cz**

Web je staticky kompilovaný v době změny, čili v repozitáři je opravdu všechno.

Správci webu: Ondřej Profant, Stanislav Štipl, Jakub Michálek, Vojta Pikal, Jan Loužek

Správci obsahu: Zdenek Kubala

## 1. Markdown a yaml

Je třeba znát značkovací **markdown**, který je velmi podobný grafickému plaintextu.
Markdown si můžete vyzkoušet i v [online editoru](http://dillinger.io/) s náhledem.
Není třeba se ho bát. Do markdownu též můžete vložit přímo html. Například pokud chcete vložit složitější tabulku nebo google kalendář.

```md
# Nadpis 1. úrovně

## Nadpis 2. úrovně

### Odstavce

Samostatný odstavec. Lorem ipsum. **Tučně**, *kurzíva*, [link](https://www.pirati.cz)

Odstavec se zalomením se provede  
pomocí dvou mezer na konci řádku.

1\. odstavec začínající řadovou číslovkou.

### Seznamy

1. číslovaný seznam 1
2. číslovaný seznam 2

- nečíslovaný seznam 1
- nečíslovaný seznam 2

### Obrázky

![Popisek obrázku](assets/img/brand/logo.svg)

### Citace

> Pro kratší citace zcela dostačují české úvozovky, popřípadě v kurzivě. Nicméně pro delší citace je dobré větší zdůraznění.

```

**Yaml** se používá pro zanesení metadat k článkům (stránkám). Yaml hlavičku umístíme před markdown:

```Yaml
key1: hodnota
key2:
  - pole
  - hodnot
key3:
  key4: val1
  key5: val2
```

Nejlépe je to srozumitelné na [příkladu](https://raw.githubusercontent.com/pirati-web/pirati.cz/gh-pages/_people/ondrej-profant.md).

## Github

Jedná se o systém pro sdílení verzí textových dokumentů (jako např. náš web).
Umí toho mnohem více. Pro vás je důležité vytvořit si registraci.

Návrhy na změnu (pull request) se projeví až po schválení. Ale i pokud máte přímo právo zápisu, tak se změny neobjeví zcela okamžitě.

## Články


### Tagy

Tagy neoddělujeme čárkami, ale pouze mezerou.
Zvolit správný tag není jednoduché - musí být vystižný, ale zároveň dost obecný, aby dával smysl i u dalších článků.

## Lidé a další stránky


## Sociální sítě

Stránku je dobré otestovat ve [FB debbuger](https://developers.facebook.com/tools/debug/), aby se správně zobrazovala při sdílení. [Správné rozměry obrázku](https://developers.facebook.com/docs/sharing/best-practices#images) (1200 x 630)

## Složitější změny

Zatím jsme prošli základy. Ale většinou není více potřeba. Pro opravdové změny je třeba ještě znát:

- HTML, CSS, JS
- git
- jekyll (liquid template)

### HTML

Některé stránky jsou složitější a je potřeba znalost HTML. Seznámení s HTML není obsahem tohoto návodu.

### Struktura webu

1. Kolekce začínají podtržítkem a jsou definovány v config.yaml. Včetně některých defaultních hodnot (např. obsah pravého sloupce).
2. Stránky jsou obvykle samostatné složky obsahující soubor `index.html` nebo `index.md`. Mohou zde být i další stránky např. `pripoj-se/kalendar.html`.
3. Hlavička, patička, pravý sloupec jsou ve složce `_includes`

Članky: 1300x744
People (lidé), foto 165x220
