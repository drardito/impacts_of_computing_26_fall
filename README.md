# 🌐 PHL 3100 / MAC 5100: Impacts of Computing
## Asynchronous Course Repository & Sovereign Learning Web

Welcome to the central node for **Impacts of Computing**. This course investigates data enclosure, digital surveillance, platform decay ("enshittification"), and the ethical structures of modern technology. 

Rather than using a centralized, commercial corporate dashboard that harvests your student usage data, this course operates as a decentralized workspace running directly on your own hardware.

---

## ⚖️ Theoretical Framework: Convivial vs. Manipulative Computing

This course does not merely study digital ethics from a distance; its physical architecture acts as a living laboratory for the ideas of social philosopher **Ivan Illich**. In his 1973 text [*Tools for Conviviality*](https://archive.org/details/toolsforconvivia0000illi), Illich outlines a critical distinction that governs our 14-week infrastructure design:

* **Manipulative (Industrial) Tools:** Technologies designed and enclosed by a corporate elite that strip users of autonomy, enforce conformity, track behaviors, and maximize dependency (e.g., algorithmic timelines, corporate clouds, and centralized, data-harvesting Learning Management Systems).
* **Convivial Tools:** Transparent, accessible infrastructures that give the individuals using them the greatest opportunity to enrich their environment with their own vision. They maximize individual liberty, require no corporate gatekeepers, and encourage localized self-reliance.

By bypassing standard corporate learning dashboards and requiring you to configure local Markdown files and local Git networks running directly on your own machine hardware, you are actively practicing an act of **technological ascesis**. This course treats your terminal and local workspace as a *convivial tool* designed to preserve your digital sovereignty.

---

## 📅 The 14-Week Core Architecture

Your coursework tracking is divided into two distinct open-portfolio phases, shifting away from corporate infrastructure at the exact midpoint of the semester:

1. **Phase 1 (Weeks 1-7):** Operating pseudonymously within the GitHub sandbox.
2. **Phase 2 (Weeks 8-14):** Executing a structural migration to Codeberg—a member-owned, privacy-first European non-profit Git forge.

For detailed timeline instructions and the philosophical meaning behind this infrastructure shift, please read the official [Migration & Maintenance Notice](docs/MAINTENANCE-NOTICE.md).

---

## 🛠️ Operational Core: Using the Version Control System

To complete assignments, you will fork this master repository using a pseudonymous account, complete weekly analytical labs locally on your hard drive, and submit your work using Git Pull Requests.

### Track A: The Graphical Interface (GitHub Desktop)
1. **Fork the Repo:** Click the **Fork** button at the top right of this web page to create a copy on your account.
2. **Clone Locally:** Open GitHub Desktop, select **Clone a Repository**, and choose your forked version to download it to your machine.
3. **Commit & Push:** Save your written lab answers into the appropriate weekly directory. Open GitHub Desktop, write a short summary note in the summary box, click **Commit to main**, and click **Push origin** to upload your work online.

### Track B: The Command-Line Terminal
```bash
# 1. Clone your personal fork down to your computer
git clone [https://github.com/YourPseudonymousHandle/impacts-of-computing.git](https://github.com/YourPseudonymousHandle/impacts-of-computing.git)

# 2. Navigate inside the course folder
cd impacts-of-computing

# 3. Stage changes, commit with a message, and push to your account fork
git add .
git commit -m "lab: complete module 01 logs"
git push origin main
```

## 🔄 Keeping Your Course Files Up to Date (Syncing the Upstream)

As the semester progresses, new modules and lab files will be added to the instructor's master repository. Because your workspace is an isolated fork, you must manually pull these updates from the **Upstream** master.

### Using the GitHub Browser Interface (Zero-Installation Sync)

1. Navigate directly to your personal fork page on the GitHub website.
2. Look at the status bar right above your project files. If you are behind, you will see a message indicating it.
3. Click the **Sync fork** dropdown button on the right side of that bar.
4. Click the green **Update branch** button. Your online fork is now completely up to date.
5. *Operational Note:* To run new interactive HTML labs locally, go to the updated file on your web browser, click **Download raw file** to save it to your local machine, and launch it in your browser.

### Using the Command-Line Terminal

```
Bash

# Link the master source once during Week 1
git remote add upstream [https://github.com/YourInstructorHandle/impacts-of-computing.git](https://github.com/YourInstructorHandle/impacts-of-computing.git)

# Weekly synchronization pipeline:
git fetch upstream
git merge upstream/main
git push origin main
```

### 🚨 Break Glass Protocol: Handling "Merge Conflicts"

If you accidentally edited an existing assignment file that the instructor later updated, Git may flag a conflict. Run this sequence to safely wipe the local conflict and accept the instructor's official template:

```
Bash

git merge --abort
git checkout upstream/main -- path/to/conflicting-file.md
git add .
git commit -m "sys: sync upstream and clear local file conflict"
git push origin main
```

## 📝 License

This course curriculum and its interactive laboratories are licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/). You are free to share, copy, and remix these materials, provided you give appropriate attribution, do not use them for commercial gain, and share any adaptations under these exact same copyleft terms.