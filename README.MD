##Input propeties
To define a variable itse value can be set by user, use input keyword:
```
input int MaxStopLoss=5000;  
```
## Indicator and Expert advisor difference ( programatically )
Indicatore uses OnInit() and OnCalculator events, but

[EA](https://www.mql5.com/en/articles/1495) usees Init() and Start() events
## Indicator
Every mql4 [indicator](https://docs.mql4.com/customind) needs at list one array of doubles to keep value of prices of line of the indicator
```
double buf0[];
```
oninit function is used to initialize the varibles, including the buffers
```
int OnInit()
{ 
  SetIndexBuffer(0,buf0);     
  SetIndexStyle (0,DRAW_LINE,STYLE_SOLID,2,clrYellowGreen);
  return(INIT_SUCCEEDED);
}
```
OnCalculate is the repeating event for each candle



  
