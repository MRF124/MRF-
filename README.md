<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mr. Maruf's News</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f8f9fa;
        }
        header {
            background-color: #007bff;
            color: white;
            padding: 10px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        header h1 {
            margin: 0;
        }
        header .clock {
            font-size: 1.2rem;
        }
        main {
            padding: 20px;
        }
        .news-section {
            margin-bottom: 20px;
        }
        .news-section h2 {
            margin-bottom: 10px;
        }
        .news-item {
            padding: 10px;
            background-color: white;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Mr. Maruf's News</h1>
        <div class="clock" id="clock">12:00 AM</div>
    </header>
    <main>
        <section class="news-section">
            <h2>Top Stories</h2>
            <div class="news-item">Sample news headline 1</div>
            <div class="news-item">Sample news headline 2</div>
            <div class="news-item">Sample news headline 3</div>
        </section>
        <section class="news-section">
            <h2>Technology</h2>
            <div class="news-item">Sample tech news 1</div>
            <div class="news-item">Sample tech news 2</div>
        </section>
    </main>

    <script>
        function updateClock() {
            const clockElement = document.getElementById('clock');
            const now = new Date();
            let hours = now.getHours();
            const minutes = now.getMinutes();
            const ampm = hours >= 12 ? 'PM' : 'AM';
            hours = hours % 12;
            hours = hours ? hours : 12; // The hour '0' should be '12'
            const minutesStr = minutes < 10 ? '0' + minutes : minutes;
            clockElement.textContent = `${hours}:${minutesStr} ${ampm}`;
        }

        setInterval(updateClock, 1000);
        updateClock(); // Initial call to set the clock immediately
    </script>
</body>
</html>
