<p align="center">
  <a href="https://www.youtube.com/@LearnWithSazzad">YouTube Channel</a> | 
  <a href="https://github.com/sazzadhossain1623/">Github</a> |
  <a href="https://www.facebook.com/LWS01">Facebook</a> |
  <a href="https://react-hook-form.com/faqs">FAQs</a> |
</p>

### Animated Neon Text Glow by HTML & CSS

```jsx
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body {
            margin: 0;
            height: 100vh;
            align-items: center;
            justify-content: center;
            background-color: black;
        }

        .neon {
            position: relative;
            overflow: hidden;
            filter: brightness(200%);
        }

        .text {
            background-color: black;
            color: #fff;
            font-size: 180px;
            font-weight: bold;
            text-transform: uppercase;
            position: relative;
            user-select: none;
        }

        .text::before {
            content: attr(data-text);
            position: absolute;
            color: #fff;
            filter: blur(0.02em);
            mix-blend-mode: difference;
        }

        .gradient {
            position: absolute;
            background: linear-gradient(
                45deg, 
                red,gold, lightgreen, gold, 
                red);
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            mix-blend-mode: multiply;
        }

        .spotlight {
            position: absolute;
            top: -100%;
            left: -100%;
            right: 0;
            bottom: 0;
            background: radial-gradient(circle, white, transparent 25%) center/25% 25%, radial-gradient(circle, white, black 25%)center/12.5% 12.5%;
            animation: light 5s linear infinite;
            mix-blend-mode: color-dodge;
        }

        @keyframes light {
            to {
                transform: translate(50%, 50%);
            }
        }
    </style>
</head>

<body>
    <div class="neon">
        <span class="text" data-text="sazzad">Sazzad</span>
        <span class="gradient"></span>
        <span class="spotlight"></span>
    </div>
</body>

</html>
```
