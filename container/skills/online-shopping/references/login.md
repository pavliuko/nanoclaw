# Login and Browser Session

You log in to the store account of the user yourself. The user gives you the username and the password in chat.

A store password is not a gateway credential. The rule "keep real credentials in the gateway" is for API tokens. A store website has no API that a gateway can use. The user decided that you keep the store password in a file and type it into the login form.

## Files

A store can have two files in `/workspace/agent/browser-state/`:

- `<domain>.json` — the browser session (cookies). Example: `continente.pt.json`.
- `<domain>.login.json` — the username and the password. Example: `continente.pt.login.json`:

  ```json
  {"username": "name@example.com", "password": "..."}
  ```

## Load the session

1. If the session file exists, load it before you open the store:

   ```bash
   agent-browser state load /workspace/agent/browser-state/continente.pt.json
   agent-browser open https://www.continente.pt
   ```

2. Make sure that the page shows the account name or the account menu. If it shows a login link, for example "Login", "Entrar", or "Login ou Registo", the session expired. Go to [Log in](#log-in).
3. If the session file does not exist, open the store and go to [Log in](#log-in).

## Log in

1. If the login file does not exist, ask the user for the username and the password of this store. When the user replies, write the login file. Set its file mode to 600. Do not ask again in later sessions.
2. Open the login page of the store. If the store has a reference file, read its login section.
3. Use `agent-browser snapshot -i` to find the fields and the buttons.
4. Type the username and the password. Click the submit button.
5. Some stores show the password field only after you submit the username. On these stores, submit each page.
6. If the store asks for a code from SMS or email, ask the user for the code. Type it when the user replies.
7. Make sure that the page shows the account. Then [save the session](#save-the-session).

If the store says that the username or the password is wrong:

1. Do not try again with the same password. Many failed logins can lock the account.
2. Tell the user. Ask for the correct password. Write it to the login file.

If you cannot pass a step, for example a CAPTCHA, stop. Tell the user what the page shows. Then offer the [operator login](#operator-login).

## Save the session

The store changes the session cookies over time. Save the session after each login and at the end of each shopping session, so the next session starts logged in.

1. Make sure that the page still shows the account. Do not save a guest session over a good file.
2. Save to the same path:

   ```bash
   agent-browser state save /workspace/agent/browser-state/continente.pt.json
   ```

## Operator login

Use this only when you cannot log in yourself, for example because of a CAPTCHA. The operator logs in on the computer that runs NanoClaw. Send these steps to the user. Replace `<domain>`, `<agent folder>`, and the URL.

```
cd <nanoclaw folder>
npx -y agent-browser@0.27.1 install
npx -y agent-browser@0.27.1 --headed open https://www.continente.pt
```

Then:

1. In the browser window, log in and select the delivery address.
2. Save the session to the folder of this agent:

   ```
   npx -y agent-browser@0.27.1 state save groups/<agent folder>/browser-state/<domain>.json
   npx -y agent-browser@0.27.1 close
   ```

3. Tell the agent that you finished the login.

The first command is necessary only one time on a computer. It downloads Chrome.

When the user says that they finished the login, start again at step 1 of [Load the session](#load-the-session).
