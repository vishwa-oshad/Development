
# Laravel

Here’s **every Laravel command** you need — from installation to daily development, debugging, database, and deployment.

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
# Laravel Backend File Creation Commands

Here's a comprehensive guide to all Laravel Artisan commands for creating backend files:

## 🎮 Controllers

```bash
# Basic controller
php artisan make:controller UserController

# Resource controller (with CRUD methods)
php artisan make:controller UserController --resource

# API resource controller (without create/edit views)
php artisan make:controller API/UserController --api

# Controller with model
php artisan make:controller UserController --model=User

# Invokable controller (single action)
php artisan make:controller ShowUserController --invokable
```

## 📊 Models

```bash
# Basic model
php artisan make:model User

# Model with migration
php artisan make:model User -m

# Model with migration, factory, and seeder
php artisan make:model User -mfs

# Model with everything (migration, factory, seeder, controller, policy)
php artisan make:model User --all
php artisan make:model User -a

# Model with resource controller
php artisan make:model User -c --resource

# Model with API controller
php artisan make:model User -c --api
```

## 🗃️ Migrations

```bash
# Create migration
php artisan make:migration create_users_table

# Create migration for existing table
php artisan make:migration add_phone_to_users_table

# Create pivot table migration
php artisan make:migration create_role_user_table

# Run migrations
php artisan migrate

# Rollback last migration
php artisan migrate:rollback

# Rollback all migrations
php artisan migrate:reset

# Rollback and re-run all migrations
php artisan migrate:refresh

# Rollback and re-run with seeding
php artisan migrate:refresh --seed

# Drop all tables and re-run migrations
php artisan migrate:fresh

# Drop all tables, re-run migrations and seed
php artisan migrate:fresh --seed
```

## 🌱 Seeders

```bash
# Create seeder
php artisan make:seeder UserSeeder

# Run all seeders
php artisan db:seed

# Run specific seeder
php artisan db:seed --class=UserSeeder
```

## 🏭 Factories

```bash
# Create factory
php artisan make:factory UserFactory

# Create factory for specific model
php artisan make:factory UserFactory --model=User
```

## 🔐 Middleware

```bash
# Create middleware
php artisan make:middleware CheckAge

# Create middleware in subdirectory
php artisan make:middleware Admin/CheckRole
```

## 📝 Requests (Form Requests)

```bash
# Create form request
php artisan make:request StoreUserRequest

# Create form request in subdirectory
php artisan make:request User/StoreUserRequest
```

## 📦 Resources (API Resources)

```bash
# Create resource
php artisan make:resource UserResource

# Create resource collection
php artisan make:resource UserCollection

# Create resource with collection
php artisan make:resource User --collection
```

## 🔧 Services/Repositories

```bash
# Laravel doesn't have built-in commands, but you can create manually:

# Create service directory structure
mkdir -p app/Services
touch app/Services/UserService.php

# Create repository directory structure
mkdir -p app/Repositories
touch app/Repositories/UserRepository.php
```

## 📮 Mail

```bash
# Create mailable class
php artisan make:mail WelcomeEmail

# Create mailable with markdown template
php artisan make:mail WelcomeEmail --markdown=emails.welcome
```

## 📢 Notifications

```bash
# Create notification
php artisan make:notification InvoicePaid

# Create notification with markdown
php artisan make:notification InvoicePaid --markdown=mail.invoice.paid
```

## 🎯 Events

```bash
# Create event
php artisan make:event UserRegistered

# Create event listener
php artisan make:listener SendWelcomeEmail

# Create listener for specific event
php artisan make:listener SendWelcomeEmail --event=UserRegistered
```

## 💼 Jobs

```bash
# Create job
php artisan make:job ProcessPodcast

# Create synchronous job
php artisan make:job ProcessPodcast --sync
```

## 🛡️ Policies

```bash
# Create policy
php artisan make:policy UserPolicy

# Create policy for model
php artisan make:policy UserPolicy --model=User
```

## ✅ Rules (Validation Rules)

```bash
# Create validation rule
php artisan make:rule Uppercase

# Create implicit rule
php artisan make:rule Uppercase --implicit
```

## 🔔 Observers

```bash
# Create observer
php artisan make:observer UserObserver

# Create observer for model
php artisan make:observer UserObserver --model=User
```

## 🎨 Commands (Console Commands)

```bash
# Create Artisan command
php artisan make:command SendEmails

# Create command with custom name
php artisan make:command SendEmails --command=emails:send
```

## 🧪 Tests

```bash
# Create feature test
php artisan make:test UserTest

# Create unit test
php artisan make:test UserTest --unit

# Create pest test (if using Pest)
php artisan make:test UserTest --pest
```

## 🔐 Authentication Scaffolding

```bash
# Install Laravel Breeze (simple auth)
composer require laravel/breeze --dev
php artisan breeze:install
npm install && npm run dev
php artisan migrate

# Install Laravel Jetstream (advanced auth)
composer require laravel/jetstream
php artisan jetstream:install livewire
# or
php artisan jetstream:install inertia
npm install && npm run dev
php artisan migrate

# Install Laravel Sanctum (API authentication)
composer require laravel/sanctum
php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
php artisan migrate
```

## 📡 Broadcasting

```bash
# Create channel class
php artisan make:channel OrderChannel
```

## 🔄 Casts

```bash
# Create custom cast
php artisan make:cast Json

# Create inbound cast
php artisan make:cast Hash --inbound
```

## 🌐 Providers

```bash
# Create service provider
php artisan make:provider PaymentServiceProvider
```

## 🗂️ Complete Project Setup Commands

```bash
# Start a complete CRUD module
php artisan make:model Post -a
# This creates: Model, Migration, Factory, Seeder, Policy, Controller (resource), Form Requests

# Alternative complete setup
php artisan make:model Post -mcrs
# Model, Migration, Controller (resource), Seeder

# With API controller
php artisan make:model Post -a --api
```

## 🔍 Useful Helper Commands

```bash
# List all routes
php artisan route:list

# Clear cache
php artisan cache:clear
php artisan config:clear
php artisan view:clear
php artisan route:clear

# Create symbolic link for storage
php artisan storage:link

# Generate app key
php artisan key:generate

# Optimize application
php artisan optimize

# Clear optimization
php artisan optimize:clear

# Run queue worker
php artisan queue:work

# List all artisan commands
php artisan list

# Get help for specific command
php artisan help make:controller
```

## 📋 Common Workflow Example

```bash
# 1. Create model with everything
php artisan make:model Product -a

# 2. Create API resource
php artisan make:resource ProductResource

# 3. Create form requests
php artisan make:request StoreProductRequest
php artisan make:request UpdateProductRequest

# 4. Create service
mkdir -p app/Services
touch app/Services/ProductService.php

# 5. Run migration
php artisan migrate

# 6. Create observer (optional)
php artisan make:observer ProductObserver --model=Product

# 7. Create tests
php artisan make:test ProductTest
php artisan make:test ProductTest --unit
```

These commands will help you quickly scaffold your Laravel backend! Use the `-h` or `--help` flag with any command to see all available options.
Would you like me to show **the commands + code** for your specific **Contact Form API** (controller, route, request validation, and mail notification)?
That will complete the full Laravel + React form flow.
