<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Car Sales</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            text-align: center;
        }
        header {
            background: linear-gradient(135deg, #ff6600, #cc5500);
            color: #fff;
            padding: 20px 0;
            font-size: 28px;
            font-weight: bold;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        .container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            padding: 20px;
        }
        .car {
            background: #fff;
            border-radius: 15px;
            margin: 20px;
            padding: 20px;
            width: 320px;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
        }
        .car:hover {
            transform: scale(1.08);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.4);
        }
        img {
            width: 100%;
            border-radius: 10px;
            transition: transform 0.3s ease-in-out;
        }
        .car:hover img {
            transform: scale(1.05);
        }
        button {
            background: #ff6600;
            color: #fff;
            padding: 12px 18px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 18px;
            font-weight: bold;
            transition: background 0.3s ease-in-out, transform 0.2s ease-in-out;
        }
        button:hover {
            background: #cc5500;
            transform: scale(1.1);
        }
        footer {
            margin-top: 40px;
            background: #333;
            color: #fff;
            padding: 15px 0;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Our Car Sales</h1>
    </header>
    <div class="container">
        <div class="car">
            <img src="car1.jpg" alt="Car 1">
            <h2>Car Model 1</h2>
            <p>Price: $20,000</p>
            <button>Buy Now</button>
        </div>
        <div class="car">
            <img src="car2.jpg" alt="Car 2">
            <h2>Car Model 2</h2>
            <p>Price: $25,000</p>
            <button>Buy Now</button>
        </div>
        <div class="car">
            <img src="car3.jpg" alt="Car 3">
            <h2>Car Model 3</h2>
            <p>Price: $30,000</p>
            <button>Buy Now</button>
        </div>
    </div>
    <footer>
        <p>&copy; 2025 Car Sales. All Rights Reserved.</p>
    </footer>
</body>
</html>
