# React commands (for any React or Laravel + Inertia + React project)

I’ve grouped them clearly by purpose — so you can easily use them in your **lead generation engine** or any other React setup.

---

## ⚙️ 1. **React Project Setup**

| Purpose                                  | Command                                                | Notes                                    |
| ---------------------------------------- | ------------------------------------------------------ | ---------------------------------------- |
| Create a new React app (Vite)            | `npm create vite@latest my-app -- --template react`    | Recommended (modern build)               |
| Create React + TypeScript app            | `npm create vite@latest my-app -- --template react-ts` |                                          |
| (Alternative) Create React app (old CRA) | `npx create-react-app my-app`                          | Slower, not recommended for new projects |
| Move into folder                         | `cd my-app`                                            |                                          |
| Install dependencies                     | `npm install`                                          |                                          |
| Run local dev server                     | `npm run dev`                                          |                                          |
| Build for production                     | `npm run build`                                        |                                          |
| Preview production build                 | `npm run preview`                                      |                                          |
| Install packages                         | `npm install package-name`                             | Example: `npm install axios`             |
| Uninstall package                        | `npm uninstall package-name`                           |                                          |

---

## 🧩 2. **React with Laravel (Inertia Setup)**

| Purpose                            | Command                          | Notes                                |
| ---------------------------------- | -------------------------------- | ------------------------------------ |
| Install React + Inertia in Laravel | `npm install @inertiajs/react`   |                                      |
| Run Laravel Mix/Vite dev server    | `npm run dev`                    | (Runs alongside `php artisan serve`) |
| Build for production               | `npm run build`                  |                                      |
| Watch for changes                  | `npm run watch`                  |                                      |
| Rebuild dependencies               | `npm rebuild`                    | Use if node modules break            |
| Fix version mismatch               | `npm install --legacy-peer-deps` | Use if dependency errors occur       |

---

## 🧠 3. **React Component & File Commands (Manual)**

You create components manually, but here’s the convention:

| Purpose          | File Example                            | Description             |
| ---------------- | --------------------------------------- | ----------------------- |
| Create Component | `src/components/Form.tsx`               | Component file          |
| Create Page      | `src/pages/Contact.tsx`                 | Page used in routing    |
| Create Config    | `src/config/contact-form.config.tsx`    | Your form configuration |
| Import Component | `import Contact from './pages/Contact'` | Use in parent route     |

---

## 🧰 4. **Useful npm / Yarn Commands**

| Purpose              | npm Command                          | Yarn Equivalent           |
| -------------------- | ------------------------------------ | ------------------------- |
| Install dependencies | `npm install`                        | `yarn install`            |
| Add new package      | `npm install axios`                  | `yarn add axios`          |
| Add dev dependency   | `npm install -D tailwindcss`         | `yarn add -D tailwindcss` |
| Run project          | `npm run dev`                        | `yarn dev`                |
| Build project        | `npm run build`                      | `yarn build`              |
| Update all packages  | `npm update`                         | `yarn upgrade`            |
| Remove node_modules  | `rm -rf node_modules`                | same                      |
| Reinstall all        | `rm -rf node_modules && npm install` | same                      |

---

## 💅 5. **Tailwind CSS Commands (if used)**

| Purpose                    | Command                                           | Notes                          |
| -------------------------- | ------------------------------------------------- | ------------------------------ |
| Install Tailwind CSS       | `npm install -D tailwindcss postcss autoprefixer` |                                |
| Initialize Tailwind config | `npx tailwindcss init -p`                         | Generates `tailwind.config.js` |
| Run dev (watch mode)       | `npm run dev`                                     |                                |
| Build CSS                  | `npm run build`                                   | Compiles production CSS        |

---

## 🧪 6. **React Developer Tools**

| Purpose                    | Command                    | Notes                                          |
| -------------------------- | -------------------------- | ---------------------------------------------- |
| Start Dev Tools in browser | *(no command)*             | Install React Developer Tools Chrome Extension |
| Check versions             | `npm list react react-dom` | See installed versions                         |

---

## 🧱 7. **TypeScript (if used)**

| Purpose              | Command                     | Notes |
| -------------------- | --------------------------- | ----- |
| Install TypeScript   | `npm install -D typescript` |       |
| Create tsconfig.json | `npx tsc --init`            |       |
| Type check           | `npx tsc --noEmit`          |       |

---

## 🧑‍💻 8. **React Common Libraries (install commands)**

| Purpose             | Package                   | Install Command                |
| ------------------- | ------------------------- | ------------------------------ |
| HTTP requests       | Axios                     | `npm install axios`            |
| Routing             | React Router DOM          | `npm install react-router-dom` |
| Form validation     | React Hook Form           | `npm install react-hook-form`  |
| Icons               | Lucide React              | `npm install lucide-react`     |
| Animations          | Framer Motion             | `npm install framer-motion`    |
| UI Components       | Shadcn UI                 | `npx shadcn-ui@latest init`    |
| Toast Notifications | React Hot Toast           | `npm install react-hot-toast`  |
| State management    | Zustand                   | `npm install zustand`          |
| Dark mode toggle    | `npm install next-themes` | For theme management           |

---

## ⚙️ 9. **Debugging / Maintenance**

| Purpose                 | Command                                                |
| ----------------------- | ------------------------------------------------------ |
| Check outdated packages | `npm outdated`                                         |
| Fix vulnerabilities     | `npm audit fix`                                        |
| Reinstall all clean     | `rm -rf node_modules package-lock.json && npm install` |
| Delete cache            | `npm cache clean --force`                              |

---

## 🚀 10. **Run Full Laravel + React App**

```bash
# 1️⃣ Start backend
php artisan serve

# 2️⃣ Start frontend
npm run dev
```

→ Now open [http://localhost:8000](http://localhost:8000)
Laravel serves your React pages through Inertia.

---

Would you like me to add **the exact React folder structure + file tree** for your Lead Generation Form setup (with `/config`, `/pages`, `/components`, and `/api` integration)?
That will give you a ready-to-run structure for both **React + Laravel** sides.
