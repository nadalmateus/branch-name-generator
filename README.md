# Azure DevOps → Branch Name Generator

A simple, lightweight, and privacy-friendly tool that automatically converts **Azure DevOps work item titles** into standardized **Git branch names**.

No backend. No database. No installation. No external services.

Everything runs directly in your browser.

## ✨ Features

- Automatically converts Azure DevOps work item titles into Git branch names
- Generates branches **in real time** while typing
- Supports multiple work items, one per line
- Supports multiple Azure DevOps work item types
- Automatically converts descriptions to **kebab-case**
- Removes accents and special characters
- Removes duplicate hyphens
- Copy individual branch names
- Copy all generated branches at once
- Configurable prefix for bugs
- Responsive interface
- Built with plain **HTML, CSS, and JavaScript**
- No backend or database required
- Runs entirely locally in the browser

## 🚀 How It Works

Enter Azure DevOps work item titles using the following format:

```text
<Type> <ID>: <Description>
```

For example:

```text
User Story 1234: Implement user authentication
Bug 5678: Fix invalid password validation
Task 9012: Update project documentation
Feature 3456: Add dark mode support
```

The application automatically extracts the **work item type**, **ID**, and **description**, then generates the corresponding Git branch name.

### Default Convention

```text
feature/<ticket-id>-<description>
fix/<ticket-id>-<description>
chore/<ticket-id>-<description>
hotfix/<ticket-id>-<description>
```

For example:

```text
User Story 1234: Implement user authentication
```

becomes:

```text
feature/1234-implement-user-authentication
```

## 📋 Supported Work Item Types

| Work Item Type | Branch Prefix |
|---|---|
| Feature | `feature/` |
| User Story | `feature/` |
| Task | `chore/` |
| Bug | Configurable |

### Bug Prefix

Bugs can use one of the following prefixes:

```text
fix/
bug/
hotfix/
```

The selected prefix can be changed directly from the user interface and is applied immediately to all generated bug branches.

## 🔄 Real-Time Generation

Branch names are generated automatically whenever the input changes.

There is no need to click a button to update the results.

Multiple work items can be entered by placing each one on a separate line:

```text
User Story 1001: Create customer dashboard
Bug 1002: Fix dashboard loading error
Task 1003: Update dashboard documentation
Feature 1004: Add dashboard export
```

The application generates:

```text
feature/1001-create-customer-dashboard
fix/1002-fix-dashboard-loading-error
chore/1003-update-dashboard-documentation
feature/1004-add-dashboard-export
```

## 🧹 Name Normalization

Descriptions are automatically normalized into Git-friendly **kebab-case** names.

The normalization process:

1. Converts text to lowercase
2. Removes accents and diacritics
3. Replaces spaces with hyphens
4. Removes special characters
5. Removes duplicate hyphens
6. Removes leading and trailing hyphens

### Example

Input:

```text
User Story 1234: Implement autenticação de usuários!
```

Output:

```text
feature/1234-implement-autenticacao-de-usuarios
```

## 📋 Copy to Clipboard

Each generated branch includes its own **Copy** button.

The application also provides a **Copy All** option that copies every generated branch to the clipboard, with one branch per line.

Example:

```text
feature/1001-create-customer-dashboard
fix/1002-fix-dashboard-loading-error
chore/1003-update-dashboard-documentation
```

This makes it easy to copy the generated branches directly into your terminal, Git client, or documentation.

## ⌨️ Keyboard Shortcut

| Shortcut | Action |
|---|---|
| `Ctrl + Enter` | Generate branches |

Real-time generation remains enabled regardless of the keyboard shortcut.

The shortcut is provided as a convenient alternative when working with the input field.

## 🔒 Privacy

Privacy is one of the core principles of this application.

The application:

- Runs entirely in the user's browser
- Does not send ticket titles to a server
- Does not use a backend
- Does not require a database
- Does not require an API
- Does not require an Azure DevOps connection
- Does not send data to third-party services

Your Azure DevOps work item titles remain in your browser.

## 🛠️ Technology

The application intentionally uses a minimal technology stack:

- **HTML**
- **CSS**
- **JavaScript**

There is no framework or backend required.

The goal is to keep the application:

- Simple
- Fast
- Lightweight
- Portable
- Easy to maintain
- Easy to host

## 📦 Running Locally

Since the application is completely client-side, no installation or build process is required.

Simply clone the repository:

```bash
git clone <repository-url>
```

Navigate to the project directory:

```bash
cd <project-directory>
```

Then open the HTML file in your browser.

Alternatively, serve the project using any static web server.

For example, with Python:

```bash
python -m http.server
```

Then open the application in your browser.

## 🌐 Deployment

Because the application is entirely static, it can be hosted on virtually any static hosting provider.

Examples include:

- GitHub Pages
- Azure Static Web Apps
- Netlify
- Vercel
- Cloudflare Pages
- Any traditional web server

No server-side runtime is required.

## 🎯 Branch Naming Convention

The default branch naming convention is:

```text
feature/<ticket-id>-<description>
fix/<ticket-id>-<description>
chore/<ticket-id>-<description>
hotfix/<ticket-id>-<description>
```

This convention keeps branch names:

- Consistent
- Predictable
- Easy to read
- Easy to search
- Easy to associate with Azure DevOps work items

## 💡 Example

Given the following Azure DevOps work items:

```text
User Story 2501: Create customer management page
Bug 2502: Corrigir erro de validação de endereço
Task 2503: Update README documentation
Feature 2504: Add dark mode
```

The generated branches are:

```text
feature/2501-create-customer-management-page
fix/2502-corrigir-erro-de-validacao-de-endereco
chore/2503-update-readme-documentation
feature/2504-add-dark-mode
```

## ❤️ Why?

Creating Git branches from Azure DevOps work items is a small task, but doing it repeatedly can become tedious and inconsistent.

This tool automates that process while keeping the workflow:

**Simple → Fast → Consistent → Private**

---

Made with ❤️ to make **Azure DevOps → Git branch naming** faster and more consistent.
