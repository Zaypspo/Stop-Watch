# Tittle

- Stop-Watch

## DESC

- Using from {HTML-CSS-JAVA_SCRIPT}

## You can follow youtube video

- [![Youtube Video](https://i9.ytimg.com/vi_webp/xXs6nVpWUAw/mqdefault.webp?v=61a312c1&sqp=CISqjI0G&rs=AOn4CLAITsmEBpkLEf8oNvcFAeHYY7pWqA)](https://youtu.be/xXs6nVpWUAw)

## ReadMe Card

- [![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=AiDarkEzio&repo=Stop-Watch&theme=nightowl)](https://github.com/AiDarkEzio/Stop-Watch)

### __CODE__

- ``HTML`` code

```html
    <div class="wrapper">
        <h1>Stopwatch</h1>
        <h2>JavaScript Stopwatch</h2>
        <p><span id="seconds">00</span>:<span id="tens">00</span></p>
        <button id="button-start">Start</button>
        <button id="button-stop">Stop</button>
        <button id="button-reset">Reset</button>
    </div> 
```

- ``CSS`` code

```css
body 
{
  background:#390053;
  font-family: "HelveticaNeue-Light", "Helvetica Neue Light", "Helvetica Neue", Helvetica, Arial, "Lucida Grande", sans-serif; 
  height:100%;
}

.wrapper 
{
  border-radius: 3px;
  background: #00c070;
  width: 800px;
  margin: 30px auto;
  color:rgb(47, 0, 255);
  text-align:center;
}

.wrapper:hover
{
  background: #00cf91;
  width: 800px;
  margin: 30px auto;
  color:rgb(122, 40, 255);
  text-align:center;
}

h1, h2, h3 
{
  font-family: 'Roboto', sans-serif;
  font-weight: 100;
  font-size: 2.6em;
  text-transform: uppercase;
}

#seconds, #tens
{
  font-size:2em;
}

button
{
  background:#ffa600;
  color:#fff;
  border: solid 1px #fff;
  text-decoration:none;
  cursor:pointer;
  font-size:1.2em;
  padding:18px 10px;
  width:180px;
  margin: 10px;
  outline: none;
  border-radius: 5px;
}
button:hover
{
  background:#fff;
  border: solid 1px #fff;
  color:#ffa600;
}
```

- ``JS`` code

```js
    window.onload = function () {
  
        var seconds = 00; 
        var tens = 00; 
        var appendTens = document.getElementById("tens")
        var appendSeconds = document.getElementById("seconds")
        var buttonStart = document.getElementById('button-start');
        var buttonStop = document.getElementById('button-stop');
        var buttonReset = document.getElementById('button-reset');
        var Interval ;

        buttonStart.onclick = function() {
            clearInterval(Interval);
            Interval = setInterval(startTimer, 10);
        }
    
        buttonStop.onclick = function() {
            clearInterval(Interval);
        }
    
        buttonReset.onclick = function() {
            clearInterval(Interval);
            tens = "00";
            seconds = "00";
            appendTens.innerHTML = tens;
            appendSeconds.innerHTML = seconds;
        }
    
        function startTimer () {  
            tens++; 
            
            if(tens <= 9){
                appendTens.innerHTML = "0" + tens;
            }

            if (tens > 9){
                appendTens.innerHTML = tens;
            } 

            if (tens > 99) {
                console.log("seconds");
                seconds++;
                appendSeconds.innerHTML = "0" + seconds;
                tens = 0;
                appendTens.innerHTML = "0" + 0;
            }

            if (seconds > 9){
                appendSeconds.innerHTML = seconds;
            }
        }
    }
```

### LICENSE

- **MIT License**

- *Copyright (c) 2021* ``Subadra Poshitha``
