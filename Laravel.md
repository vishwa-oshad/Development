Perfect ✅ — let’s go step by step!

Here’s **every Laravel command** you need — from installation to daily development, debugging, database, and deployment — **fully explained and grouped** for you.

---

## 🧱 1. **Project Setup**

| Purpose                          | Command                                                | Notes                                                        |
| -------------------------------- | ------------------------------------------------------ | ------------------------------------------------------------ |
| Create new Laravel project       | `composer create-project laravel/laravel project_name` | Installs latest Laravel version                              |
| Run local development server     | `php artisan serve`                                    | Default URL → [http://127.0.0.1:8000](http://127.0.0.1:8000) |
| Check Laravel version            | `php artisan --version`                                |                                                              |
| Clear Laravel cache (use often!) | `php artisan optimize:clear`                           | Clears view, route, config, and cache                        |
| Rebuild cache                    | `php artisan optimize`                                 | Speeds up performance                                        |

---

## 🧩 2. **Environment Setup**

| Purpose                | Command                    | Notes                               |
| ---------------------- | -------------------------- | ----------------------------------- |
| Generate app key       | `php artisan key:generate` | Sets APP_KEY in `.env`              |
| Link storage to public | `php artisan storage:link` | Makes `/storage` accessible via URL |
| Cache config           | `php artisan config:cache` | Improves config loading             |
| Clear config cache     | `php artisan config:clear` | Use when `.env` changes             |
| Clear route cache      | `php artisan route:clear`  |                                     |
| Clear view cache       | `php artisan view:clear`   |                                     |

---

## 🗄️ 3. **Database & Migrations**

| Purpose                                   | Command                                              | Notes                         |
| ----------------------------------------- | ---------------------------------------------------- | ----------------------------- |
| Run all migrations                        | `php artisan migrate`                                | Creates database tables       |
| Rollback last migration                   | `php artisan migrate:rollback`                       | Undo last batch               |
| Reset all migrations                      | `php artisan migrate:reset`                          | Undo everything               |
| Refresh (rollback + migrate)              | `php artisan migrate:refresh`                        | Useful for development        |
| Fresh migrate (drop all tables + migrate) | `php artisan migrate:fresh`                          |                               |
| Run seeders                               | `php artisan db:seed`                                | Runs `DatabaseSeeder`         |
| Migrate + Seed                            | `php artisan migrate --seed`                         |                               |
| Create a migration file                   | `php artisan make:migration create_table_name_table` | Example: `create_users_table` |

---

## 🧠 4. **Models, Controllers, Views**

| Purpose                                 | Command                                                 | Notes                                        |
| --------------------------------------- | ------------------------------------------------------- | -------------------------------------------- |
| Create a model                          | `php artisan make:model ModelName`                      | Example: `make:model Contact`                |
| Create model with migration             | `php artisan make:model ModelName -m`                   |                                              |
| Create controller                       | `php artisan make:controller ControllerName`            | Example: `make:controller ContactController` |
| Create controller with resource methods | `php artisan make:controller ControllerName --resource` |                                              |
| Create view (manually)                  | `resources/views/...`                                   | Blade file: `contact.blade.php`              |
| Create middleware                       | `php artisan make:middleware MiddlewareName`            |                                              |

---

## ⚙️ 5. **Routing & API**

| Purpose                        | Command                                                   | Notes |
| ------------------------------ | --------------------------------------------------------- | ----- |
| List all routes                | `php artisan route:list`                                  |       |
| Create API resource controller | `php artisan make:controller Api/ContactController --api` |       |
| Define routes in file          | `/routes/web.php` or `/routes/api.php`                    |       |

---

## 🧰 6. **Requests, Resources, Factories**

| Purpose                   | Command                                                   | Notes                 |
| ------------------------- | --------------------------------------------------------- | --------------------- |
| Create a Form Request     | `php artisan make:request StoreContactRequest`            | Validates form data   |
| Create Resource (for API) | `php artisan make:resource ContactResource`               | Converts model → JSON |
| Create Factory            | `php artisan make:factory ContactFactory --model=Contact` | For testing/seeding   |
| Create Seeder             | `php artisan make:seeder ContactSeeder`                   | For fake data         |

---

## 👨‍💻 7. **Authentication (Breeze, Jetstream, etc.)**

| Purpose                              | Command                                  | Notes |
| ------------------------------------ | ---------------------------------------- | ----- |
| Install Breeze (simple auth)         | `composer require laravel/breeze --dev`  |       |
| Scaffold Breeze with Inertia + React | `php artisan breeze:install react`       |       |
| Scaffold Breeze with Blade           | `php artisan breeze:install blade`       |       |
| Install Jetstream (advanced)         | `composer require laravel/jetstream`     |       |
| Jetstream + Inertia                  | `php artisan jetstream:install inertia`  |       |
| Jetstream + Livewire                 | `php artisan jetstream:install livewire` |       |
| Migrate after installing             | `php artisan migrate`                    |       |

---

## 🧮 8. **Queue, Jobs, Events, Listeners**

| Purpose           | Command                                             | Notes |
| ----------------- | --------------------------------------------------- | ----- |
| Create Job        | `php artisan make:job SendEmailJob`                 |       |
| Create Event      | `php artisan make:event ContactSubmitted`           |       |
| Create Listener   | `php artisan make:listener SendContactNotification` |       |
| Run queue worker  | `php artisan queue:work`                            |       |
| Stop queue worker | `php artisan queue:restart`                         |       |

---

## 🔒 9. **Testing**

| Purpose     | Command                                 | Notes                   |
| ----------- | --------------------------------------- | ----------------------- |
| Create test | `php artisan make:test ContactFormTest` |                         |
| Run tests   | `php artisan test`                      | Or `vendor/bin/phpunit` |

---

## 🌍 10. **Deployment & Optimization**

| Purpose                 | Command                      | Notes                      |
| ----------------------- | ---------------------------- | -------------------------- |
| Optimize for production | `php artisan optimize`       | Cache routes, config, etc. |
| Cache routes            | `php artisan route:cache`    |                            |
| Cache views             | `php artisan view:cache`     |                            |
| Clear everything        | `php artisan optimize:clear` |                            |

---

## 🧱 11. **Common Composer Commands**

| Purpose              | Command                           |
| -------------------- | --------------------------------- |
| Install dependencies | `composer install`                |
| Update dependencies  | `composer update`                 |
| Require package      | `composer require vendor/package` |
| Remove package       | `composer remove vendor/package`  |
| Dump autoload        | `composer dump-autoload`          |

---

## 💡 12. **Frontend (if using Laravel Mix or Vite)**

| Purpose              | Command         |
| -------------------- | --------------- |
| Install npm packages | `npm install`   |
| Run dev server       | `npm run dev`   |
| Build for production | `npm run build` |
| Watch for changes    | `npm run watch` |

---

## 🧩 13. **Laravel + Inertia (React/Vue)**

| Purpose                   | Command                                                           |
| ------------------------- | ----------------------------------------------------------------- |
| Install Inertia           | `composer require inertiajs/inertia-laravel`                      |
| Install React Adapter     | `npm install @inertiajs/react`                                    |
| Create Inertia middleware | `php artisan inertia:middleware`                                  |
| Publish config            | `php artisan vendor:publish --provider="Inertia\ServiceProvider"` |

---

Would you like me to show **the commands + code** for your specific **Contact Form API** (controller, route, request validation, and mail notification)?
That will complete the full Laravel + React form flow.
