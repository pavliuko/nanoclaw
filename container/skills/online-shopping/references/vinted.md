# Vinted

Facts about vinted.pt and other Vinted sites. Write new facts that you learn to `memory/shopping/stores/vinted.pt.md`, not to this file.

Vinted is a marketplace of used items from private sellers. Each item is one piece. There is no cart for many items from different sellers, and no size choice.

## Search

- Use the category (for example "Homem") and the size filter. Sort by relevance and also by newest. New listings sell fast.
- Search with several queries: the brand, the brand and the type (hoodie, crewneck, cardigan), and style words ("oversized", "boxy", "heavyweight").
- vinted.pt shows only items that can ship to Portugal.
- Item URL: `https://www.vinted.pt/items/<id>`. Give the ID and the link for each item.

## Price

- The price on the listing includes the buyer protection fee. Shipping is extra. Tell the user both.
- Some sellers accept offers ("negotiable"). Do not send an offer without a "yes" from the user.

## Condition and status

- Condition labels, from best: "Novo com etiquetas", "Novo sem etiquetas", "Muito bom", "Bom", "Satisfatório". Skip "Satisfatório" unless the user asks.
- Open the item page before you recommend an item. Check that it is not reserved, not sold, and not deleted. A sold item shows a "Sold" label. A deleted item returns 404.
- Before you send an old list again, check each item again.

## Size

- Listings rarely give measurements. Read the description and the photos for a measurement. If the seller gives measurements, compare them with the reference garment in `references/clothing-fit.md`.
- Sellers often say how the size fits, for example "XXL fits like L". Trust this over the label.

## Fakes

Fakes are common for designer and streetwear brands. Read the description: some sellers say that the item is not genuine, or that it is a parody. Tell the user when the listing gives no proof of authenticity, such as a receipt or the tag.

## Rate limits

Vinted can return HTTP 429 or a "Session refresh" page after many item pages. Wait, then reload the catalog page. Tell the user how many item pages you could read.

## Do not buy

Buying on Vinted pays at once. Critical rule 1 applies: do not click "Comprar". You can add an item to favourites when the user asks.
