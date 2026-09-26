# Your Planboard — from zero to a website you control

This folder contains a **working starter website** for breaking a difficult problem into a plan. It is intentionally small enough for an ASUS VivoBook E410KA running Windows 11: one HTML file, with its CSS and JavaScript inside. There is **no Node.js, Docker, paid software, build command, external font, analytics, or third-party image** to install. E410KA configurations vary, so these steps do not depend on a particular processor or memory size.

- `index.html` — the complete website. You can edit, copy, and publish it.
- `README.md` — this guide.

The example website lets you create several plans, describe goals and dates, add and complete steps, filter steps, see progress, and download/import a JSON backup. It saves plans **in the browser on that device**, not in a shared online account. The sample plan is editable and can be deleted.

## Step 0 — decide what problem your eventual website will solve

Before you change any code, write answers to these five questions in a notebook:

1. **Who** will use the site? Be specific.
2. **What one problem** do they face?
3. **What is the one main action** they should take on your site?
4. **What are the first three features** that make that action possible?
5. **How will you tell** if it helped? (For example, five real people complete the action.)

Example: “Students in my class need to organize exam preparation; the main action is turning a chapter into a set of study steps.” Your Planboard is a working example of that general pattern. It does **not** automatically implement bookings, shared accounts, payments, or AI for a different problem; those need additional development.

## Step 1 — put the files on your Windows 11 laptop

1. Download `index.html` and `README.md` from the provided starter folder. Keep them together in a folder such as `Documents\Your-Planboard`.
2. In File Explorer, double-click `index.html`. It should open in Microsoft Edge or your default browser. **You do not need an internet connection to try this local copy.**
3. If Windows opens it in an editor, right-click `index.html` → **Open with** → **Microsoft Edge**. Check that its name is `index.html`, **not** `index.html.txt`. File Explorer → **View** → **Show** → **File name extensions** displays extensions.
4. If your laptop is slow, close unused browser tabs before editing. You do not need a virtual machine or heavyweight development tools for this starter.

> Double-clicking a local HTML file usually works. Some browsers restrict storage for `file://` pages. If the page says “Not saved · export a backup,” you can still test it, but export your work; publish it using Step 5 for a stable website address.

## Step 2 — learn the working example

1. Edit the sample plan “Build a helpful website,” or press **Create a new plan**.
2. Write the problem in **What are you working on?** and the result you want in **What would success look like?**
3. Optionally set a date, then type one doable action and press **Add step**. Choose High / Normal / Low priority.
4. Check a step to complete it. Try the **All**, **Open**, and **Done** filters. The progress circle updates.
5. Press **Export**. A `your-planboard-backup-....json` file downloads. Save that somewhere safe; **do not upload private plan backups to your public website repository**. Press **Import** to add plans from a backup. Import **adds** plans rather than deleting your existing ones.
6. Refresh the page. Your plans should still be there. Browser private/incognito mode, clearing site data, switching browsers, or switching devices can remove or separate these plans. Export regularly.

**Important:** the local file address and your published GitHub Pages address are separate browser locations. Plans will **not** move automatically. Export locally, then open the published website and import the backup if you want the same plans there.

## Step 3 — edit the website without installing anything

1. Right-click `index.html` → **Open with** → **Notepad**. An optional nicer editor is Visual Studio Code from its official website, but Notepad is sufficient.
2. Press **Ctrl+F** to find `Hard problems,` and edit the homepage heading in the HTML. Search for `your planboard` to change the visible name; also edit the `<title>` and `<meta name="description">` near the top.
3. For colors, find `:root` near the start of the `<style>` block. Try changing `--ink` or `--green-light` to another hex color, such as `#234d5b`. Keep the variable names unchanged.
4. Find the “A simple method” section near the bottom of the HTML to rewrite the three explanatory cards. The code below `<script>` controls how plans and steps work; make a copy of the file before changing that code.
5. Press **Ctrl+S** to save. Return to Edge and press **Ctrl+R** to see your changes. Keep the file ending in `.html`, not `.txt`.

A website has three basic ingredients: **HTML** for the content and structure, **CSS** for its appearance, and **JavaScript** for interactions. This starter keeps all three in one place to reduce setup and make backups easy.

## Step 4 — test before you publish

- Create a new plan, add a step, mark it complete, export, refresh, and import the backup.
- In Edge, press **F12**, then click the phone/tablet icon (or press **Ctrl+Shift+M**) to inspect the narrow-screen layout. Press F12 again to close the tools.
- Ask one person to try the site and watch where they get stuck. Fix that before adding many features.
- Never paste a password, secret API key, or private exported backup into `index.html`. Anyone can view the source of a published static page.

