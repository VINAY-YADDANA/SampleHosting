# SampleHosting

## Project Overview

SampleHosting is a lightweight web hosting platform designed to simplify the deployment and management of static websites. It provides an intuitive CLI for initializing projects, building assets, and publishing to a configurable hosting service.

## Features

- **Zero‑configuration deployment**: Deploy with a single command.
- **Local development server** with live reload.
- **Custom domain support**.
- **Extensible plugin system** for additional build steps.

## Prerequisites

- **Node.js** (>= 14.x) and **npm** (or **yarn**) installed.
- Git installed and configured for version control.

## Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-org/samplehosting.git
   cd samplehosting
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or using yarn
   yarn install
   ```

3. **Run the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```
   The site will be available at `http://localhost:3000` with hot‑reloading enabled.

4. **Build for production**
   ```bash
   npm run build
   # or
   yarn build
   ```
   The compiled assets will be placed in the `dist/` directory.

5. **Deploy**
   ```bash
   npm run deploy
   # or
   yarn deploy
   ```
   Follow the prompts to configure your hosting provider (e.g., Netlify, Vercel, or a custom S3 bucket).

## Usage Examples

### Initializing a New Project
```bash
npx samplehosting init my-awesome-site
cd my-awesome-site
npm install
npm run dev
```

### Adding a Custom Plugin
Create a plugin file `plugins/markdown-to-html.js`:
```js
module.exports = function markdownToHtml() {
  // plugin logic here
};
```
Then register it in `samplehosting.config.js`:
```js
module.exports = {
  plugins: [require('./plugins/markdown-to-html')]
};
```

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Make your changes and ensure all tests pass.
4. Submit a pull request with a clear description of your changes.

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.