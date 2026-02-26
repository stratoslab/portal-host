# PrivaMargin Portal Host

Simple parent app that embeds the PrivaMargin app in an iframe (portal-style).

## Run locally

```bash
cd portal-host
npm install
npm run dev
```

Open the host URL and set the embedded app URL in the input.

You can also pass it as query param:

```text
http://localhost:5173/?app=https://your-privamargin.pages.dev/
```

## Notes

- This host is only a wrapper to satisfy iframe embedding.
- It sends `wallet_event.networkChanged` messages to the child for testing.
- If the child app uses a real wallet SDK bridge, add that integration in this host.
