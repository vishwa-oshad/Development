# Laravel + React Starter Kit

## Create Project 

    laravel new project-name

    select 
        ->> React ->> laravel --> 0 
        

## 🧱 Project Setup (after clone)

    composer install
    composer update
  
    npm install
    npm run build 


### 🧩 Environment Setup
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


### 🗄️ Database & Migrations

    php artisan config:clear
    php artisan config:cache
    
    php artisan migrate
    php artisan migrate:fresh --seed
    php artisan storage:link


### Run:

    composer run dev

## Extention: 

<img width="470" height="150" alt="image" src="https://github.com/user-attachments/assets/3444e8fa-9e9a-4983-b12d-a9400ee38936" />
<img width="614" height="126" alt="image" src="https://github.com/user-attachments/assets/f12495ec-3b65-4bf9-a193-c2fd40d834c6" />




