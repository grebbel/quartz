In **Quartz**, updating your site with new documents (Markdown notes) is a **manual process** that involves adding, committing, and pushing changes to your GitHub repository. Here’s how it works and how to automate or streamline the process:

---

---

## **1. Manual Update Process**
### **Step-by-Step Workflow**
1. **Add New Documents:**
   - Place your new Markdown files (e.g., `new-note.md`) in the **`content/` folder** of your local Quartz repository.
   - Organize them into subfolders if needed (e.g., `content/research/`, `content/meetings/`).

2. **Preview Locally (Optional):**
   - Run the following command to preview your site locally and ensure the new notes render correctly:
     ```bash
     npx quartz build --serve
     ```
   - This starts a local server (usually at `http://localhost:8080`). Check that your new notes appear as expected.

3. **Commit Changes:**
   - Use Git to stage and commit your changes:
     ```bash
     git add content/new-note.md
     git commit -m "Added new research note on zoonoses"
     ```

4. **Push to GitHub:**
   - Push the changes to your GitHub repository to update the live site:
     ```bash
     git push
     ```
   - GitHub Pages will automatically rebuild your site with the new content.

5. **Verify the Update:**
   - Visit your deployed site (e.g., `https://grebbel.github.io/quartz/`) to confirm the new notes are live.

---

---
## **2. Automating Updates**
While Quartz itself doesn’t auto-sync local files to GitHub, you can use **third-party tools** or **scripts** to streamline the process:

### **Option A: GitHub Desktop**
- Use [GitHub Desktop](https://desktop.github.com/) to:
  - Drag and drop new Markdown files into the `content/` folder.
  - Commit and push changes with a GUI (no command line required).

### **Option B: Script for Bulk Updates**
- Create a **Bash script** (e.g., `update_quartz.sh`) to automate the process:
  ```bash
  #!/bin/bash
  git add content/
  git commit -m "Updated notes on $(date +%Y-%m-%d)"
  git push
  ```
- Run the script whenever you add new files:
  ```bash
  chmod +x update_quartz.sh
  ./update_quartz.sh
  ```

### **Option C: Obsidian + Quartz Sync**
- If you use **Obsidian** for note-taking:
  1. Store your Obsidian vault in the same folder as your Quartz `content/` directory.
  2. Use the **`npx quartz sync`** command to sync changes from Obsidian to Quartz.
  3. Commit and push the updates to GitHub.

### **Option D: GitHub Actions (Advanced)**
- Set up a **GitHub Actions workflow** to auto-deploy your site when changes are pushed to a specific branch (e.g., `main`).
- Example workflow file (`.github/workflows/deploy.yml`):
  ```yaml
  name: Deploy Quartz
  on:
    push:
      branches: [ main ]
  jobs:
    deploy:
      runs-on: ubuntu-latest
      steps:
        - uses: actions/checkout@v4
        - uses: actions/setup-node@v4
          with:
            node-version: 22
        - run: npm install
        - run: npx quartz build
        - run: |
            git config --global user.name "GitHub Actions"
            git config --global user.email "actions@github.com"
            git add .
            git commit -m "Auto-deploy Quartz"
            git push
  ```
- This will **automatically rebuild and deploy** your site whenever you push changes to the `main` branch.

---
---
## **3. Syncing with External Tools**
### **Obsidian**
- Quartz is **compatible with Obsidian**:
  - Use the **Obsidian Git plugin** to automatically commit and push changes from Obsidian to your Quartz repository.
  - Enable **wikilinks** and **backlinks** in Obsidian to match Quartz’s linking system.

### **Roam Research**
- Quartz supports **Roam Research compatibility**:
  - Export your Roam notes as Markdown and place them in the `content/` folder.
  - Use the `npx quartz sync` command to process Roam-style notes.

### **Notion (via Export)**
- Export Notion pages as Markdown (using tools like [Notion2MD](https://github.com/souvikns/notion2md)) and add them to `content/`.

---
---
## **4. Best Practices**
1. **Organize with Folders/Tags:**
   - Use subfolders (e.g., `content/projects/`, `content/literature/`) and **tags** (e.g., `#microbiology`, `#one-health`) to keep notes structured.

2. **Version Control:**
   - Commit changes **frequently** with descriptive messages (e.g., `"Added notes on zoonoses transmission pathways"`).

3. **Preview Before Pushing:**
   - Always preview locally (`npx quartz build --serve`) to catch formatting issues or broken links.

4. **Backup:**
   - Regularly back up your `content/` folder to avoid losing notes.

---
---
## **5. Troubleshooting**
| Issue                          | Solution                                                                 |
|--------------------------------|--------------------------------------------------------------------------|
| New notes not appearing        | Check for typos in filenames or Markdown syntax. Run `npx quartz build` locally to debug. |
| GitHub Pages not updating      | Ensure GitHub Pages is set to deploy from the correct branch (e.g., `main` or `gh-pages`). |
| Broken wikilinks               | Verify that linked notes exist in `content/` and use the correct filename (case-sensitive). |
| Build errors                   | Run `npm install` to update dependencies, then retry `npx quartz build`. |

---
Would you like help:
- Setting up **GitHub Actions** for auto-deployment?
- Configuring **Obsidian or Roam Research** to sync with Quartz?
- Creating a **custom script** for your workflow?