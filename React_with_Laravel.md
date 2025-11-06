# React with Laravel - Ceygenic

## 🧱 1. Project Setup (after clone)

    composer install
    composer update
  
    npm install

### 🧩 2. Environment Setup
### File edited

  .env-example
  .env      (copy and name change)

| Purpose                | Command                    | Notes                               |
| ---------------------- | -------------------------- | ----------------------------------- |
| Generate app key       | `php artisan key:generate` | Sets APP_KEY in `.env`              |
| Link storage to public | `php artisan storage:link` | Makes `/storage` accessible via URL |
| Cache config           | `php artisan config:cache` | Improves config loading             |
| Clear config cache     | `php artisan config:clear` | Use when `.env` changes             |
| Clear route cache      | `php artisan route:clear`  |                                     |
| Clear view cache       | `php artisan view:clear`   |                                     |





### Database setup

    php artisan config:clear
    php artisan config:cache
    
    php artisan migrate
    php artisan migrate:fresh --seed
    php artisan storage:link


### Run:

    composer run dev

    

      composer run dev

