# MSSR Legislation

The official website for the law of the Mongey Squidy Soviet Republic, published at **legislation.mssr.work.gd**.

Within MSSR only. MSSR is a virtual state and has no standing under the law of the United Kingdom. This is not a government website.

## What is in this folder

| File or folder | What it does |
| --- | --- |
| `laws/` | The text of every law, one file each (for example `laws/constitution.md`) |
| `data/laws.json` | The list of every law: its title, type, status, dates and plain-English summary |
| `data/gazette.json` | The Official Gazette entries |
| `index.html`, `browse.html`, `law.html`, `gazette.html`, `search.html`, `about.html` | The pages of the site. You never need to edit these |
| `assets/` | The look of the site (colours, crest) and the code that builds each page |
| `CNAME` | Tells GitHub to use the address legislation.mssr.work.gd |
| `robots.txt` | Asks search engines not to list the site |
| `.nojekyll` | Tells GitHub to show the files exactly as they are |

## How to add a new law

Two steps. Both are done on github.com, no coding needed.

### Step 1: add the law's text

1. Open the `laws` folder on GitHub.
2. Click **Add file**, then **Create new file**.
3. Name it with lowercase words and dashes, ending in `.md`. For example: `crimes-act-2026.md`.
4. Paste in the law's text. Copy the layout from `_template-act.md`:
   - `#` the title
   - `##` a Part (for example `## Part 1 — Offences`)
   - `###` a numbered section (for example `### 1. Theft`)
   - `(1)`, `(2)` subsections and `(a)`, `(b)` paragraphs, each as its own line with a blank line between
5. Click **Commit changes**.

### Step 2: add it to the list

1. Open `data/laws.json` and click the pencil icon to edit.
2. Copy the whole block for the Constitution, from `{` to `}`.
3. Paste it after the last block, and put a comma `,` after the `}` of the block before it.
4. Change the details:

| Field | What to put |
| --- | --- |
| `id` | A short name with dashes, used in the address. For example `crimes-act` |
| `type` | `act`, `regulation`, `case` or `constitution` |
| `title` | The full title |
| `shortTitle` | A short title |
| `number` | The Act's number that year, for example `"1"` |
| `year` | The year, for example `2026` |
| `status` | `In force`, `Not yet in force`, `Draft` or `Repealed` |
| `inForce` | The date it came into force, written `YYYY-MM-DD` |
| `madeBy` | For example `Presidium Assent, Resolution No. 2` |
| `file` | The file from step 1, for example `laws/crimes-act-2026.md` |
| `summary` | A few short sentences in plain English, each in quotes, separated by commas |

5. Click **Commit changes**. The site updates within a minute or two.

## How to add a Gazette entry

Open `data/gazette.json`, copy the last entry, paste it at the end (with a comma between entries), give it the next `number`, and change the date, title and text.

## Changing a law

Edit its file in `laws/` and commit. GitHub keeps every old version automatically, and the site links to that history from each law.

## Rules

- Usernames only. Never put a real name or personal details in any law or Gazette entry (Constitution, section 42).
- Only publish a law once it has Presidium Assent, and record the Assent in the Gazette.
