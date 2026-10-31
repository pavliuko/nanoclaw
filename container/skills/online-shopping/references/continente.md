# continente.pt

Facts about continente.pt. Write new facts that you learn to `memory/shopping/stores/continente.pt.md`, not to this file.

## Pages and buttons

| Name on the site | What it is |
|---|---|
| "Os meus favoritos" | Favourites list |
| "As minhas encomendas" | Order history |
| "Finalizar compra", "Pagar", "Confirmar encomenda" | Checkout and payment. Critical rule 1 applies. |
| "Produto indisponível" | Out of stock. On a result tile this label can be wrong. Read the product page. |
| "Não encontramos resultados para X" | The search found nothing. The results below are for a broader query. |

## Login

1. Open `https://www.continente.pt/login/`. The cookie banner blocks clicks. Close it first. Decline the cookies that are not necessary, as in step 1.7 of the skill workflow.
2. The form is in an iframe from `login.continente.pt`. `snapshot -i` shows the fields inside the iframe. Use their refs.
3. Page 1: type the email or phone number in "Introduza o número de telefone ou email". Click "Avançar".
4. Page 2 can show a password field or ask for a code. Type the password, or ask the user for the code. Then click the submit button.
5. After the login, the header does not show "Login ou Registo".

## Promotions

- **"EM CARTÃO" or "Cartão Continente".** The discount goes to the Cartão Continente balance as credit. The price at checkout does not change. Tell the user this every time.
- **"Poupa Mais".** This is also a card promotion. Read the label to find if it is credit or a direct discount.
- **"Leve 3 Pague 2", "2.ª unidade".** Multi-buy. It is a saving only at the required quantity.
- **PVPR.** Discounts on unknown "Premium" own-label products often start from a PVPR that is not a real price. See `references/deals-and-unit-prices.md`.

## Traps

- Own-label products often use one name and one price for different sizes, for example a 30-dose bag and a 50-dose bag at €4,99. Read the size on the product page.
- Toilet paper and kitchen paper: "2 rolos = 4 rolos" means double-length rolls. Calculate the price for each standard roll.
- Cans and bottles can have a deposit that the unit price does not include.
- Fruit and vegetables use a unit stepper that maps to a weight. See `references/cart-mechanics.md`.
- The prices and the stock depend on the delivery address. Check the address before you compare prices, as in step 1.6 of the skill workflow.