## Step 5 — publish a free starter URL under YOUR account

These are browser-only steps; you do **not** need to install Git to publish the first version.

1. Create a GitHub account using **your own email address**. Turn on two-factor authentication and retain your recovery codes.
2. At GitHub, choose **New repository**. Name it, for example, `your-planboard`. Choose **Public** for a free GitHub Pages site on a personal account. You can leave the initialize-with-README options unchecked. Create the repository.
3. In that repository, choose **Add file → Upload files**. Upload **`index.html`** from your folder. You may upload `README.md` too. Select **Commit changes**. Make sure `index.html` is in the **top level** of the repository, not inside another folder.
4. Go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch** as the source. Select the **main** branch and **/(root)** folder, then **Save**. GitHub's menu labels may change slightly over time.
5. Wait for deployment, then open the URL shown on the Pages settings screen. It is usually `https://YOUR-USERNAME.github.io/your-planboard/`. Replace `YOUR-USERNAME` with your username. If it does not open immediately, give deployment a few minutes and check the repository's **Actions** tab for errors.
6. To update the site later, edit your local `index.html`, upload that changed file to the same repository, and commit the change. Refresh your published site after deployment.

**Public means public source code.** Do not upload your exported plan JSON, personal documents, passwords, or private keys. GitHub Pages serves these static files; it does **not** turn this example into a multi-user app or synchronize browser data across visitors.

## Step 6 — get your own domain (optional)

The free GitHub Pages address is already a real public website. If you want something like `www.example.com`, buy a domain from a registrar using **your own** name, email, payment method, and login. In the repository's **Settings → Pages**, enter it under **Custom domain**. Then follow GitHub Pages' current DNS instructions at your registrar and enable **Enforce HTTPS** once available. A domain normally has a renewal charge; keep billing access and renewal reminders under your control. No domain is required to own or use these files.

## Step 7 — keep actual control and ownership

- The provided starter files are yours to copy, modify, and publish. They contain no externally licensed stock images, CDN assets, or framework dependencies. Add **your own** writing, branding, photographs, and other assets only when you have the rights to use them.
- Keep the source files and periodic JSON exports on a drive **you control**, with a second backup if the work matters to you.
- Use **your own** GitHub, registrar, and hosting accounts. Keep two-factor authentication and recovery access. You do not need to give me or anyone else your password.
- The repository belongs under your account; the domain registration belongs in your name. Hosting companies still operate their own platforms subject to their terms. This guide does not register a domain or make a legal transfer of third-party rights on your behalf.
- Copyright treatment of AI-generated material depends on local law and your own creative contributions. For a business where legal ownership is critical, obtain legal advice and add your original text, design, and functionality.

## Step 8 — when your problem requires a more demanding website

This starter is **static and local-first**. The laptop edits the files; the hosting provider serves visitors. Your E410KA does not have to handle the visitor traffic. Add complexity only when there is a real need:

| Need | Next step |
| --- | --- |
| More pages and public information | Add HTML pages and link to them; keep images compressed. |
| People need to share data across devices | Add a hosted backend and database. Browser `localStorage` is not shared storage. |
| User accounts | Use a trusted authentication service; check access permissions on the server. |
| Payments | Use a reputable payment provider; never collect card details in this starter. |
| AI, huge files, or intensive calculations | Run the expensive work on a hosted server/API, not on this laptop or inside a public secret-bearing JavaScript file. |
| Real users' personal information | Plan consent, security, access rules, backups, a privacy notice, and applicable legal requirements before collection. |

When you grow beyond this starter, build one feature at a time, test it with users, and use a host that supports the backend you choose. **Never put API secrets in a public HTML/JavaScript file.** The starter's browser storage is not appropriate for sensitive information or team collaboration.

### Quick troubleshooting

- **Blank page?** Ensure the file is named `index.html` and open it in Edge. If you changed the `<script>`, restore the original from your backup.
- **Work disappeared?** Check that you are using the same browser and same address. Import a previously exported JSON backup. Clearing site data can erase browser storage.
- **Pages link says 404?** Confirm `index.html` is at the repository root, Pages is set to **main / (root)**, and deployment has finished.
- **Need to own it?** Keep the repository, source files, domain, account recovery, and billing in your own name. The visible site name alone does not establish that control.
