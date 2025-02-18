# Import-Export-Excel-and-CSV
We will use the `maatwebsite/excel` composer package for import and export tasks. In this example, we will create a simple form for input where you can upload a CSV file and create multiple users. Then, I will create an export route that will download all users from the database in an Excel file.

### Steps to Setup Laravel 11 with Excel Import/Export

1. **Install Laravel 11**  
2. **Install maatwebsite/excel Package**  
3. **Create Dummy Records**  
4. **Create Import Class**  
5. **Create Export Class**  
6. **Create Controller**  
7. **Create Routes**  
8. **Create Blade File**  
9. **Run Laravel App**  

```bash
git clone https://github.com/ruhulamin63/Import-Export-Excel-and-CSV.git
```

```bash
cp .env.example .env
```

```bash
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your-db-name
DB_USERNAME=root
DB_PASSWORD=
```

```bash
composer install
```

```bash
php artisan migrate
```

### In this step, we will create some dummy records for the users table so we can export them later. Let's run the following Tinker command:
```bash
php artisan tinker
  
User::factory()->count(10)->create()
```

### Public Access Route
```bash
http://127.0.0.1:8000/users
```

#### ======== Enjoy coding ============