# Designing and Managing IT Systems - Obsidian Notes

This repository contains comprehensive notes for the course **Designing and Managing IT Systems**, written in Obsidian format with atomic note-taking principles.

The notes are organised into interconnected atomic concepts that build upon each other, making it easy to understand complex relationships between different topics.

## Table of Contents

- [Getting Started](#getting-started)
- [Setup Instructions](#setup-instructions)
    - [macOS](#macos)
    - [Windows](#windows)
    - [Linux](#linux)
- [Keeping Your Vault Updated](#keeping-your-vault-updated)
- [Adding Your Own Notes](#adding-your-own-notes)
- [Repository Structure](#repository-structure)
- [Contributing](#contributing)

## Getting Started

You have two main options for using these notes:

1. **Simple Download**: Download and use the notes as-is (no updates)
2. **Fork & Sync**: Create your own fork to add personal notes while receiving updates

**We recommend Option 2** if you plan to add your own notes and want to keep receiving updates to the course material.

## Setup Instructions

### Prerequisites

1. Install [Obsidian](https://obsidian.md/) (free)
2. Install [Git](https://git-scm.com/) (if you want to sync updates)

### macOS

#### Option 1: Simple Download (No Updates)

1. Click the green **Code** button on GitHub → **Download ZIP**
2. Extract the ZIP file to your desired location
3. Open Obsidian
4. Click **Open folder as vault**
5. Select the extracted folder

#### Option 2: Fork & Sync (Recommended)

1. **Fork this repository** (click Fork button on GitHub)

2. **Clone your fork locally:**
   ```bash
   # Replace YOUR_USERNAME with your GitHub username
   git clone https://github.com/YOUR_USERNAME/designing-managing-it-systems-notes.git
   cd designing-managing-it-systems-notes
   ```

3. **Add the original repository as upstream:**
   ```bash
   git remote add upstream https://github.com/ORIGINAL_USERNAME/designing-managing-it-systems-notes.git
   ```

4. **Open in Obsidian:**
   - Open Obsidian
   - Click **Open folder as vault**
   - Select the cloned folder

### Windows

#### Option 1: Simple Download (No Updates)

1. Click the green **Code** button on GitHub → **Download ZIP**
2. Extract the ZIP file using Windows Explorer or 7-Zip
3. Open Obsidian
4. Click **Open folder as vault**
5. Select the extracted folder

#### Option 2: Fork & Sync (Recommended)

1. **Fork this repository** (click Fork button on GitHub)

2. **Clone your fork locally:**
   ```cmd
   # Open Command Prompt or PowerShell
   # Replace YOUR_USERNAME with your GitHub username
   git clone https://github.com/YOUR_USERNAME/designing-managing-it-systems-notes.git
   cd designing-managing-it-systems-notes
   ```

3. **Add the original repository as upstream:**
   ```cmd
   git remote add upstream https://github.com/ORIGINAL_USERNAME/designing-managing-it-systems-notes.git
   ```

4. **Open in Obsidian:**
   - Open Obsidian
   - Click **Open folder as vault**
   - Select the cloned folder

### Linux

#### Option 1: Simple Download (No Updates)

1. Click the green **Code** button on GitHub → **Download ZIP**
2. Extract the ZIP file:
   ```bash
   unzip designing-managing-it-systems-notes-main.zip
   ```
3. Open Obsidian
4. Click **Open folder as vault**
5. Select the extracted folder

#### Option 2: Fork & Sync (Recommended)

1. **Fork this repository** (click Fork button on GitHub)

2. **Clone your fork locally:**
   ```bash
   # Replace YOUR_USERNAME with your GitHub username
   git clone https://github.com/YOUR_USERNAME/designing-managing-it-systems-notes.git
   cd designing-managing-it-systems-notes
   ```

3. **Add the original repository as upstream:**
   ```bash
   git remote add upstream https://github.com/ORIGINAL_USERNAME/designing-managing-it-systems-notes.git
   ```

4. **Open in Obsidian:**
   - Open Obsidian (install via package manager or download from website)
   - Click **Open folder as vault**
   - Select the cloned folder

## Keeping Your Vault Updated

If you used the **Fork & Sync** method, you can regularly pull updates from the original repository while keeping your personal notes.

### Step 1: Commit Your Personal Changes

Before updating, always commit your personal notes:

```bash
# Add your changes
git add .
git commit -m "Add my personal notes"
git push origin main
```

### Step 2: Fetch and Merge Updates

```bash
# Fetch latest changes from the original repository
git fetch upstream

# Merge the updates into your fork
git merge upstream/main

# Push the updates to your fork
git push origin main
```

### Handling Merge Conflicts

If you've modified the same files that were updated in the original repository, you may encounter merge conflicts:

1. Git will mark conflicted files
2. Open the files in Obsidian or a text editor
3. Look for conflict markers (`<<<<<<`, `======`, `>>>>>>`)
4. Choose which version to keep or combine both
5. Remove the conflict markers
6. Commit the resolved conflicts:
   ```bash
   git add .
   git commit -m "Resolve merge conflicts"
   git push origin main
   ```

## Adding Your Own Notes

### Recommended Organization

To avoid conflicts with future updates, organize your personal notes like this:

```
📁 Your Vault/
├── 📁 Atomic/          # Original course notes (try not to modify)
├── 📁 Figures/         # Original figures (try not to modify)  
├── 📁 Lectures/        # Original lecture notes (try not to modify)
├── 📁 Personal/        # 👈 Your personal notes go here
│   ├── My Questions.md
│   ├── Study Plan.md
│   └── Extra Research.md
├── 📁 Projects/        # 👈 Your project work
│   ├── Assignment 1.md
│   └── Group Project.md
└── 📄 README.md
```

### Linking to Original Notes

You can link from your personal notes to the atomic notes:

```markdown
# My Understanding of Risk Management

I found the [[Risk]] concept particularly interesting because...

My additional thoughts on [[Project Risks]]:
- Personal experience from internship...
- Question: How does this apply to agile projects?

See also: [[My Questions]] about risk assessment.
```

### Best Practices

- **Create new folders** for your content instead of modifying existing ones
- **Link liberally** to connect your notes with the original atomic notes
- **Use descriptive filenames** that won't conflict with course material
- **Regular commits** help track your learning progress

## Repository Structure

```
📁 Repository/
├── 📁 Atomic/          # Atomic notes (single concepts)
│   ├── Risk.md
│   ├── Use Case.md
│   └── ...
├── 📁 Figures/         # Diagrams and images
│   ├── Risk Types.png
│   └── ...
├── 📁 Lectures/        # Lecture-based notes
│   ├── Week 1.md
│   └── ...
└── 📄 README.md        # This file
```

## Contributing

Found an error or want to improve the original notes? Contributions are welcome!

1. Fork this repository
2. Create a feature branch: `git checkout -b fix-typo-in-risk-notes`
3. Make your changes
4. Commit: `git commit -m "Fix typo in Risk.md"`
5. Push: `git push origin fix-typo-in-risk-notes`
6. Create a Pull Request

## Tips for Success

- **Start with the Graph View** in Obsidian to see how concepts connect
- **Use the search function** to find related concepts quickly
- **Enable backlinks** to see which notes reference your current note
- **Install community plugins** like Calendar and Templater for better organization
- **Set up daily notes** to track your learning progress

## Troubleshooting

### Images Not Displaying

If images aren't showing in Obsidian:
1. Go to Settings → Files & Links
2. Enable "Automatically update internal links"
3. Check that image files are in the `Figures/` folder

### Git Issues

If you encounter git issues:
- Make sure you're in the correct directory
- Check your remotes: `git remote -v`
- Verify your branch: `git branch -a`

### Merge Conflicts

If updates cause conflicts:
- Don't panic! Your notes are safe
- Follow the merge conflict resolution steps above
- When in doubt, create a backup of your personal notes first

---

**Happy studying!**

Feel free to explore, learn, and make these notes your own. The atomic structure is designed to help you build a deep, interconnected understanding of IT systems design and management.
