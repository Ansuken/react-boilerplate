# React + TypeScript + Vite Boilerplate

This boilerplate is designed to help you start new React projects quickly with Vite, TypeScript, and a ready-to-use ESLint configuration.

## 🚀 **What's included in this boilerplate?**
- **React + Vite** setup with Hot Module Replacement (HMR).
- **TypeScript** as the base language.
- **ESLint** with recommended rules, including React support and advanced typing options.
- **Base project structure** to get started quickly (folders like `common/styleVars`, `common/styles`, etc.).
- **A basic `_reset.css` is included.**

---

## 📦 **Project structure**

```bash
.
├── src
│   ├── common/          # Reusable components
│       ├── styleVars    # CSS Var files 
│       ├── styles       # Some styles for forms, components...
│   ├── utils/           # Utility functions
│   ├── App.tsx          # Main component
│   ├── _reset.css       # CSS Reset file
│   └── main.tsx         # Entry point
├── eslint.config.js     # ESLint configuration
├── tsconfig.json        # TypeScript configuration
└── vite.config.ts       # Vite configuration
```

---

## 📖 **How to start a new project using this boilerplate**

### **Option 1: Use `degit` to clone the boilerplate**
1. Install `degit` globally if you haven't:
   ```bash
   npm install -g degit
   ```

2. Open a terminal and run:
   ```bash
   npx degit https://github.com/Ansuken/react-boilerplate.git project-name
   cd project-name
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

Your project will be running at `http://localhost:5173`.

---

### **Option 2: Manually clone the repository**
1. Clone the project:
   ```bash
   git clone https://github.com/Ansuken/react-boilerplate.git project-name
   cd project-name
   ```

2. Remove the Git history if you don’t need it:
   ```bash
   rm -rf .git
   git init
   git remote add origin [new-repository-url.git]
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

4. Start the project:
   ```bash
   npm run dev
   ```

---

## 🔧 **Expanding the ESLint configuration**

If you’re developing a production-ready application, we recommend enabling stricter lint rules with type checking.

### 1. Configure `parserOptions`:
```js
export default tseslint.config({
  languageOptions: {
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})
```

### 2. Replace the recommended config:
Replace `tseslint.configs.recommended` with:
- `tseslint.configs.recommendedTypeChecked`
- `tseslint.configs.strictTypeChecked`
- Optionally: `...tseslint.configs.stylisticTypeChecked`

### 3. Add the React plugin:
```js
import react from 'eslint-plugin-react'

export default tseslint.config({
  settings: { react: { version: '18.3' } },
  plugins: {
    react,
  },
  rules: {
    ...react.configs.recommended.rules,
    ...react.configs['jsx-runtime'].rules,
  },
})
```

---

## 📚 **Available scripts**

- `npm run dev` - Start the development server.
- `npm run build` - Build the application for production.
- `npm run preview` - Preview the production build.
- `npm run lint` - Run ESLint to detect issues.

---

## ✨ **Recommended customizations**
You can further customize this boilerplate by:
- Setting up routes using `react-router-dom`.
- Adding additional global styles or CSS libraries (e.g., Tailwind or Sass).
- Creating custom hooks inside the `hooks/` folder.

---

## 🛠️ **Tools used**
- **[Vite](https://vitejs.dev/)**
- **[React](https://reactjs.org/)**
- **[TypeScript](https://www.typescriptlang.org/)**
- **[ESLint](https://eslint.org/)**

---

## 🌟 **Contributions**
If you have suggestions to improve this boilerplate, feel free to open an issue or submit a pull request.

---

## 📝 **License**
This project is licensed under the [MIT License](./LICENSE).
