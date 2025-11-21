🐦 Flappy Bird Game (Web Version)
A lightweight, browser-based recreation of the classic Flappy Bird game, built entirely with HTML5, CSS3, and Vanilla JavaScript. This project demonstrates DOM manipulation, game loops using requestAnimationFrame, and collision detection logic.

(Note: Capture a screenshot of your game running and save it as game-preview.png in your images folder to display it here.)

✨ Features
Physics Engine: Simulates gravity and jump mechanics for smooth movement.

Dynamic Obstacles: Pipes are generated with random heights and gaps endlessly.

Collision Detection: Pixel-perfect detection using getBoundingClientRect() to handle game-over states (pipes, ground, or ceiling collisions).

Score Tracking: Real-time score updates when passing pipes.

Audio Effects: Integrated sound effects for scoring points and game over.

Responsive Design: Adapts to different screen sizes via CSS Media Queries.

🚀 Tech Stack
HTML5: Semantic structure.

CSS3: Styling, background management, and responsive adjustments.

JavaScript (ES6): Core game logic, event listeners, and state management.

📂 Project Structure
To ensure the game runs correctly, your file structure must match the paths defined in the code:

Plaintext

Flappy-Bird-JS/
│
├── index.html          # Main entry point
├── style.css           # Styling and assets loading
├── script.js           # Game logic
│
├── images/             # Image assets
│   ├── background-img.png
│   ├── Bird.png
│   ├── Bird-2.png
│   └── favicon.ico
│
└── sounds effect/      # Audio assets (Note the space in the folder name)
    ├── point.mp3
    └── die.mp3
⚠️ Important: The JavaScript code references the folder 'sounds effect' (with a space). Ensure your folder name matches exactly, or update the path in script.js.

🎮 How to Play
Start the Game: Press Enter on your keyboard.

Control the Bird: Press ArrowUp or the Spacebar to fly upwards.

Objective: Navigate through the gaps in the green pipes without hitting them or touching the ground/ceiling.

Restart: If you crash, press Enter to restart the game.

💻 Installation & Setup
You don't need to install any dependencies (like Node.js) to run this game.

Clone the repository:

Bash

git clone https://github.com/YOUR-USERNAME/REPO-NAME.git
Run the game: Simply navigate to the folder and double-click index.html to open it in your default web browser.

🧠 Code Highlights
The Game Loop
Instead of setInterval, this project uses requestAnimationFrame for smoother rendering and better performance:

JavaScript

function play(){
    function move(){
        // Logic for moving pipes
        requestAnimationFrame(move);
    }
    requestAnimationFrame(move);
    // ... gravity logic ...
}
Collision Detection
The game calculates collisions by comparing the coordinates of the bird and the pipes in real-time:

JavaScript

if(
    bird_props.left < pipe_props.left + pipe_props.width && 
    bird_props.left + bird_props.width > pipe_props.left && 
    bird_props.top < pipe_props.top + pipe_props.height && 
    bird_props.top + bird_props.height > pipe_props.top
){
    game_state = 'End'; // Collision detected
}
🤝 Contributing
Contributions, issues, and feature requests are welcome!

Fork the project.

Create your Feature Branch (git checkout -b feature/AmazingFeature).

Commit your changes (git commit -m 'Add some AmazingFeature').

Push to the branch (git push origin feature/AmazingFeature).

Open a Pull Request.

📝 License
This project is open source and available for educational purposes.


🐦 بازی Flappy Bird (نسخه تحت وب)
یک بازسازی ساده و جذاب از بازی محبوب Flappy Bird که با استفاده از HTML5، CSS3 و Vanilla JavaScript خالص پیاده‌سازی شده است. این پروژه برای درک نحوه کار با DOM، انیمیشن‌ها در جاوااسکریپت و منطق بازی‌های دو بعدی بسیار مفید است.

(پیشنهاد: یک اسکرین‌شات از بازی خود بگیرید و با نام game-preview.png در پوشه images ذخیره کنید تا اینجا نمایش داده شود)

