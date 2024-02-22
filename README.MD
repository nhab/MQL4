## Basics
 read about basics [here](https://www.cashbackforex.com/article/basic-structure-of-an-expert-advisor)
## Input propeties
To define a variable itse value can be set by user, use input keyword:
```
input int MaxStopLoss=5000;  
```
## Indicator and Expert advisor difference ( programatically )
Indicatore uses OnInit() and OnCalculator events, but

[EA](https://www.mql5.com/en/articles/1495) usees Init() and Start() events

see [template1](https://github.com/trevone/ea-template/blob/master/ea-template.mq4)
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

[Example1](https://book.mql4.com/samples/icustom)
## Exper Advisor ( EA )

this is the template :
```
//| BasicTemplate.mq4 |

//| Copyright © 2011, ExcelMarkets |

//| /school |

//+——————————————————–+

// Structure #1 (Optional): Directives
#property copyright “Copyright © 2011, excelmarkets.com”

#property link “/school”// Structure #2 (Optional): Input parameters

extern double Lots=0.1;

extern int TakeProfit = 250;

extern int StopLoss = 150;

// Structural #3 (Optional): expert initialization function

int init()
{

//—- start up code
return(0);
}

// Structure #4 (Optional): expert deinitialization function
<structural#4>
int deinit()
{

//—-  shutdown code
return(0);
}

// Structure #5 (Essential): expert start function

int start()
{

//—- your trade conditions and orders
return(0);
}

// Structure #6 (Optional): Custom Functions
</structural#4>

int customfunction1(){
// your custom option conditions
return (0); }

void customfunction2(){
// your custom function conditions
}
```


  
