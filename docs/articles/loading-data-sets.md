---
layout: default
title: "Loading the Statistical Thinking Data Sets in R"
date: 2022-06-11
original: https://rpubs.com/kambonalytic/913637
---

[← Back to portfolio](../index.md)

*Published 2022-06-11 · Originally on [RPubs](https://rpubs.com/kambonalytic/913637) · Data: [Statistical Thinking datasets](http://pluto.huji.ac.il/~msby/StatThink/)*

```r
cars<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/cars.csv')
aids<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/aids.csv')
cushings<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/cushings.csv')
diet<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/diet.csv')
discriminate<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/discriminate.csv')
ex1<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/ex1.csv')
ex2<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/ex2.csv')
flowers<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/flowers.csv')
height<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/height.csv')
job<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/job.csv')
QC<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/QC.csv')
magnets<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/magnets.csv')
pop1<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/pop1.csv')
pop2<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/pop2.csv')
pop3<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/pop3.csv')
teacher<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/teacher.csv')
transfusion<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/transfusion.csv')
sleep_paired<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/sleep_paired.csv')
sleep_unpaired<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/sleep_unpaired.csv')
weapons<-read.csv('http://pluto.huji.ac.il/~msby/StatThink/Datasets/weapons.csv')
```

```r
head(cars)
```

```text
##          make fuel.type num.of.doors  body.style drive.wheels engine.location
## 1 alfa-romero       gas          two convertible          rwd           front
## 2 alfa-romero       gas          two convertible          rwd           front
## 3 alfa-romero       gas          two   hatchback          rwd           front
## 4        audi       gas         four       sedan          fwd           front
## 5        audi       gas         four       sedan          4wd           front
## 6        audi       gas          two       sedan          fwd           front
##   wheel.base length width height curb.weight engine.size horsepower peak.rpm
## 1       88.6  168.8  64.1   48.8        2548         130        111     5000
## 2       88.6  168.8  64.1   48.8        2548         130        111     5000
## 3       94.5  171.2  65.5   52.4        2823         152        154     5000
## 4       99.8  176.6  66.2   54.3        2337         109        102     5500
## 5       99.4  176.6  66.4   54.3        2824         136        115     5500
## 6       99.8  177.3  66.3   53.1        2507         136        110     5500
##   city.mpg highway.mpg price
## 1       21          27 13495
## 2       21          27 16500
## 3       19          26 16500
## 4       24          30 13950
## 5       18          22 17450
## 6       19          25 15250
```

```r
tail(cars)
```

```text
##      make fuel.type num.of.doors body.style drive.wheels engine.location
## 200 volvo       gas         four      wagon          rwd           front
## 201 volvo       gas         four      sedan          rwd           front
## 202 volvo       gas         four      sedan          rwd           front
## 203 volvo       gas         four      sedan          rwd           front
## 204 volvo    diesel         four      sedan          rwd           front
## 205 volvo       gas         four      sedan          rwd           front
##     wheel.base length width height curb.weight engine.size horsepower peak.rpm
## 200      104.3  188.8  67.2   57.5        3157         130        162     5100
## 201      109.1  188.8  68.9   55.5        2952         141        114     5400
## 202      109.1  188.8  68.8   55.5        3049         141        160     5300
## 203      109.1  188.8  68.9   55.5        3012         173        134     5500
## 204      109.1  188.8  68.9   55.5        3217         145        106     4800
## 205      109.1  188.8  68.9   55.5        3062         141        114     5400
##     city.mpg highway.mpg price
## 200       17          22 18950
## 201       23          28 16845
## 202       19          25 19045
## 203       18          23 21485
## 204       26          27 22470
## 205       19          25 22625
```

```r
head(aids)
```

```text
##   year diagnosed deaths
## 1 1981       319    121
## 2 1982      1170    453
## 3 1983      3076   1482
## 4 1984      6240   3466
## 5 1985     11776   6878
## 6 1986     19032  11987
```

```r
tail(aids)
```

```text
##    year diagnosed deaths
## 17 1997     47149  20736
## 18 1998     38393  19005
## 19 1999     25174  18454
## 20 2000     25522  17347
## 21 2001     25643  17402
## 22 2002     26464  16371
```

```r
head(cushings)
```

```text
##   tetra pregn type
## 1   3.1 11.70    a
## 2   3.0  1.30    a
## 3   1.9  0.10    a
## 4   3.8  0.04    a
## 5   4.1  1.10    a
## 6   1.9  0.40    a
```

```r
tail(cushings)
```

```text
##    tetra pregn type
## 22   5.1   0.4    u
## 23  12.9   5.0    u
## 24  13.0   0.8    u
## 25   2.6   0.1    u
## 26  30.0   0.1    u
## 27  20.5   0.8    u
```

```r
head(diet)
```

```text
##   type health
## 1  aha cancer
## 2  aha cancer
## 3  aha cancer
## 4  aha cancer
## 5  aha cancer
## 6  aha cancer
```

```r
tail(diet)
```

```text
##     type  health
## 600  med healthy
## 601  med healthy
## 602  med healthy
## 603  med healthy
## 604  med healthy
## 605  med healthy
```

```r
head(discriminate)
```

```text
##   weight time
## 1 BMI=23   15
## 2 BMI=23   15
## 3 BMI=23   45
## 4 BMI=23   40
## 5 BMI=23   45
## 6 BMI=23   20
```

```r
tail(discriminate)
```

```text
##    weight time
## 66 BMI=30   30
## 67 BMI=30   30
## 68 BMI=30   30
## 69 BMI=30   30
## 70 BMI=30   30
## 71 BMI=30   30
```

```r
head(ex1)
```

```text
##        id    sex height
## 1 5696379 FEMALE    182
## 2 3019088   MALE    168
## 3 2038883   MALE    172
## 4 1920587 FEMALE    154
## 5 6006813   MALE    174
## 6 4055945 FEMALE    176
```

```r
tail(ex1)
```

```text
##          id    sex height
## 95  9448072 FEMALE    174
## 96  7085816   MALE    187
## 97  3596409 FEMALE    141
## 98  9383288   MALE    195
## 99  1582961 FEMALE    129
## 100 9805356   MALE    172
```

```r
head(flowers)
```

```text
##   Sepal.Length Sepal.Width Petal.Length Petal.Width Species
## 1          5.1         3.5          1.4         0.2  setosa
## 2          4.9         3.0          1.4         0.2  setosa
## 3          4.7         3.2          1.3         0.2  setosa
## 4          4.6         3.1          1.5         0.2  setosa
## 5          5.0         3.6          1.4         0.2  setosa
## 6          5.4         3.9          1.7         0.4  setosa
```

```r
tail (flowers)
```

```text
##     Sepal.Length Sepal.Width Petal.Length Petal.Width   Species
## 145          6.7         3.3          5.7         2.5 virginica
## 146          6.7         3.0          5.2         2.3 virginica
## 147          6.3         2.5          5.0         1.9 virginica
## 148          6.5         3.0          5.2         2.0 virginica
## 149          6.2         3.4          5.4         2.3 virginica
## 150          5.9         3.0          5.1         1.8 virginica
```

```r
head(height)
```

```text
##   index    sex hight
## 1     1   MALE   190
## 2     2 FEMALE   180
## 3     3 FEMALE   180
## 4     4 FEMALE   180
## 5     5 FEMALE   179
## 6     6 FEMALE   180
```

```r
tail(height)
```

```text
##     index  sex hight
## 95     95 MALE   191
## 96     96 MALE   190
## 97     97 MALE   189
## 98     98 MALE   189
## 99     99 MALE   190
## 100   100 MALE   191
```

```r
head(job)
```

```text
##    grip   arm ratings  sims
## 1 105.5  80.5    31.8  1.18
## 2 106.5  93.0    39.8  0.94
## 3  94.0  81.0    46.8  0.84
## 4  90.5  33.5    52.2 -2.45
## 5 104.0  47.5    31.2  1.00
## 6 171.0 125.5    46.6  4.38
```

```r
tail(job)
```

```text
##      grip  arm ratings  sims
## 142 131.0 86.0    37.0  1.03
## 143 147.0 71.0    57.2  0.53
## 144 109.5 86.5    43.0  2.89
## 145  54.0 67.5    41.7 -1.38
## 146 126.0 63.5    37.0  1.33
## 147  94.0 38.0    37.3 -1.53
```

```r
head(QC)
```

```text
##      h1    h2    h3    h4    h5    h6    h7    h8
## 1 16.13 16.16 15.85 16.09 16.05 16.11 15.94 16.00
## 2 16.09 16.04 15.93 15.84 15.97 15.94 15.97 16.06
## 3 16.02 16.05 16.02 16.01 15.83 15.79 16.06 15.85
## 4 16.05 15.89 15.99 15.93 15.93 15.99 15.94 15.88
## 5 16.16 15.94 15.83 16.04 15.86 15.94 16.00 15.98
## 6 16.04 15.86 15.73 15.96 15.96 15.94 15.85 15.92
```

```r
tail(QC)
```

```text
##       h1    h2    h3    h4    h5    h6    h7    h8
## 45 16.00 16.01 15.84 16.31 16.09 15.81 15.87 15.78
## 46 16.13 15.99 16.11 16.03 16.06 15.85 16.04 15.99
## 47 16.13 16.11 15.98 15.96 15.98 15.91 15.99 16.16
## 48 16.09 15.88 15.91 15.98 16.03 16.08 16.02 16.01
## 49 15.91 15.83 15.84 15.83 16.00 16.23 15.99 15.92
## 50 16.08 15.97 15.96 15.99 15.75 16.05 16.12 15.91
```

```r
head(magnets)
```

```text
##   score1 score2 change active
## 1     10      0     10    "1"
## 2     10      4      6    "1"
## 3      8      7      1    "1"
## 4     10      0     10    "1"
## 5     10      4      6    "1"
## 6     10      2      8    "1"
```

```r
tail(magnets)
```

```text
##    score1 score2 change active
## 45     10     10      0    "2"
## 46      9      9      0    "2"
## 47     10      9      1    "2"
## 48     10     10      0    "2"
## 49     10     10      0    "2"
## 50     10      9      1    "2"
```

```r
head(pop1)
```

```text
##        id    sex height
## 1 5696379 FEMALE    182
## 2 3019088   MALE    168
## 3 2038883   MALE    172
## 4 1920587 FEMALE    154
## 5 6006813   MALE    174
## 6 4055945 FEMALE    176
```

```r
tail(pop1)
```

```text
##             id    sex height
## 99995  5038824   MALE    181
## 99996  5647616 FEMALE    177
## 99997  1561921 FEMALE    161
## 99998  3553493   MALE    179
## 99999  9449207   MALE    170
## 100000 8286152 FEMALE    175
```

```r
head(pop2)
```

```text
##        id    sex age      bmi systolic diastolic  group
## 1 3695908 FEMALE  34 28.78903 112.5887  64.84949 NORMAL
## 2 5778095 FEMALE  33 18.91321 122.9261  78.71555 NORMAL
## 3 5138370   MALE  32 27.66339 128.3985  86.57248 NORMAL
## 4 2109892 FEMALE  35 26.30668 124.0975  79.18808 NORMAL
## 5 4132609 FEMALE  34 21.78160 121.3278  78.51906 NORMAL
## 6 9681961   MALE  29 28.90402 128.6520  85.01723 NORMAL
```

```r
tail(pop2)
```

```text
##             id    sex age      bmi systolic diastolic  group
## 99995  8378453   MALE  34 25.04188 126.0858  80.30195 NORMAL
## 99996  5344778 FEMALE  39 26.84842 129.6371  85.88189 NORMAL
## 99997  7902557 FEMALE  31 31.09695 121.6597  77.67906 NORMAL
## 99998  7118574 FEMALE  28 25.68135 124.1160  77.73954 NORMAL
## 99999  1838885   MALE  43 25.62096 112.0367  73.59764 NORMAL
## 100000 1100793 FEMALE  37 30.85461 140.6699 102.97422   HIGH
```

```r
head(pop3)
```

```text
##   type       time
## 1    b  0.1022744
## 2    b 22.1781342
## 3    c  9.5181055
## 4    a  4.0313741
## 5    b 24.0751296
## 6    c  9.1636315
```

```r
tail(pop3)
```

```text
##        type     time
## 99995     c 4.489552
## 99996     a 9.388816
## 99997     a 5.949696
## 99998     b 3.528619
## 99999     b 7.794870
## 100000    a 9.006003
```

```r
head(teacher)
```

```text
##   condition rating
## 1         P 2.6667
## 2         C 1.6667
## 3         P 2.0000
## 4         C 3.0000
## 5         C 1.6667
## 6         C 2.3333
```

```r
tail(teacher)
```

```text
##    condition rating
## 44         C 2.6667
## 45         P 2.0000
## 46         P 2.3333
## 47         P 2.3333
## 48         P 3.3333
## 49         C 2.3333
```

```r
head(transfusion)
```

```text
##   recency frequency monetary time march2007
## 1       2        50    12500   98       yes
## 2       0        13     3250   28       yes
## 3       1        16     4000   35       yes
## 4       2        20     5000   45       yes
## 5       1        24     6000   77        no
## 6       4         4     1000    4        no
```

```r
tail(transfusion)
```

```text
##     recency frequency monetary time march2007
## 743      16         3      750   86        no
## 744      23         2      500   38        no
## 745      21         2      500   52        no
## 746      23         3      750   62        no
## 747      39         1      250   39        no
## 748      72         1      250   72        no
```

```r
head(sleep_paired)
```

```text
##   drug1 drug2
## 1   0.7   1.9
## 2  -1.6   0.8
## 3  -0.2   1.1
## 4  -1.2   0.1
## 5  -0.1  -0.1
## 6   3.4   4.4
```

```r
tail(sleep_paired)
```

```text
##    drug1 drug2
## 5   -0.1  -0.1
## 6    3.4   4.4
## 7    3.7   5.5
## 8    0.8   1.6
## 9    0.0   4.6
## 10   2.0   3.4
```

```r
head(sleep_unpaired)
```

```text
##   group extra
## 1 drug1   0.7
## 2 drug1  -1.6
## 3 drug1  -0.2
## 4 drug1  -1.2
## 5 drug1  -0.1
## 6 drug1   3.4
```

```r
tail(sleep_unpaired)
```

```text
##    group extra
## 15 drug2  -0.1
## 16 drug2   4.4
## 17 drug2   5.5
## 18 drug2   1.6
## 19 drug2   4.6
## 20 drug2   3.4
```

```r
head(weapons)
```

```text
##   sex      aw      an      cw      cn
## 1   F 44.6667 44.0000 43.2409 45.1564
## 2   F 42.7083 43.7273 46.8628 45.1278
## 3   F 41.6957 41.8182 44.4939 43.3712
## 4   F 34.7778 37.1364 35.2715 34.4035
## 5   F 47.0833 44.3478 46.2482 46.3137
## 6   F 39.7727 41.7647 42.9762 42.1587
```

```r
tail(weapons)
```

```text
##    sex      aw      an      cw      cn
## 27   M 40.2174 41.1250 42.7546 42.9607
## 28   M 30.1176 34.4118 33.6941 31.9481
## 29   M 43.2500 42.6250 44.6222 44.6203
## 30   M 47.9048 49.1739 49.8551 49.8009
## 31   M 39.1304 38.0833 39.9209 39.7252
## 32   M 42.5217 46.0833 42.6268 42.7801
```
