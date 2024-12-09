##### Center:
> Center describes a *typical value* of a datapoint. Two common measures of center:

**Mean**: average value = Q2 = sum / n

**Median**: Arrange data in order, then find the middle. If even, find avg of the two middle.

**Mode**: The most repeated value.
{2,2,2,5,5,5} mode = 2, 5
{1,2,3} mode = There is no mode

##### Spread:
> Spread describes the *variation* of the data. Two measures of spread are:

**Range**: difference between the highest and lowest values in our dataset = $max - min$

**Standard Deviation**: average distance between each data point and the mean.
> [!NOTE]
> See [[Calculator]] for StdDev

---
**IQR - Inter Quartile Range:** Q3 - Q1

**Outliers:**
- Low outlier $< Q_1 - 1.5 * IQR$ 
- High outlier $> Q_3 + 1.5 * IQR$

### Questions:
> If 𝑥 is the average of 𝑚 and 9, 𝑦 is the average of 2𝑚 and 15, and 𝑧 is the average of 3𝑚 and 18, what is the average of 𝑥, 𝑦, and 𝑧 in terms of 𝑚?

$x = (m+9)/2$
$y = (2m+15)/2$
$z = (3m + 18)/2$
$avg = (x+y+z)/3)$
$$
0.5m + 4.5 + m + 7.5 + 1.5m + 9
= 3m + 21
$$
> **About what percent of the boxes of raisins weighed more than 29 grams?** Q1 = 29
> ![](https://cdn.kastatic.org/ka-perseus-graphie/2b9e73c490d5fbc5cdcb1b6910e7103da58e3518.svg)

Since Q1 is 29, about 25% of data is lower than 29 and **75% is above 29**.

### Box Whisker Plots
Does not show outliers:
> ![](https://cdn.kastatic.org/ka-perseus-graphie/7f75d1d232769a7e065d6fde97c26512139149d7.svg)

Shows outliers:
> ![](https://cdn.kastatic.org/ka-perseus-graphie/09ccd0330dd307840c27ca250e6c0ed7fa7f7b8e.svg)

Points = outliers
Whisker: extends to furthest point that's not an outlier