# Login Form

![register](https://github.com/ByteWizCode/login-form-app/assets/136901319/436bf469-6a9b-4830-9765-eaee3acea0cd)

![login](https://github.com/ByteWizCode/login-form-app/assets/136901319/0c2cfcbf-53ad-4789-acde-9a6bf95a64ee)

![1](https://github.com/ByteWizCode/login-form-app/assets/136901319/4574e810-f70a-4359-94f2-86c2a766124e)
![2](https://github.com/ByteWizCode/login-form-app/assets/136901319/e475e2a3-1301-4b96-a873-68710a86fb6b)
![3](https://github.com/ByteWizCode/login-form-app/assets/136901319/111f7ecc-2895-4a40-a633-7ea9462c2721)
![4](https://github.com/ByteWizCode/login-form-app/assets/136901319/6cde3169-16ef-4dc8-9885-c486160916f8)
![5](https://github.com/ByteWizCode/login-form-app/assets/136901319/9b107551-28ff-406b-8471-11d593277034)
![6](https://github.com/ByteWizCode/login-form-app/assets/136901319/f20f0845-429e-4678-9eda-e4acc845cef4)
![7](https://github.com/ByteWizCode/login-form-app/assets/136901319/a4defd34-3b99-4688-995d-de54acc70dfc)
![8](https://github.com/ByteWizCode/login-form-app/assets/136901319/6143e86a-807b-43ae-8434-628b6a2d5170)


## How to run the code

1. git clone https://github.com/ByteWizCode/login-form-app.git
2. cd login-form-app
3. run : `composer install`
4. run : `npm install`
5. run : `npm run dev`
6. cp .env.example `.env` dan sesuaikan konfigurasi database.

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE={{ nama_database }}
DB_USERNAME=root
DB_PASSWORD=
```

Isi `{{ nama_database }}` dengan nama database yang ingin digunakan.

7. Sesuaikan konfigurasi SMTP pada file `.env` untuk mengirim email.

```
MAIL_MAILER=smtp
MAIL_HOST={{ host_smtp }}
MAIL_PORT={{ port_smtp }}
MAIL_USERNAME={{ username_smtp }}
MAIL_PASSWORD={{ password_smtp }}
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS="hello@example.com"
MAIL_FROM_NAME="${APP_NAME}" 
```

Isi `{{ host_smtp }}`, `{{ port_smtp }}`, `{{ username_smtp }}`, dan `{{ password_smtp }}` dengan konfigurasi SMTP yang ingin digunakan. Dapat menggunakan SMTP dengan menggunakan service seperti [Mailtrap](https://mailtrap.io/) (free) atau [SendGrid](https://sendgrid.com/) (free).

8. Sesuaikan konfigurasi ReCaptcha pada file `.env` untuk mengaktifkan fitur captcha.

```
RECAPTCHA_SITE_KEY={{ site_key }}
RECAPTCHA_SECRET_KEY={{ secret_key }}
RECAPTCHA_SITE=https://www.google.com/recaptcha/admin/
```

Daftar akun ReCaptcha [disini](https://www.google.com/recaptcha/admin/create). gunakan recapcha v2.

9. run : `php artisan key:generate`
10. run : `php artisan migrate:fresh --seed`
11. run : `php artisan serve`
12. Buka browser dan akses `http://localhost:8000`.
