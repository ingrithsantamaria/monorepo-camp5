# monorepo-camp5
# 🚀 Automated Testing Monorepo

This repository is a monorepo containing automated tests implemented with:
- **Cypress** for E2E testing
- **Cucumber (BDD)** for natural language specifications
- **Page Object Model (POM)** design pattern
- **Lighthouse** for performance and accessibility audits

## 📁 Project Structure
monorepo-camp5/
├── .github/
│ └── workflows/ # GitHub Actions configuration
├── packages/
│ ├── cypress-bdd/ # E2E tests with Cypress + Cucumber
│ └── lighthouse/ # Performance audits
├── .gitignore
└── README.md


## 🛠 Technologies Used

| Technology | Version | Purpose |
|------------|---------|---------|
| Cypress | ^12.0+ | E2E Testing |
| @badeball/cypress-cucumber-preprocessor | ^15.0+ | BDD Integration |
| Lighthouse | ^10.0+ | Web Audits |
| Node.js | 18.x+ | Runtime Environment |

## 🏁 Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/ingrithsantamaria/monorepo-camp5.git
   cd monorepo-camp5

2. Install dependencies:
    npm install

3. Install package-specific dependencies:
    cd packages/cypress-bdd && npm install
    cd ../lighthouse && npm install

▶️ Running Tests
Cypress Tests (BDD + POM)

# Run in headless mode
npm run test --workspace=cypress-bdd

# Open interactive runner
npm run cy:open --workspace=cypress-bdd

Lighthouse Audits
npm run audit --workspace=lighthouse

📊 Reports
Cypress: HTML reports in cypress/reports/

Lighthouse: HTML reports in lighthouse/audits/
🔄 CI/CD Pipeline
GitHub Actions workflow triggers on:

Pushes to main

Pull requests to main

See configuration: .github/workflows/ci.yml

📝 Implemented Patterns
Page Object Model (POM)

Classes organized in packages/cypress-bdd/pages/

Example: LoginPage.js

Behavior Driven Development (BDD)

Gherkin feature files: *.feature

Associated step definitions