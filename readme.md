# Internship Task 2 – Strict Tech Stack Implementation

## 📌 Project Overview
This project is a modern refactoring of a static HTML website. It transitions from using standalone HTML files to a professional workflow using a **Templating Engine (Nunjucks)** and a **Bundler (Vite)**.

The primary objective is to implement "Separation of Concerns"—keeping the website structure separate from the content—to make the code scalable and maintainable.

---
 ##Live Link :  https://nawabcaters.netlify.app/
## 🛠️ Mandatory Technology Stack

### 1. Templating Engine: **Nunjucks**
We selected Nunjucks over standard HTML and Handlebars for its advanced templating capabilities.

**Why do we separate Layouts (`layout.njk`) from Pages (`index.njk`)?**
* **Separation of Concerns:** We keep the "skeleton" of the site (Header, Navigation, Footer) in one file (`layout.njk`) and the unique content in separate files. This ensures that the design logic is distinct from the page data.
* **Eliminates Redundancy (DRY Principle):** In a normal HTML project, changing a menu item requires editing every single file. By separating the layout, we edit the header in one place, and it updates globally across all pages.
* **Maintainability:** Large websites are impossible to manage if every file contains the full HTML structure. Separating them makes the codebase cleaner and easier to read.

### 2. Bundler: **Vite**
We selected Vite as the build tool to handle asset management and local development.
* **Asset Optimization:** Vite automatically compresses and hashes images (e.g., `logo.hash123.png`) during the build process, ensuring users always see the newest version of an image.
* **Path Resolution:** It solves the common "broken link" issue in hosting by automatically calculating relative paths for scripts and styles during the build.

---

## 📂 Folder Structure

🚀 How to Install & Run
Follow these steps to set up the project on your machine.

Prerequisites
You must have Node.js installed.

1. Install Dependencies
Open your terminal (Command Prompt or VS Code Terminal) in the project folder and run:

Bash

npm install
This downloads the necessary tools (Vite and Nunjucks) into the node_modules folder.

2. Run in Development Mode
To view the website while you are working on it:

Bash

npm run dev
The terminal will show a link (usually http://localhost:5173).

Open that link in your browser. Changes you make to the code will appear instantly.

3. Build for Production
When you are ready to submit the task or host the website:

Bash

npm run build
This creates a dist/ folder.

Nunjucks templates are converted into standard HTML.

Images and CSS are optimized and linked correctly.


```text
my-internship-task/
├── dist/                  # The final "Product" (Generated only after running build)
├── node_modules/          # Libraries and dependencies
├── src/                   # The "Source" code (Where we work)
│   ├── assets/            # Images and CSS
│   ├── templates/         # 
│   │   └── layout.njk     # The MASTER template (Header/Footer)
│   ├── index.njk          # Home page content
│   ├── page2.njk          # Task Details content
│   └── page3.njk          # Contact content
├── package.json           # Project configuration
└── vite.config.js         # Settings to prevent broken links



