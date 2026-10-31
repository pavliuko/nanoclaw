# Restock Check

Find the staples that the household probably needs before they see an empty package. Do this check only after you finish the requested list, or when the user asks.

## Sources

Use these sources in this order:

1. `memory/shopping/purchases.md` — your own purchase log.
2. Order history in the store account, for the last 2 to 3 months.
3. The favourites list in the store account.

## Find staples that are running out

1. Find the items that the household buys again and again. Typical staples: toilet paper, kitchen paper, water, laundry detergent, dishwasher tablets, bin bags, oil, salt, coffee, toothpaste, cleaning products.
2. For each staple, calculate the usual interval between purchases. Use the real dates of this household, not general rules.
3. Compare the interval with the time since the last purchase:
   - The time is longer than the interval: the item is **probably finished**.
   - The time is a little shorter than the interval: the item is **finishing soon**. Example: the household buys coffee every 4 weeks, and the last purchase was 3 weeks ago.
   - The household bought the item only one time: it is not a staple. Ignore it.
4. Send a short list. Put the most overdue items first. Show the reason for each item.

Example message in Ukrainian:

```
Схоже, закінчились:
1) Туалетний папір — купували 8 тижнів тому, зазвичай кожні 5
2) Пральний порошок — 7 тижнів тому, зазвичай кожні 6
Скоро закінчиться:
3) Кава — 3 тижні тому, зазвичай кожні 4
Що додати? Відповідай номерами.
```

The user knows what is in the cupboard. The list is a suggestion. Never add these items without a "yes".

## Favourites

Do not send the full favourites list. Select not more than 10 items in two groups:

1. Items with a promotion now.
2. Items that the household buys often and that are not in the cart.

The favourites also show the taste of the user: region, producer, style, price level. Use this when the user asks for "something similar". Tell the user the pattern you see, so they can correct it.

If the user usually buys a more expensive version of an item in the cart, tell the user the unit-price difference. Offer the change. Do not make it without a "yes".

## Next step

Process the items that got a "yes" with steps 3 to 6 of the main workflow. A staple with a promotion now is a good item to buy in quantity. A staple without a promotion can possibly wait one week.
