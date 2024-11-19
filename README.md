
# Portfolio-Remo

This repository contains a modern web portfolio built with **Vue 3** and **Vite**, designed for fast and efficient development.

## Features

- Modern web technologies (Vue 3, Vite)
- TailwindCSS integration for responsive and sleek designs
- Hot-reload development server for quick iterations
- Optimized production build

---

## Prerequisites

Ensure you have the following installed on your system:

- **Node.js**: Latest stable version. Install via [Node.js official site](https://nodejs.org/).
- **npm**: Comes with Node.js. Confirm installation with:

  ```sh
  npm -v
  ```

- **Git**: Clone the repository using Git. Install via [Git official site](https://git-scm.com/).

- **Ubuntu Essentials**: Update your system with the latest packages.

  ```sh
  sudo apt update && sudo apt upgrade -y
  ```

---

## Installation Guide

### Step 1: Clone the Repository

Clone this repository to your local machine:

```sh
git clone https://github.com/yourusername/Portfolio-Remo.git
```

Replace `yourusername` with the appropriate GitHub username.

### Step 2: Navigate to the Project Directory

Move into the project directory:

```sh
cd Portfolio-Remo
```

### Step 3: Install Dependencies

Install the required dependencies using npm:

```sh
npm install
```

### Step 4: Start the Development Server

Run the development server to preview your portfolio:

```sh
npm run dev
```

Access the application at the address provided (e.g., `http://localhost:5173`).

---

## Commands Reference

### Compile and Minify for Production

Build the application for deployment:

```sh
npm run build
```

---

## Updating Node.js and npm (Ubuntu)

To ensure compatibility, update to the latest versions of Node.js and npm:

1. Install or update Node.js using NodeSource:

   ```sh
   curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
   sudo apt install -y nodejs
   ```

   Replace `18.x` with the latest version as needed.

2. Verify installation:

   ```sh
   node -v
   npm -v
   ```

---

## Recommended IDE Setup

- **[VSCode](https://code.visualstudio.com/)**: Lightweight and feature-rich IDE.
- **[Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar)**: Vue 3 support for VSCode (disable Vetur for best results).

---

## Customize Configuration

Refer to the [Vite Configuration Reference](https://vite.dev/config/) for advanced setup options.

---

## Contributing

Feel free to submit issues or pull requests. Contributions are welcome!

---

## License

This project is open-source and available under the [MIT License](LICENSE).
