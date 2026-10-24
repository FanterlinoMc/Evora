# EVORA — Homepage design prompt

Copy everything below into a design or build tool (Claude, Cursor, v0, a designer's brief). It describes the homepage as currently designed.

---

Design a single-page homepage for **EVORA**, an independent perfume house from Cairo. Evora makes four extrait-strength fragrances, blended in small batches and built to last a full day, at an accessible price. The page should feel like an object from something expensive: quiet, confident, physical. It must not look like a Shopify template or an AI-generated landing page.

## The idea

**The bottle, shown bigger than seems reasonable.** The product is the hero. The arch shape of its printed label (a tall rounded oval) is the one motif, reused as the frame for photographs.

## The product

- **Bottle:** rounded-rectangle glass body, clear faceted crystal cap, short silver neck (black on Velora). A tall oval label in ivory with a copper keyline reads, top to bottom: EV monogram, EVORA, the scent name, a short rule, "EAU DE PARFUM · 30 ML".
- **The four signatures, dark to light, the way the juice runs:**

| Signature | Juice | Notes | One-line difference |
| --- | --- | --- | --- |
| Suvelle | Cognac `#B5672F` | Black pepper, vanilla, amber | Peppered amber. The darkest of the four. |
| Vanilla Reverie | Honey gold `#D9A94F` | Vanilla, sandalwood, amber | Sandalwood underneath. The warmest of the four. |
| Velora (black neck) | Pale straw `#DCC68F` | Jasmine, vanilla, amber | Jasmine at the centre. The only floral of the four. |
| Vanilla Cloud | Near-clear `#EFE4C6` | Vanilla, cashmere, musk | Cashmere all the way down. The lightest of the four. |

- **Discovery set:** four 2 ml vials, one of each signature. The full price comes off the first 30 ml bottle.
- **Sales channel:** WhatsApp is the main way people order in Egypt, so make it prominent.

## Visual system

- **Colour:** one ground, one ink, one accent, all flat.
  - Ground: espresso `#1C1410`, with a one-step lighter tone `#251B15` and a panel tone `#2C2019`.
  - Ink: cream `#F1E8DA`; softer text `#C2B4A2`.
  - Accent: gold `#D3A55A`, used only on the main action and the selected row.
  - One light field for the pricing section: `#EFE6D8`, with a paper tone `#FFFCF6`.
- **Type:** Bodoni Moda for headings and large figures, Manrope for everything else. About five sizes in total. The hero headline is very large (about 13vw, tight tracking, line-height 0.86). Body text is 16–18px.
- **Buttons:** one style only, square-cornered and solid. Gold with espresso text on dark sections, espresso with cream text on light ones.
- **Banned:** gradients, shadows on anything at rest, glass/blur, small spaced-out uppercase labels above headings, 01/02/03 numbering, hairline divider lines, italic or coloured accent words inside headlines, emoji, icon-topped feature cards, and the words *luxurious, premium, journey, essence, unforgettable, exquisite, indulge, elevate, dupe, inspired by, cheaper than*. No exclamation marks.
- Separate areas with space or a change of background tone, never with lines.

## Sections, in order

1. **Hero.** Espresso field. A very large drawn bottle (Vanilla Reverie), tilted about 14°, cropped by the top, left and bottom edges of the screen. On the right, the h1 "Evora / Parfums" on two lines, right-aligned. Under it, one sentence: "Extrait-strength perfume, blended in small batches in Cairo and made to stay from morning to night." No navigation bar: only a small EVORA wordmark top-right, and one gold "Shop the four" button fixed to the bottom-right corner for the whole page. The bottle must not overlap the headline.
2. **Dark to light (the live feature).** Heading "Dark … to light", split in two with the bottle standing in the gap. Below, four full-width rows, one per signature: name and one-line difference on the left, notes and "30 ml · price" on the right. Rows alternate between the two dark tones. Clicking a row turns it gold, and the bottle, which travels down the centre of the list as you scroll (sticky), fills with that signature's juice colour. Vanilla Reverie is selected by default.
3. **Vanilla Reverie close-up.** The product photograph fills the screen as a tight close-up. A solid cream card one grid column wide sits in the second column: name (the section heading), "Eau de parfum, 30 ml", price, a small drawn bottle, one line of notes, and a full-width "Add to bag" button.
4. **Notes band.** A full-width gold band about 300px tall. The seven materials (black pepper, vanilla, jasmine, sandalwood, cashmere, amber, white musk) are set at about 8vw on one line, separated by round dots, cropped by both screen edges and moving slowly left. Below it, one plain sentence explaining that these seven materials make all four signatures.
5. **Our story.** A dark panel inset from the page edges. Heading: "Made to outlast the afternoon". The photograph sits bottom-left, masked to the label's arch shape and cropped by the panel's bottom edge. On the right, two short blocks: "Extrait, at this price" (most perfume at this price is gone by lunch) and "Two sprays is enough" (sprayed at 07:40, still there at 23:00, measured on skin), then an "Order on WhatsApp" button.
6. **Discovery set.** Light cream field. Left: heading "Start with all four", one sentence, and an "Order the discovery set" button. Right: a tall paper receipt with a zigzag torn bottom, its top running off the section. It lists Suvelle, Vanilla Reverie, Velora and Vanilla Cloud at 2 ml each, delivery in Cairo, a thick bar, then the total set large.
7. **Footer.** Split in half. Left: a very tight crop of the label from the photograph, cropped by the left and bottom edges. Right, on espresso: a small wordmark, then a large stacked menu (Shop the four, Vanilla Reverie, Discovery set, Our story, Order on WhatsApp). On hover the hovered item shifts right and the others dim. Below the menu: contact (WhatsApp, Cairo) and Instagram, then a small copyright line.

## Motion

Slow ease-out only; nothing bounces or spins.

- **Hero:** the bottle slides in, the headline rises line by line, light glints across the cap, a band of light passes across the glass, and the bottle floats gently.
- **Close-up section:** the photograph opens with a shutter (clip from the top) while it settles from 1.12× scale. This is the page's one big motion moment.
- **Every section:** heading, text and picture rise in with a staggered delay as the section scrolls into view.
- **Other movement:** the notes band moves slowly left, and the photographs drift slowly in scale.
- **Controls:** buttons press on click, rows react on hover, and the selected juice colour changes smoothly.
- **Reduced motion:** with `prefers-reduced-motion`, show everything static.

## Technical

- **Responsive:** works from 360px wide.
  - On a phone the hero bottle moves to the top and the headline sits under it.
  - The travelling bottle in the list is hidden, and rows stack.
  - The close-up card docks to the bottom of the photograph.
  - The footer photo comes first, then the menu.
- **Accessibility:** real `<button>` and `<a>` elements with visible focus, alt text on every image, and WCAG AA contrast.
- **Imagery:** one real product photograph (Vanilla Reverie on marble with vanilla flowers and pods), used in three different crops. Everything else is a flat drawing of the bottle. More product photography is welcome, especially one shot per signature.

## Placeholders — do not invent

Bottle and set prices, the delivery fee, the WhatsApp number, the Instagram handle, and the measured longevity times. Show the times as `[PRICE] EGP` style placeholders until they are real.
