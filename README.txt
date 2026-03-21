ERAS Pocket Guide — Local Setup
================================

FILES IN THIS FOLDER
--------------------
  index.html        — Viewer (open this on iPhone/desktop)
  eras-editor.html  — Editor (open this to add/edit protocols)
  protocols.json    — Protocol data (this is your database)
  README.txt        — This file

HOW IT WORKS
------------
All protocol data lives in protocols.json. No internet connection,
no accounts, no servers required to view or edit protocols.

VIEWING PROTOCOLS (iPhone or any browser)
-----------------------------------------
Open index.html in any browser. It reads protocols.json automatically.
If protocols.json is not found it falls back to the baked-in seed data.

On iPhone: use the Files app or AirDrop to copy the folder, then open
index.html with Safari. Add to Home Screen for an app-like experience.

EDITING PROTOCOLS
-----------------
1. Open eras-editor.html in a browser
2. Make your changes (add protocols, edit interventions, add visual aids)
3. Click "Save protocols.json" in the top bar
4. Your browser will download an updated protocols.json
5. Replace the protocols.json in this folder with the downloaded one
6. The viewer will now show your changes

DOCUMENT UPLOAD (optional — requires Anthropic API key)
--------------------------------------------------------
To upload a PDF or Word doc and have Claude parse it into a protocol:
1. Get a free API key at console.anthropic.com
2. In the editor click Settings (gear icon) and paste your key
3. Click "+ Add Protocol" → "Upload Document"
Keys are stored in your browser only — never sent anywhere except Anthropic.

IMAGE UPLOAD FOR VISUAL AIDS (optional — requires ImgBB key)
-------------------------------------------------------------
Visual aid images are uploaded to ImgBB free hosting (the URL is stored
in protocols.json rather than the raw image data, keeping the file small).
1. Get a free API key at api.imgbb.com
2. In the editor click Settings and paste your ImgBB key
Without a key, image upload will fail with an error message.

SHARING UPDATES WITH COLLEAGUES
--------------------------------
After editing and downloading protocols.json, share the updated file
with anyone who has the ERAS folder. They replace their protocols.json
and the viewer immediately shows the new content.

For a shared live experience (everyone sees edits instantly), deploy
to Netlify Drop (app.netlify.com/drop) — drag the whole folder and
Netlify hosts it for free at a public URL.
