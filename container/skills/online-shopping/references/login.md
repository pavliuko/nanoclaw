# Login and Browser Session

You do not log in. The operator logs in to the store account of the user on the computer that runs NanoClaw. Then the operator gives you a browser state file. The file contains the session cookies of that account. Critical rule 8 applies to it.

Each store has a separate state file. A store without a state file has no session. You can search it as a guest, but you cannot change its cart.

## State file

The path is `/workspace/agent/browser-state/<domain>.json`. Example: `/workspace/agent/browser-state/continente.pt.json`.

## Load the session

1. Make sure that the state file exists. If it does not exist, go to [Ask the operator to log in](#ask-the-operator-to-log-in).
2. Load it before you open the store:

   ```bash
   agent-browser state load /workspace/agent/browser-state/continente.pt.json
   agent-browser open https://www.continente.pt
   ```

3. Make sure that the page shows the account name or the account menu. If it shows a login link, for example "Login" or "Entrar", the session expired. Go to [Ask the operator to log in](#ask-the-operator-to-log-in).

## Save the session

The store changes the session cookies over time. Save the state at the end of each shopping session, so the next session starts logged in.

1. Make sure that the page still shows the account. Do not save a guest session over a good file.
2. Save to the same path:

   ```bash
   agent-browser state save /workspace/agent/browser-state/continente.pt.json
   ```

## Ask the operator to log in

Stop all cart changes in that store. Do not try to log in. Send the steps below to the user, in the language of the user. Tell them these facts:

- Only the operator can do the steps, on the computer that runs NanoClaw.
- The owner of the store account types the password in the browser window.

Replace `<domain>` and the URL with the store.

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
