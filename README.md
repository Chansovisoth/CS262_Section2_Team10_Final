# CS262_Team10_API_Section2_AY2023-2024

To utilize all functionalities of this project, please follow the steps below:

### Profile Picture Functionality

Ensure the profile picture feature works by running the following command:

```bash
php artisan storage:link
```

### Email Functionality

#### Frontend

In `app\Http\Controllers\ContactMailController.php`, on line 26, the `Mail::to` method will send an email to the registered email address. Note that Mailtrap can only send emails to specific addresses, so it will work for `ourden.cs262@gmail.com`.

#### API

In `app\Http\Controllers\Auth\LoginRegisterController.php`, on line 56, the `Mail::to` method will send an email to the registered email address. Similar to the frontend, Mailtrap can only send emails to specific addresses. Therefore, it will work for `ourden.cs262@gmail.com`. However, you can change the `MAIL` environment variable to `sandbox` to send emails to the Mailtrap account.

### .env File Configuration

To ensure the `.env` file is configured correctly, copy and paste the content below:

```env
APP_NAME=Laravel
APP_ENV=local
APP_KEY=base64:m6oUsH3dRBnHQlAgPVn5EmiAi1kSLoZcyOjPAgDGGys=
APP_DEBUG=true
APP_URL=http://localhost

LOG_CHANNEL=stack
LOG_DEPRECATIONS_CHANNEL=null
LOG_LEVEL=debug

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=cs262_final
DB_USERNAME=root
DB_PASSWORD=

BROADCAST_DRIVER=log
CACHE_DRIVER=file
FILESYSTEM_DISK=local
QUEUE_CONNECTION=sync
SESSION_DRIVER=file
SESSION_LIFETIME=120

MEMCACHED_HOST=127.0.0.1

REDIS_HOST=127.0.0.1
REDIS_PASSWORD=null
REDIS_PORT=6379

# --- FOR MAILTRAP DEMO MAIL (ourden.cs262@gmail.com) ---
MAILTRAP_API_KEY=8dd9b163f6ee899e4482dca666e3a82a
MAIL_MAILER=smtp
MAIL_HOST=live.smtp.mailtrap.io
MAIL_PORT=587
MAIL_USERNAME=api
MAIL_PASSWORD=8dd9b163f6ee899e4482dca666e3a82a
MAIL_FROM_ADDRESS="no-reply@demomailtrap.com"
MAIL_FROM_NAME="OURDEN"

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=us-east-1
AWS_BUCKET=
AWS_USE_PATH_STYLE_ENDPOINT=false

PUSHER_APP_ID=
PUSHER_APP_KEY=
PUSHER_APP_SECRET=
PUSHER_HOST=
PUSHER_PORT=443
PUSHER_SCHEME=https
PUSHER_APP_CLUSTER=mt1

VITE_PUSHER_APP_KEY="${PUSHER_APP_KEY}"
VITE_PUSHER_HOST="${PUSHER_HOST}"
VITE_PUSHER_PORT="${PUSHER_PORT}"
VITE_PUSHER_SCHEME="${PUSHER_SCHEME}"
VITE_PUSHER_APP_CLUSTER="${PUSHER_APP_CLUSTER}"

GOOGLE_CLIENT_ID=728268641713-pgm0sl00i70l7maorrc29a7mr8rkap9v.apps.googleusercontent.com
GOOGLE_CLIENT_SECRET=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
GOOGLE_REDIRECT_URL=http://127.0.0.1:8000/google/callback
```
