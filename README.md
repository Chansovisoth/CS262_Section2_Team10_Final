# CS262_Team10_API_Section2_AY2023-2024
Fully Complete API For CS262 Final Team10 Section2 AY2023-2024


To be able to utilise the full functions:
-   Ensure the profile picture functionality works by running the command: ```php artisan storage:link```
-   In app\Http\Controllers\ContactMailController.php, on line 26, Mail::to will send an email to the registered email (mailtrap cannot send to random emails so it can only work for ourden.cs262@gmail.com) (we can however change the MAIL env to sandbox and send it to mailtrap account)
