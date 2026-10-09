# Payload strikethrough repro

Minimal [Payload CMS](https://payloadcms.com) project to reproduce a bug with **strikethrough** in the rich text (Lexical) editor. SQLite database, no external services.

## Setup

```bash
npm install
cp .env.example .env   # already committed as .env locally
npm run dev
```

## Reproduce

1. Open http://localhost:3000/admin
2. Create the first admin user (stored in the local SQLite file).
3. Go to **Posts** > **Create New**.
4. In the **Content** rich text field, apply **strikethrough** to some text.

## Notes

- `src/collections/Posts.ts` holds the rich text field that uses the default `lexicalEditor()` from `src/payload.config.ts`.
- Bug description / steps go here.
