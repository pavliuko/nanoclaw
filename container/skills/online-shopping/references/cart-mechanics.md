# Cart Mechanics

Store "add" buttons often fail and show no error. Do not trust an add until the cart page shows the item.

## Add items

1. Open the product page of the item. Do not add from a tile in the search results. Tile buttons often do nothing and show no error.
2. On the product page, make sure that the size and the price are the same as in the list that got the "yes". A search result can open a different size.
3. Read the cart counter and the cart total in the page header.
4. Run `agent-browser snapshot -i` to get fresh element refs. Pages move after banners load, so old refs can point to the wrong element.
5. Click the add button by its ref.
6. Read the cart counter and the cart total again. If they did not change, the add failed.
7. After not more than 5 adds, open the cart page. Compare it with the list that got the "yes".

Do not tell the user that an item is in the cart before step 7 shows it.

## Wait for a page

Follow the rule in the `agent-browser` skill. Every wait must have a time limit and a maximum number of attempts. If the wait times out, take a snapshot and report what you see. Do not start the same wait again.

## Items sold by weight

Fresh produce often has a unit stepper that maps to a weight, for example "4 un = 1.04 kg". Select the value nearest to the requested weight. Tell the user the real weight and price. The store weighs these items again on the delivery day.

## Keep the session

1. Do not run `agent-browser close` during a shopping session. A new browser can open as a guest with an empty cart.
2. These signs show that the session ended:
   - The header shows "Login" or "Register".
   - The cart becomes empty.
   - The delivery address changes to a default.
   - The site language changes.
3. If you see one of these signs, stop all cart changes. Follow `references/login.md`.

## Keep the cart in sync with changes by the user

The user can also change the cart in their own browser or app.

1. Keep your own list of the items you added in this session.
2. Before each batch, read the full cart again. Compare it with your list.
3. If items disappeared, appeared, or changed quantity, tell the user. Ask if the user made the change.
4. Do not add again an item that disappeared. The user possibly removed it on purpose.

## When the browser fails

Try the command again one time. If it fails again, stop. Tell the user what you completed and what is not done.
