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

## Laravel MVC Architecture for React Starter Kit

<img width="724" height="560" alt="image" src="https://github.com/user-attachments/assets/a5f1b86e-d44b-468a-8240-3944aa49502d" />

###  Controller 

    php artisan make:controller ControllerName



### 🗄️ Database & Migrations

    php artisan config:clear
    php artisan config:cache
    
    php artisan migrate
    php artisan migrate:fresh --seed
    php artisan storage:link





### Run:

    composer run dev

## Extension: 

<img width="470" height="150" alt="image" src="https://github.com/user-attachments/assets/3444e8fa-9e9a-4983-b12d-a9400ee38936" />
<img width="614" height="126" alt="image" src="https://github.com/user-attachments/assets/f12495ec-3b65-4bf9-a193-c2fd40d834c6" />


## Library:

<img width="644" height="132" alt="image" src="https://github.com/user-attachments/assets/38b01d17-c912-481b-8854-44d3753b8d5b" />
https://lucide.dev/

<img width="650" height="125" alt="image" src="https://github.com/user-attachments/assets/4fe3935e-63a6-4bf8-909b-985886ee918f" />
https://inertiajs.com/

<img width="662" height="131" alt="image" src="https://github.com/user-attachments/assets/65e61548-3cb2-45e0-9a8f-e83264f36f21" />
https://ui.shadcn.com/





