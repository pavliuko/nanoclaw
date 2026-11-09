# Clothing Fit

Select a size from measurements and history, not from the size label. Read this file before you recommend or add clothes or shoes.

## Reference measurements

1. Read the sizes and the reference garment of the user in `memory/shopping/preferences.md`. A reference garment is one item that fits well, measured flat in centimetres: chest (pit to pit), length, shoulder, sleeve.
2. If there is no reference garment, ask the user for one. Write the answer to `preferences.md`.

## Size chart

1. Read the size chart on the product page or the size guide of the store.
2. A conversion table (S = 46–48 and so on) or a body chart is not a garment chart. If the store shows only one of these, open the size guide on the site of the brand. Brand sites often publish garment measurements.
3. Compare the garment chart with the reference garment. Select the size with the nearest chest width and length. Tell the user the numbers, for example "XXL: 63,5 / 80 cm, your tee 62 / 74 cm".
4. Read how the store or the brand measures the length. Some brands measure from the shoulder seam, not from the highest shoulder point. Their length reads 1–2 cm shorter.
5. If no garment chart exists, estimate from the fit type ("regular", "loose", "oversized"), the size that the model wears and the model height, and the store hint (for example "Veste grande" on Zalando). Tell the user that the size is an estimate.

## Label traps

- The same label means different sizes in different brands. Japanese and Asian labels are often one size smaller than EU or US labels (Asia XXL ≈ US XL).
- A sale filter or a listing filter for a size does not prove stock in that size for each colour. Read the size picker on the product page for the colour you recommend.
- A set (top and pants) that is sold as one size can fit on the top and not on the pants. Prefer sets where the pieces are sold separately.

## History

1. If the store has an order history, read it before you recommend clothes. Items the user kept show taste and fit. Items the user returned show the opposite.
2. Give the past order as evidence, for example "you kept Les Deux Stamp tee, order 2026-09".
3. Items that the user left in the cart between rounds are the strongest signal of taste. Items that the user removed are a signal against.
4. Write new size facts to `preferences.md` with the date. Example: "Les Deux XL too small (order 2026-10-25), use XXL".
