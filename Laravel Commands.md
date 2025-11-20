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


# Complete Laravel Backend Project Setup Guide

Let me create a comprehensive step-by-step guide for setting up a complete Laravel backend project from scratch!

## 🚀 Initial Project Setup

```bash
# Install Laravel (choose one method)
composer create-project laravel/laravel my-project
# OR using Laravel installer
laravel new my-project

# Navigate to project
cd my-project

# Generate application key
php artisan key:generate

# Create symbolic link for storage
php artisan storage:link
```

## ⚙️ Environment Configuration

```bash
# Copy .env.example to .env (if not automatically created)
cp .env.example .env

# Configure your .env file
# Update these values:
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

## 📦 Install Essential Packages

```bash
# API Authentication (Sanctum)
composer require laravel/sanctum
php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"

# IDE Helper (for better autocomplete)
composer require --dev barryvdh/laravel-ide-helper

# Laravel Debugbar (for debugging)
composer require --dev barryvdh/laravel-debugbar

# Laravel Telescope (for monitoring)
composer require laravel/telescope --dev
php artisan telescope:install

# Spatie Permissions (role & permission management)
composer require spatie/laravel-permission
php artisan vendor:publish --provider="Spatie\Permission\PermissionServiceProvider"

# Laravel Excel (for import/export)
composer require maatwebsite/excel
```

## 🏗️ Create Complete CRUD Module Example (Blog System)

### 1. User Module
```bash
# User already exists, just add API resources
php artisan make:resource UserResource
php artisan make:resource UserCollection
php artisan make:request StoreUserRequest
php artisan make:request UpdateUserRequest
php artisan make:controller API/UserController --api
```

### 2. Post Module
```bash
# Create Post model with everything
php artisan make:model Post -a

# Additional files
php artisan make:resource PostResource
php artisan make:resource PostCollection
php artisan make:request StorePostRequest
php artisan make:request UpdatePostRequest
php artisan make:observer PostObserver --model=Post
php artisan make:policy PostPolicy --model=Post

# Create service
mkdir -p app/Services
touch app/Services/PostService.php

# Create repository
mkdir -p app/Repositories
touch app/Repositories/PostRepository.php
```

### 3. Category Module
```bash
php artisan make:model Category -mcrs
php artisan make:controller API/CategoryController --api
php artisan make:resource CategoryResource
php artisan make:request StoreCategoryRequest
php artisan make:request UpdateCategoryRequest
```

### 4. Comment Module
```bash
php artisan make:model Comment -mcrs
php artisan make:controller API/CommentController --api
php artisan make:resource CommentResource
php artisan make:request StoreCommentRequest
php artisan make:request UpdateCommentRequest
```

### 5. Tag Module
```bash
php artisan make:model Tag -mcrs
php artisan make:controller API/TagController --api
php artisan make:resource TagResource
```

### 6. Media/File Upload Module
```bash
php artisan make:model Media -mc
php artisan make:controller API/MediaController
php artisan make:request UploadMediaRequest
```

## 🔐 Authentication & Authorization

```bash
# Create authentication controllers
php artisan make:controller API/Auth/LoginController
php artisan make:controller API/Auth/RegisterController
php artisan make:controller API/Auth/LogoutController
php artisan make:controller API/Auth/ForgotPasswordController
php artisan make:controller API/Auth/ResetPasswordController

# Create authentication requests
php artisan make:request Auth/LoginRequest
php artisan make:request Auth/RegisterRequest
php artisan make:request Auth/ForgotPasswordRequest
php artisan make:request Auth/ResetPasswordRequest

# Create middleware
php artisan make:middleware CheckRole
php artisan make:middleware CheckPermission
php artisan make:middleware ApiTokenMiddleware
```

## 📧 Notifications & Events

```bash
# Email verification
php artisan make:notification VerifyEmailNotification
php artisan make:notification WelcomeEmailNotification

# Post related events
php artisan make:event PostCreated
php artisan make:event PostUpdated
php artisan make:event PostDeleted

# Listeners
php artisan make:listener SendPostCreatedNotification --event=PostCreated
php artisan make:listener SendPostUpdatedNotification --event=PostUpdated
php artisan make:listener UpdatePostCache --event=PostCreated

# Mail classes
php artisan make:mail WelcomeMail --markdown=emails.welcome
php artisan make:mail PostPublishedMail --markdown=emails.post-published
```

## 💼 Jobs & Queues

```bash
# Create jobs
php artisan make:job ProcessImageUpload
php artisan make:job SendBulkEmails
php artisan make:job GenerateReport
php artisan make:job ExportPosts
php artisan make:job ImportUsers

# Create job batches
php artisan queue:batches-table
php artisan migrate
```

## ✅ Validation Rules

```bash
# Custom validation rules
php artisan make:rule Uppercase
php artisan make:rule PhoneNumber
php artisan make:rule ValidSlug
php artisan make:rule UniqueEmail
```

## 🧪 Testing

```bash
# Feature tests
php artisan make:test API/Auth/LoginTest
php artisan make:test API/Auth/RegisterTest
php artisan make:test API/PostTest
php artisan make:test API/CategoryTest
php artisan make:test API/CommentTest

# Unit tests
php artisan make:test Services/PostServiceTest --unit
php artisan make:test Services/UserServiceTest --unit
php artisan make:test Repositories/PostRepositoryTest --unit
```

## 🗄️ Database Setup

```bash
# Create migrations for relationships
php artisan make:migration create_category_post_table
php artisan make:migration create_post_tag_table
php artisan make:migration add_columns_to_users_table

