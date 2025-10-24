# retail-sales-predictive
Predictive analytics project on retail sales data 
Seeing that Google Gemini can make basic generic charts from my data, from these charts we will try and use different models to predict sales from this specific retail store. 

On the contrary, the graphs provided are terrible, we'll make them better.
Before plotting everything, turning dependent vari date into dateType.Food for thought this method was coding is amazing running each cell and seeing the output on each, very nice.

 Sales over time plot(Trend)
 Its kind of all over the place with just the data I input, I im going to see if i can make it look a bit better. 

Before:
<img width="586" height="455" alt="download" src="https://github.com/user-attachments/assets/4f808a24-fdfc-4064-bc7b-157c7d572dae" />

After:
So I tried to do a body by body comparsion with the averages of the sales, but im starting to think that a line plot simply wont do to show a trend in sales by date(day).
<img width="1169" height="624" alt="download" src="https://github.com/user-attachments/assets/5037039c-a3f1-481e-bad8-b457a652149b" />

After2:
im going to group the dates by month instead of day
<img width="1178" height="624" alt="download" src="https://github.com/user-attachments/assets/ceec57f7-83d6-4f62-a52f-c0a6c7b4e393" />
It smoothed out by alot, although the average monthly sales are flat, sales are consistent im assuming. 
(Having diificulty with my weekly sales trend, I'll be back to it.) 

MACHINE LEARNING METHODS CONSIDERED:
Classical time series models and linear regression models
The choice has been linear regression since I am not advanced yet, but reading an article on it I found something pretty cool and useful. 
"The test_size=0.2 parameter reserves 20% of data for testing. The random_state=42 ensures reproducibility—you’ll get the same split every time you run the code. This is crucial for comparing different models or sharing results with colleagues." from: https://mljourney.com/step-by-step-linear-regression-in-jupyter-notebook/ 

This is the important set up basically because we need to train this model 80 percent of the way and test it 20 percent.
Ran into a big problem with linear regression had to change gender(Male and female) to binary(1 and 0) and now finding out I have missing values. Lot's to learn. 
In a crunch of time, so i took out gender entirely since that was the missing value although it was shown in the csv file. I will be coming back after to dinner to investigate the issue, i even went back in the csv file and changed the column for gender into binary. I finally got the linear regression to work with me though.

WHAT CAME OUT OF THIS PRACTICE ANALYSIS:
Coefficients in the Slope
[-3.14145462  0.69716868]
Age and week corresponds with these numbers age being -3.141 and week being 0.697.
Total amount decreases as age increasees and total amount increases and week increases.
and my intercept is 580.855
LINEAR REGRESSION EQUATION:

Total amount = -3.141age+0.697week + 580.855
 Actual   Predicted
521    1500  437.045386
737     100  454.844165
740     300  437.734164
660     100  447.511308
411    2000  527.442010
..      ...         ...
408     900  523.250607
332    1200  412.610918
208     200  494.977516
613    1200  461.127075
78      300  476.834348
MY MODEL IS SO BAD, im so fired lol.
I'm adding more parameters. That didn't change a thing.














