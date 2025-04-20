# 📁 File Upload System with Email Notification (PHP + PHPMailer)

This project is a simple PHP-based file upload system that allows users to upload various file types and automatically sends an email confirmation using **PHPMailer** once a file is uploaded.

## ✨ Features

- Upload support for documents, images, and presentations
- File size and extension validation
- Automatic email confirmation via Gmail SMTP using PHPMailer
- Displays list of previously uploaded files with timestamp
- Minimal UI for quick usage

##  Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/php-file-upload-email.git
cd php-file-upload-email

### 2. Set Up Your Environment
Ensure your PHP environment is running (Apache, Nginx, or PHP built-in server) and that Composer is installed.

### 3. Install Dependencies
This project uses PHPMailer. Install it using Composer:

composer require phpmailer/phpmailer
If you're not using Composer, manually download PHPMailer and adjust the require path accordingly.

### 4. Configure Email Settings
Open the main PHP file and update the following values to match your email setup:
$mail->Username = 'your_email@gmail.com';       // Your Gmail
$mail->Password = 'your_app_password';          // Your app password
$mail->setFrom('your_email@gmail.com', 'Name');
$mail->addAddress('recipient_email@gmail.com', 'Recipient');
📌 For Gmail, make sure you generate and use an App Password.

### 5. Run the Project
Place the project in your web server root or use PHP's built-in server:
php -S localhost:8000
Open your browser and go to http://localhost:8000/.

--How It Works
Users select and upload a file.

The system validates file type and size.

If valid, the file is saved in the /uploads directory.

A confirmation email is sent to the predefined email address.

Uploaded files are listed on the page with their upload timestamp.

📁 Allowed File Types
pdf, docx, doc, xls, xlsx, ppt, pptx
jpg, jpeg, png, gif.

📌 Folder Structure
├── uploads/                # Folder where files are saved
├── index.php               # Main upload and email script
├── composer.json           # Composer dependencies
└── vendor/                 # Composer dependencies (after install)



