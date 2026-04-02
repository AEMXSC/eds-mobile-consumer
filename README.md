# EDS → Mobile Consumer

**AEM XSC Demo Tool** — Show any EDS page consumed as a native mobile app. One fetch call. No Content Fragments. No GraphQL.

## What This Does

Point it at any EDS page via the [html2json service](https://demo.bbird.live/demo-docs/usecases/how-to-html2json), and it renders the content inside an iPhone 16 mockup. Demonstrates headless consumption of EDS content without additional authoring effort.

## Demo Flow

1. Open DA — show the page being authored  
2. Open the EDS site — show the standard website  
3. Open this tool — show the same content on a mobile app  
4. Edit in DA, publish  
5. Hit **Fetch** — both the website and mobile app update  

## URL Pattern

```
https://mhast-html-to-json.adobeaem.workers.dev/{org}/{repo}/{path}?compact=true&head=false
```

## Presets Included

| Label | URL |
|-------|-----|
| courtneydemo | `scdemos/courtneydemo/` |
| bbird demo | `scdemos/demo/` |
| xscteamsite | `aemxsc/xscteamsite/` |

Edit the URL field to point at **any** EDS page.

## Setup

1. Clone this repo
2. Enable GitHub Pages (Settings → Pages → Source: main branch, root)
3. Access at `https://aemxsc.github.io/eds-mobile-consumer/`

No build step. No dependencies. Single HTML file.

## Adding Presets

Edit `index.html` — find the `PRESETS` array near the top and add entries:

```javascript
{ id:"customer", label:"Acme Corp", url: SVC + "/acme/website/?compact=true&head=false" },
```