# Create seeders
php artisan make:seeder RoleSeeder
php artisan make:seeder PermissionSeeder
php artisan make:seeder AdminUserSeeder
php artisan make:seeder CategorySeeder
php artisan make:seeder PostSeeder
php artisan make:seeder TagSeeder

# Run migrations
php artisan migrate

# Seed database
php artisan db:seed
# OR seed specific seeder
php artisan db:seed --class=RoleSeeder
```

## 📋 Additional Utility Files

```bash
# Create helpers directory and file
mkdir -p app/Helpers
touch app/Helpers/helpers.php

# Create traits
mkdir -p app/Traits
touch app/Traits/HasUuid.php
touch app/Traits/Sluggable.php
touch app/Traits/Searchable.php

# Create enums (PHP 8.1+)
mkdir -p app/Enums
touch app/Enums/PostStatus.php
touch app/Enums/UserRole.php

# Create DTOs (Data Transfer Objects)
mkdir -p app/DataTransferObjects
touch app/DataTransferObjects/PostData.php
touch app/DataTransferObjects/UserData.php

# Create exceptions
php artisan make:exception PostNotFoundException
php artisan make:exception UnauthorizedException
php artisan make:exception ValidationException
```

## 📡 API Documentation

```bash
# Install Scribe for API documentation
composer require --dev knuckleswtf/scribe
php artisan vendor:publish --tag=scribe-config
php artisan scribe:generate
```

## 🔄 Caching & Performance

```bash
# Create cache management commands
php artisan make:command ClearAllCaches
php artisan make:command WarmUpCache

# Cache configuration
php artisan config:cache
php artisan route:cache
php artisan view:cache

# Clear caches
php artisan cache:clear
php artisan config:clear
php artisan route:clear
php artisan view:clear
```

## 📊 Admin Panel (Optional)

```bash
# Install Laravel Nova (paid) or Filament (free)
# Filament installation:
composer require filament/filament:"^3.0"
php artisan filament:install --panels
php artisan make:filament-user

# Create Filament resources
php artisan make:filament-resource Post
php artisan make:filament-resource Category
php artisan make:filament-resource User
```

## 🛠️ Complete Project Structure Commands

```bash
# Run all migrations with fresh database
php artisan migrate:fresh --seed

# Generate IDE helper files
php artisan ide-helper:generate
php artisan ide-helper:models
php artisan ide-helper:meta

# Optimize application
php artisan optimize

# Run tests
php artisan test
# OR with coverage
php artisan test --coverage

# Start development server
php artisan serve

# Start queue worker
php artisan queue:work

# Start schedule worker (in production)
php artisan schedule:work
```

## 📝 Git Setup

```bash
# Initialize git
git init
git add .
git commit -m "Initial Laravel backend setup"

# Create .gitignore additions
echo "*.log" >> .gitignore
echo ".env.backup" >> .gitignore
echo "storage/debugbar" >> .gitignore
```

## 🔍 Monitoring & Logging

```bash
# Create custom log channels
php artisan make:command CreateLogChannel

# View logs
tail -f storage/logs/laravel.log

# Monitor with Telescope (if installed)
# Visit: http://your-domain/telescope
```

## 🚦 Final Checklist Commands

```bash
# 1. Check all routes
php artisan route:list

# 2. Check database connection
php artisan db:show
php artisan db:table users

# 3. Run all tests
php artisan test

# 4. Check for vulnerabilities
composer audit

# 5. Optimize for production
php artisan optimize
php artisan config:cache
php artisan route:cache
php artisan view:cache

# 6. Generate API documentation
php artisan scribe:generate

# 7. Check application health
php artisan about
```

## 📦 Common Complete Setup Script

Create a setup script `setup.sh`:

```bash
#!/bin/bash

echo "🚀 Setting up Laravel Backend..."

# Install dependencies
composer install
npm install

# Environment setup
cp .env.example .env
php artisan key:generate

# Database setup
php artisan migrate:fresh --seed

# Storage link
php artisan storage:link

# Install Sanctum
php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
php artisan migrate

# Cache configuration
php artisan config:cache
php artisan route:cache

# Generate IDE helpers
php artisan ide-helper:generate
php artisan ide-helper:models --nowrite

echo "✅ Setup complete! Run 'php artisan serve' to start the server"
```

Make it executable:
```bash
chmod +x setup.sh
./setup.sh
```

## Vscode Extension

<img width="635" height="141" alt="image" src="https://github.com/user-attachments/assets/a6449ee8-25b8-4d1c-a70c-e29972d05814" />
<img width="746" height="155" alt="image" src="https://github.com/user-attachments/assets/6832e74c-7532-4fee-a35a-3cfadd5be48e" />
<img width="545" height="154" alt="image" src="https://github.com/user-attachments/assets/46dcbd88-a85c-4efa-ae2b-cd19e5ca5cb9" />
<img width="501" height="156" alt="image" src="https://github.com/user-attachments/assets/7f350196-3943-48e4-8b5c-50f88fd1d2ba" />
<img width="622" height="148" alt="image" src="https://github.com/user-attachments/assets/14d5a869-7317-4c6d-9c55-b410a56470b1" />
<img width="635" height="148" alt="image" src="https://github.com/user-attachments/assets/e9d787d6-82f6-4884-9eb4-486edabf6015" />
<img width="515" height="152" alt="image" src="https://github.com/user-attachments/assets/57e0b166-4c37-4a2d-a884-bfb1887e910b" />
<img width="657" height="134" alt="image" src="https://github.com/user-attachments/assets/94cd87e7-bd1d-4e24-964c-14b554d9c384" />