✨ ویژگی‌ها
مکانیزم جاذبه: شبیه‌سازی سقوط آزاد پرنده با استفاده از قوانین فیزیک ساده.

تولید موانع تصادفی: لوله‌ها با ارتفاع‌های متفاوت به صورت پویا تولید می‌شوند.

سیستم امتیازدهی: محاسبه امتیاز با عبور از هر لوله.

تشخیص برخورد (Collision Detection): پایان بازی در صورت برخورد با لوله‌ها، زمین یا سقف.

افکت‌های صوتی: پخش صدا هنگام امتیازگیری و باختن.

ریسپانسیو (Responsive): سازگار با اندازه صفحه‌نمایش‌های مختلف (موبایل و دسکتاپ).

🚀 تکنولوژی‌های استفاده شده
HTML5: ساختار اصلی صفحه.

CSS3: استایل‌دهی، انیمیشن‌های پس‌زمینه و طراحی ریسپانسیو.

JavaScript (ES6): منطق بازی، کنترل رویدادها (Events) و حلقه انیمیشن (requestAnimationFrame).

📂 ساختار فایل‌ها
برای اینکه بازی به درستی اجرا شود، ساختار پوشه شما باید به شکل زیر باشد:

Plaintext

Flappy-Bird-JS/
│
├── index.html          # فایل اصلی بازی
├── style.css           # فایل استایل‌ها
├── script.js           # منطق بازی
│
├── images/             # پوشه تصاویر
│   ├── background-img.png
│   ├── Bird.png
│   ├── Bird-2.png
│   └── favicon.ico
│
└── sounds effect/      # پوشه صداها
    ├── point.mp3
    └── die.mp3
نکته مهم: مطمئن شوید که فایل‌های تصویر و صدا را در پوشه‌های مربوطه قرار داده‌اید، در غیر این صورت بازی لود نمی‌شود.

🎮 نحوه اجرای بازی
این پروژه نیاز به نصب هیچ وابستگی (Dependency) یا کتابخانه‌ای ندارد.

ریپازیتوری را کلون کنید یا فایل‌ها را دانلود کنید:

Bash

git clone https://github.com/USERNAME/REPOSITORY-NAME.git
فایل index.html را در مرورگر خود باز کنید (دابل کلیک کنید).

🕹️ کنترل‌های بازی
شروع بازی: کلید Enter را فشار دهید.

پرش (بالا رفتن): کلید ArrowUp (فلش بالا) یا Space (فاصله).

شروع مجدد: پس از باخت، کلید Enter را فشار دهید.

🧠 بررسی کد (نکات آموزشی)
این پروژه شامل مفاهیم زیر است که در فایل script.js قابل مشاهده هستند:

Game Loop: استفاده از requestAnimationFrame برای ایجاد انیمیشن روان به جای setInterval.

DOM Manipulation: ایجاد و حذف عناصر HTML (لوله‌ها) به صورت پویا (document.createElement).

BoundingClientRect: استفاده از متد getBoundingClientRect() برای تشخیص دقیق موقعیت عناصر جهت بررسی برخورد (Collision).

🤝 مشارکت (Contributing)
اگر ایده‌ای برای بهبود بازی دارید (مثل اضافه کردن حالت شب، تغییر اسکین‌ها یا ثبت بالاترین امتیاز در LocalStorage)، خوشحال می‌شوم که مشارکت کنید:

این پروژه را Fork کنید.

یک Branch جدید بسازید (git checkout -b feature/NewFeature).

تغییرات خود را Commit کنید (git commit -m 'Add some NewFeature').

آن را Push کنید (git push origin feature/NewFeature).

یک Pull Request باز کنید.

📝 لایسنس
این پروژه به صورت متن‌باز (Open Source) منتشر شده است و استفاده از آن برای مقاصد آموزشی آزاد است.

ساخته شده با ❤️ و ☕
