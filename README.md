<p align="center">
  <img src="./docs/logo.png" alt="Friendly DB" width="600" />
</p>

# Friendly DB

**Visualize your PostgreSQL schema in seconds — no backend, no install. Paste your DDL and you instantly get an interactive diagram. No accounts, no servers — everything runs in the browser.** 

> 🌐 **[friendlydb.app](https://friendlydb.app)**

---

## Why this exists

I built this for myself.

I've been working with Supabase for a while, and as projects grow and tables pile up, making sense of the schema becomes painful. What references what? Does this table have an index on the FK? Is there a `text` column without a length that'll throw a warning later? The Supabase editor helps but doesn't give you the bird's-eye view you actually need.

So I made **Friendly DB**: paste your DDL and you instantly get an interactive diagram. No accounts, no servers — everything runs in the browser.

Sharing it in case it's useful to anyone else. 🙌

---

## Demo

![Friendly DB demo](./public/demo.gif)

---

## Screenshot

![Friendly DB — analyzer](./docs/screenshot-app.png)

---

## What it does

- **Interactive diagram** — Tables appear as draggable cards. Rearrange them however you want, and **group related chains at different nesting levels** to build the mental model that makes sense for your project.
- **Visual foreign keys** — Relationships are drawn as lines between tables. Select a table and its incoming/outgoing FKs light up immediately.
- **Anti-pattern warnings** — Flags FKs without indexes, tables without a primary key, and `text`/`varchar` columns without a specified length.
- **Fast search** — `⌘K` / `Ctrl+K` to jump to any table or column instantly.
- **Export** — Download the diagram as PNG or SVG to share with your team.
- **Shareable link** — Generate a URL with the schema embedded in the hash so anyone can open it without re-pasting the SQL.
- **No backend** — All parsing and rendering happens in the browser. Your SQL never leaves your machine.

---

## How to use it

1. Go to **[friendlydb.app](https://friendlydb.app)**
2. Click **"Open analyzer →"**
3. Paste your PostgreSQL DDL into the modal (copy directly from Supabase, psql, or any client)
4. Done — the diagram appears instantly

The app loads a built-in example schema on first open, so you can explore all features right away without any setup.

---

## Compatibility

Works with any PostgreSQL database:

| Platform | Status |
|---|---|
| Supabase | ✅ |
| Neon | ✅ |
| Railway | ✅ |
| Amazon RDS | ✅ |
| Fly Postgres | ✅ |
| Crunchy Data | ✅ |
| Timescale | ✅ |
| Local PostgreSQL | ✅ |

> The parser supports `CREATE TABLE` with inline and table-level constraints, and `ALTER TABLE ... ADD CONSTRAINT ... FOREIGN KEY`.

---

<p align="center">Made by a Flutter lover ❤️</p>
