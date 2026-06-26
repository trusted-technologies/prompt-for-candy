# prompt-for-candy
An open-source repository of prompts containing the skills and knowledge base of the Candy AI chatbot model.

## Structure

- `skills-prompt/` — core persona, behavior, and fallback prompts for Candy AI.
- `moderation-prompt/` — safety moderation prompts used for client and assistant messages.
- `knowledge-base/sections/` — individual knowledge base articles as Markdown files.
- `knowledge-base/knowledge-base.json` — compiled knowledge base ready for import into the WHMCS Candy AI module.

## Knowledge base format

Each `.md` file in `knowledge-base/sections/` contains only a Markdown H1 heading and plain text body:

```markdown
# Web Hosting (ISPmanager)

Website hosting with the ISPmanager panel...
```

The file name (without `.md`) is used as the section ID.

## How to update Candy AI

1. Edit the desired Markdown files in `knowledge-base/sections/`.
2. Regenerate `knowledge-base.json` if the module imports from JSON.
3. Copy the contents of `knowledge-base.json` into the Candy AI module's Knowledge Base editor, or replace the file on the server and run **Dashboard → Update Module** if the module is configured to load from this file.
