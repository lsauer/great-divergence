# The Great Intelligence Divergence - CI/CD & Tooling

This project uses a automated CI/CD pipeline and various linting tools to ensure high-quality code and accessibility.

## Tooling Stack

- **Linter**: [HTMLHint](https://htmlhint.com/) for HTML structure and best practices.
- **Formatter**: [Prettier](https://prettier.io/) for consistent code styling.
- **Accessibility**: [Pa11y](https://pa11y.org/) for automated WCAG 2.1 compliance checks.
- **Deployment**: [Netlify CLI](https://www.netlify.com/) for automated and manual deployments.

## Local Development

Install dependencies:
```bash
npm install
```

### Automation Scripts
- `npm run lint`: Lint the HTML file.
- `npm run format`: Format the code using Prettier.
- `npm run format:check`: Check if code follows formatting rules.
- `npm run a11y`: Run accessibility checks.
- `npm run deploy`: Deploy the site to Netlify (Production).

## CI/CD Pipeline

The project uses GitHub Actions (see `.github/workflows/ci.yml`) to automatically:
1. Run linting and formatting checks on every Pull Request and Push to `main`.
2. Run accessibility audits.
3. Deploy to Netlify production environment when changes are pushed to `main`.

### Requirements for Automated Deployment
To enable automated deployment via GitHub Actions, the following secrets must be set in your GitHub repository:
- `NETLIFY_AUTH_TOKEN`: Your Netlify personal access token.
- `NETLIFY_SITE_ID`: Your Netlify Site ID.
