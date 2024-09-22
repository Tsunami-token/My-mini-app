<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tsunami Airdrop</title>
    <style>
        body {
            background-color: black;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: Arial, sans-serif;
            flex-direction: column;
            text-align: center;
        }
        h1 {
            font-size: 48px;
            margin-bottom: 20px;
        }
        .invite-btn {
            background-color: #00aaff;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            font-size: 18px;
            border-radius: 5px;
            margin-top: 20px;
        }
        .countdown {
            font-size: 32px;
        }
    </style>
</head>
<body>
    <h1>Tsunami Airdrop</h1>
    <div class="countdown" id="countdown"></div>
    <a class="invite-btn" href="https://t.me/Tsunami_token_bot?start=invite">Invite Friends</a>

    <script>
        // تاریخ و زمان شروع ایردراپ (تاریخ و زمان مشخص را اینجا وارد کنید)
        const targetDate = new Date('2024-9-22T00:00:00Z').getTime();

        function updateCountdown() {
            const now = new Date().getTime();
            const distance = targetDate - now;

            if (distance < 0) {
                document.getElementById('countdown').innerHTML = "Airdrop Started!";
                clearInterval(interval);
                return;
            }

            const days = Math.floor(distance / (1000 * 60 * 60 * 24));
            const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((distance % (1000 * 60)) / 1000);

            document.getElementById('countdown').innerHTML =
                days + "d " + hours + "h " + minutes + "m " + seconds + "s ";
        }

        // بروزرسانی شمارش معکوس هر ثانیه
        const interval = setInterval(updateCountdown, 1000);

        // به‌روزرسانی در بارگذاری صفحه
        updateCountdown();
    </script>
</body>
</html>
