Objective:
To design and provide a user-friendly, accurate, and efficient tool for performing basic arithmetic operations such as addition, subtraction, multiplication, and division. The standard calculator should cater to a wide range of users, from students and professionals to everyday individuals needing quick and reliable mathematical computations.

Description:
A standard calculator is an electronic device or software application used to perform basic arithmetic calculations. It typically features a simple interface with numeric buttons (0-9), basic operation keys (addition, subtraction, multiplication, division), and function keys such as clear (C), decimal point, and equals (=).

The standard calculator is designed for ease of use, allowing users to perform calculations quickly and accurately. It is commonly used in educational settings, business environments, and everyday life for tasks such as budgeting, invoicing, homework, and general problem-solving. The calculator can be a physical handheld device or a software application available on computers, smartphones, and other digital platforms.

Program:
```C
calc.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Calculator</title>
    <link rel="stylesheet" href="theme.css">
</head>
<body>
    <div class="container">
        <h3 class="text">RAGUL E (212221043005)</h3>

        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button class="color">(</button></td>
                    <td><button class="color">)</button></td>
                    <td><button class="color">C</button></td>
                    <td><button class="color">%</button></td>
                </tr>
                <tr>
                    <td><button>7</button></td>
                    <td><button>8</button></td>
                    <td><button>9</button></td>
                    <td><button class="color">*</button></td>
                </tr>
                <tr>
                    <td><button>4</button></td>
                    <td><button>5</button></td>
                    <td><button>6</button></td>
                    <td><button class="color">-</button></td>
                </tr>
                <tr>
                    <td><button>1</button></td>
                    <td><button>2</button></td>
                    <td><button>3</button></td>
                    <td><button class="color">+</button></td>
                </tr>
                <tr>
                    <td><button>0</button></td>
                    <td><button class="color">.</button></td>
                    <td><button class="color">/</button></td>
                    <td><button class="color">=</button></td>
                </tr>
            </table>
        </div>
    </div>

    <script src="code.js"></script>
</body>
</html>
```
theme.css

.container {
    text-align: center;
    margin-top: 23px;
}

.calculator {
    border: none;
    background-color: #b1a4f1;
    padding: 30px;
    border-radius: 30px;
    display: inline-block;
}

h1 {
    font-size: 40px;
    font-family: Arial, Helvetica, sans-serif;
}

h3 {
    font-size: 20px;
    font-weight: bold;
    color: black;
    text-align: center;
    margin: auto;
    margin-top: 20px;
}

input {
    text-align: right;
    border-radius: 21px;
    border: 2px solid rgb(13, 13, 13);
    padding: 20px;
    background: rgb(233, 233, 233);
    font-size: 40px;
    height: 60px;
    width: 290px;
    color: rgb(11, 11, 11);
}

table {
    margin: auto;
}

button {
    border-radius: 20px;
    border: 0;
    outline: 0;
    box-shadow: -8px -8px 15px rgba(180, 180, 180, 0.1),  5px 5px 15px rgba(0, 0, 0, 0.2);
    font-size: 20px;
    background: transparent;
    color: rgb(8, 6, 8);
    width: 60px;
    height: 60px;
    margin: 6px;
    cursor: pointer;
}
```
code.js

.color {
    color: rgb(15, 11, 15);
}

let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }
    })
}
```
## OUTPUT:
![Screenshot 2024-07-05 131912](https://github.com/R01ty/calculator.css/assets/142526219/6d6aaccb-338a-45b1-9e51-573c04b7506f)
![Screenshot 2024-07-05 135035](https://github.com/R01ty/calculator.css/assets/142526219/808789a0-ac4c-48b3-bfb4-a71b543533ab)


