**Your tasks:** Process my unstructured notes below.

**1. Generate Markdown File Content:**
_ Synthesize notes into well-structured Markdown content suitable for saving as a `.md` file.
_ Use concise points, headings, and lists (especially bullet points) for organization based on the notes. \* Present this complete Markdown content within a single code block for easy copying and saving as a `.md` file.

**2. Generate Bulk Jira JSON:**
_ From the notes, identify all action items (subject, description).
_ Create **one single JSON object** for Jira's bulk create API (`POST /issue/bulk`), structured as `{"issueUpdates": [ /* Action items go here */ ]}`.
_ For **each** action item, add an object to the `issueUpdates` array with the following `fields`:
_ `project`: `{"id": "10433"}` (Fixed: Project RAS)
_ `issuetype`: `{"id": "10002"}` (Fixed: Task)
_ `summary`: The action item's subject.
_ `description`: The action item's description, formatted as an **ADF bulleted list** (see template below).
_ `labels`: Up to 3 intelligently generated relevant labels (lowercase, hyphenated, e.g., `api`, `vendor-x`). Default to `["meeting-action"]` if none inferred for an item.
\_ **ADF Bullet List Template for `description`:** (Create a `listItem` per point/sentence in the description)

```json
{ "type": "doc", "version": 1, "content": [ { "type": "bulletList", "content": [ { "type": "listItem", "content": [ { "type": "paragraph", "content": [ { "type": "text", "text": "<Point text>" } ] } ] } /_ Add more listItems _/ ] } ] }
```

\_ Output the complete single JSON object in one code block.

**Output:** Provide the Markdown file content (Task 1) and the bulk JSON (Task 2) in separate, clearly labeled code blocks.

**My Unstructured Notes:**
[Paste your unstructured meeting notes here]
