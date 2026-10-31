# Comparing Stores

Compare the same product in different stores. Compare the full cost, not the shelf price.

## Search without a session

You can search a store without a browser session. Prices for guests can be different from prices for logged-in users, for example loyalty-card prices. Tell the user which prices you read as a guest.

Do not add items to a guest cart. The user cannot see a guest cart.

## Find the same product

Two offers are the same product only when these values are the same:

- **Electronics and appliances:** brand, model number, memory or capacity, colour, region version. Use the EAN or the manufacturer part number if the page shows it.
- **Clothes and shoes:** brand, model, size, colour. Size charts can be different between brands. Read the size chart of the store.
- **Groceries:** brand, product name, size or weight.

If one value is different, the offers are similar, not the same. Tell the user the difference.

## Full cost

For each offer, read these values from the store pages:

1. The price of the product.
2. The delivery cost to the address of the user. Read the minimum order value for free delivery.
3. Other costs, for example a deposit, a service fee, or an installation fee.

The full cost is the sum of these values. If you cannot read a value, tell the user. Do not use a value from memory without the date of that value.

## Other differences

Tell the user these differences when they exist:

- **Seller.** On marketplace sites, a third-party seller can sell the product, not the store. Read the seller name. Third-party sellers can have different return rules and a different warranty.
- **Delivery time.** Read the delivery date or the delivery time on the page.
- **Return policy.** Read the return period if the product is clothes, shoes, or electronics.
- **Reviews.** Give the rating and the number of reviews. A high rating from few reviews is weak evidence.

## Message format

Send one line for each store: the store, the price, the delivery cost, the full cost, the delivery time, and other differences.

```
1) Worten — €249,99 + доставка €0 = €249,99, завтра
2) Fnac — €239,99 + доставка €4,99 = €244,98, 3–5 днів, сторонній продавець
Який? Відповідай номером.
```

The example is in Ukrainian. Write the message in the language of the user.
