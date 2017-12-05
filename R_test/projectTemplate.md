Red Wine Analysis by R
================
Edwin
2017-10-30

单变量部分
==========

##### 下面显示该数据集的一些统计信息，如平均值、方差、最大、最小值等。

##### 这个数据集包括1599个样本，每个样本有13个特征变量。 quality这个变量分为0到10.共11个级别。0（非常差）和10（非常好）之间.数据类型都为数字型。

    ## 'data.frame':    1599 obs. of  13 variables:
    ##  $ X                   : int  1 2 3 4 5 6 7 8 9 10 ...
    ##  $ fixed.acidity       : num  7.4 7.8 7.8 11.2 7.4 7.4 7.9 7.3 7.8 7.5 ...
    ##  $ volatile.acidity    : num  0.7 0.88 0.76 0.28 0.7 0.66 0.6 0.65 0.58 0.5 ...
    ##  $ citric.acid         : num  0 0 0.04 0.56 0 0 0.06 0 0.02 0.36 ...
    ##  $ residual.sugar      : num  1.9 2.6 2.3 1.9 1.9 1.8 1.6 1.2 2 6.1 ...
    ##  $ chlorides           : num  0.076 0.098 0.092 0.075 0.076 0.075 0.069 0.065 0.073 0.071 ...
    ##  $ free.sulfur.dioxide : num  11 25 15 17 11 13 15 15 9 17 ...
    ##  $ total.sulfur.dioxide: num  34 67 54 60 34 40 59 21 18 102 ...
    ##  $ density             : num  0.998 0.997 0.997 0.998 0.998 ...
    ##  $ pH                  : num  3.51 3.2 3.26 3.16 3.51 3.51 3.3 3.39 3.36 3.35 ...
    ##  $ sulphates           : num  0.56 0.68 0.65 0.58 0.56 0.56 0.46 0.47 0.57 0.8 ...
    ##  $ alcohol             : num  9.4 9.8 9.8 9.8 9.4 9.4 9.4 10 9.5 10.5 ...
    ##  $ quality             : int  5 5 5 6 5 5 5 7 7 5 ...

    ##        X          fixed.acidity   volatile.acidity  citric.acid   
    ##  Min.   :   1.0   Min.   : 4.60   Min.   :0.1200   Min.   :0.000  
    ##  1st Qu.: 400.5   1st Qu.: 7.10   1st Qu.:0.3900   1st Qu.:0.090  
    ##  Median : 800.0   Median : 7.90   Median :0.5200   Median :0.260  
    ##  Mean   : 800.0   Mean   : 8.32   Mean   :0.5278   Mean   :0.271  
    ##  3rd Qu.:1199.5   3rd Qu.: 9.20   3rd Qu.:0.6400   3rd Qu.:0.420  
    ##  Max.   :1599.0   Max.   :15.90   Max.   :1.5800   Max.   :1.000  
    ##  residual.sugar     chlorides       free.sulfur.dioxide
    ##  Min.   : 0.900   Min.   :0.01200   Min.   : 1.00      
    ##  1st Qu.: 1.900   1st Qu.:0.07000   1st Qu.: 7.00      
    ##  Median : 2.200   Median :0.07900   Median :14.00      
    ##  Mean   : 2.539   Mean   :0.08747   Mean   :15.87      
    ##  3rd Qu.: 2.600   3rd Qu.:0.09000   3rd Qu.:21.00      
    ##  Max.   :15.500   Max.   :0.61100   Max.   :72.00      
    ##  total.sulfur.dioxide    density             pH          sulphates     
    ##  Min.   :  6.00       Min.   :0.9901   Min.   :2.740   Min.   :0.3300  
    ##  1st Qu.: 22.00       1st Qu.:0.9956   1st Qu.:3.210   1st Qu.:0.5500  
    ##  Median : 38.00       Median :0.9968   Median :3.310   Median :0.6200  
    ##  Mean   : 46.47       Mean   :0.9967   Mean   :3.311   Mean   :0.6581  
    ##  3rd Qu.: 62.00       3rd Qu.:0.9978   3rd Qu.:3.400   3rd Qu.:0.7300  
    ##  Max.   :289.00       Max.   :1.0037   Max.   :4.010   Max.   :2.0000  
    ##     alcohol         quality     
    ##  Min.   : 8.40   Min.   :3.000  
    ##  1st Qu.: 9.50   1st Qu.:5.000  
    ##  Median :10.20   Median :6.000  
    ##  Mean   :10.42   Mean   :5.636  
    ##  3rd Qu.:11.10   3rd Qu.:6.000  
    ##  Max.   :14.90   Max.   :8.000

#### 单变量图表部分

##### 葡萄酒的品质分布并不均匀，普通品质的葡萄酒占大多数，品质高的和差的葡萄酒占少数.

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-2-1.png)

##### 固定酸度的均值在8左右，但有一些离群值。

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-3-1.png)

##### 酒精度基本都在14以下。有少量的离群值。最大约为14.8

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-4-1.png)

##### 醋酸的分布。最高值为0.6

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-5-1.png)

##### 柠檬酸的分布. 发现一些数据为0，从CSV文件中也能看到一些为0的值。估计数据采集不完整

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-6-1.png)

##### 剩余糖分的统计图. 有很多的离群值。分布也很不均匀

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-7-1.png)

##### 氯化物统计图. 同样有有很多的离群值。

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-8-1.png)

##### 游离二氧化硫的统计图。数据分布不均匀。

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-9-1.png)

##### 密度的统计图. 类似一个正态分布

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-10-1.png)

##### 总二氧化硫统计图 和游离二氧化硫（free.sulfur.dioxide）的分布差不多，也有较多的离群值。

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-11-1.png)

##### 硫酸盐的统计图 存在较多的离群值。数据分布不均匀。

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-12-1.png)

##### PH值的分布类似一个正态分布

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-13-1.png)

单变量分析
==========

### 数据集结构

#### 这个数据集包括1599个样本，每个样本有13个特征变量。 quality这个变量分为0到10.共11个级别。0（非常差）和10（非常好）之间.数据类型都为数字型。

### 以下是对每个特征变量的解释：

#### 1 - fixed acidity: most acids involved with wine or fixed or nonvolatile (do not evaporate readily)

#### 固定的酸度:与葡萄酒或固定或不挥发性有关的大多数酸(不容易挥发)

#### 2 - volatile acidity: the amount of acetic acid in wine, which at too high of levels can lead to an unpleasant, vinegar taste

#### 葡萄酒中醋酸的含量过高会导致不愉快的醋味

#### 3 - citric acid: found in small quantities, citric acid can add 'freshness' and flavor to wines

#### 少量的柠檬酸可以给葡萄酒添加新鲜感和风味

#### 4 - residual sugar: the amount of sugar remaining after fermentation stops, it's rare to find wines with less than 1 gram/liter and wines with greater than 45 grams/liter are considered sweet

#### 剩余糖分:发酵后残留的糖量，很少能发现含有少于1克/升的葡萄酒和大于45克/升的葡萄酒被认为是甜的

#### 5 - chlorides: the amount of salt in the wine

#### 氯化物:葡萄酒中的盐含量

#### 6 - free sulfur dioxide: the free form of SO2 exists in equilibrium between molecular SO2 (as a dissolved gas) and bisulfite ion; it prevents microbial growth and the oxidation of wine

#### 游离二氧化硫:SO2的自由形式存在于分子SO2(as a溶解气体)和bisulfite离子之间的平衡;它可以防止微生物的生长和葡萄酒的氧化

#### 7 - total sulfur dioxide: amount of free and bound forms of S02; in low concentrations, SO2 is mostly undetectable in wine, but at free SO2 concentrations over 50 ppm, SO2 becomes evident in the nose and taste of wine

#### 总二氧化硫:S02的自由和束缚形式;在低浓度下，SO2在葡萄酒中是无法检测的，但在自由SO2浓度超过50ppm的情况下，SO2在鼻子和葡萄酒的味道中变得明显

#### 8 - density: the density of water is close to that of water depending on the percent alcohol and sugar content

#### 密度:水的密度与水的密度接近，这取决于酒精和糖的含量

#### 9 - pH: describes how acidic or basic a wine is on a scale from 0 (very acidic) to 14 (very basic); most wines are between 3-4 on the pH scale

#### 描述一种葡萄酒的酸性或碱性从0(非常酸)到14(非常基本);大多数葡萄酒的pH值在3 - 4之间

#### 10 - sulphates: a wine additive which can contribute to sulfur dioxide gas (S02) levels, wich acts as an antimicrobial and antioxidant

#### 硫酸盐:一种能促进二氧化硫(S02)水平的葡萄酒添加剂，它是一种抗菌剂和抗氧化剂

#### 11 - alcohol: the percent alcohol content of the wine

#### 酒精:酒的酒精含量百分比

### （一）

##### 整个数据集变量两两之间的的相关性预览。从结果中可以初步看出如下几个相关性较强的特征，包含正相关或负相关。注：相关系数：两组不同数据的相关程度，取值范围\[-1，1\]，越接近0越不相关。

``` r
cor_data <- cor(
  redwine 
)
pandoc.table(cor_data)
```

    ## 
    ## -------------------------------------------------------------------------
    ##           &nbsp;                X       fixed.acidity   volatile.acidity 
    ## -------------------------- ----------- --------------- ------------------
    ##           **X**                 1          -0.2685         -0.008815     
    ## 
    ##     **fixed.acidity**        -0.2685          1             -0.2561      
    ## 
    ##    **volatile.acidity**     -0.008815      -0.2561             1         
    ## 
    ##      **citric.acid**         -0.1536       0.6717           -0.5525      
    ## 
    ##     **residual.sugar**      -0.03126       0.1148           0.001918     
    ## 
    ##       **chlorides**          -0.1199       0.09371           0.0613      
    ## 
    ##  **free.sulfur.dioxide**     0.09048       -0.1538          -0.0105      
    ## 
    ##  **total.sulfur.dioxide**    -0.1178       -0.1132          0.07647      
    ## 
    ##        **density**           -0.3684        0.668           0.02203      
    ## 
    ##           **pH**              0.136        -0.683            0.2349      
    ## 
    ##       **sulphates**          -0.1253        0.183            -0.261      
    ## 
    ##        **alcohol**           0.2451       -0.06167          -0.2023      
    ## 
    ##        **quality**           0.06645       0.1241           -0.3906      
    ## -------------------------------------------------------------------------
    ## 
    ## Table: Table continues below
    ## 
    ##  
    ## ---------------------------------------------------------------------
    ##           &nbsp;            citric.acid   residual.sugar   chlorides 
    ## -------------------------- ------------- ---------------- -----------
    ##           **X**               -0.1536        -0.03126       -0.1199  
    ## 
    ##     **fixed.acidity**         0.6717          0.1148        0.09371  
    ## 
    ##    **volatile.acidity**       -0.5525        0.001918       0.0613   
    ## 
    ##      **citric.acid**             1            0.1436        0.2038   
    ## 
    ##     **residual.sugar**        0.1436            1           0.05561  
    ## 
    ##       **chlorides**           0.2038         0.05561           1     
    ## 
    ##  **free.sulfur.dioxide**     -0.06098         0.187        0.005562  
    ## 
    ##  **total.sulfur.dioxide**     0.03553         0.203         0.0474   
    ## 
    ##        **density**            0.3649          0.3553        0.2006   
    ## 
    ##           **pH**              -0.5419        -0.08565       -0.265   
    ## 
    ##       **sulphates**           0.3128         0.005527       0.3713   
    ## 
    ##        **alcohol**            0.1099         0.04208        -0.2211  
    ## 
    ##        **quality**            0.2264         0.01373        -0.1289  
    ## ---------------------------------------------------------------------
    ## 
    ## Table: Table continues below
    ## 
    ##  
    ## -----------------------------------------------------------------------
    ##           &nbsp;            free.sulfur.dioxide   total.sulfur.dioxide 
    ## -------------------------- --------------------- ----------------------
    ##           **X**                   0.09048               -0.1178        
    ## 
    ##     **fixed.acidity**             -0.1538               -0.1132        
    ## 
    ##    **volatile.acidity**           -0.0105               0.07647        
    ## 
    ##      **citric.acid**             -0.06098               0.03553        
    ## 
    ##     **residual.sugar**             0.187                 0.203         
    ## 
    ##       **chlorides**              0.005562                0.0474        
    ## 
    ##  **free.sulfur.dioxide**             1                   0.6677        
    ## 
    ##  **total.sulfur.dioxide**         0.6677                   1           
    ## 
    ##        **density**               -0.02195               0.07127        
    ## 
    ##           **pH**                  0.07038               -0.06649       
    ## 
    ##       **sulphates**               0.05166               0.04295        
    ## 
    ##        **alcohol**               -0.06941               -0.2057        
    ## 
    ##        **quality**               -0.05066               -0.1851        
    ## -----------------------------------------------------------------------
    ## 
    ## Table: Table continues below
    ## 
    ##  
    ## ----------------------------------------------------------------------------------
    ##           &nbsp;            density       pH      sulphates   alcohol    quality  
    ## -------------------------- ---------- ---------- ----------- ---------- ----------
    ##           **X**             -0.3684     0.136      -0.1253     0.2451    0.06645  
    ## 
    ##     **fixed.acidity**        0.668      -0.683      0.183     -0.06167    0.1241  
    ## 
    ##    **volatile.acidity**     0.02203     0.2349     -0.261     -0.2023    -0.3906  
    ## 
    ##      **citric.acid**         0.3649    -0.5419     0.3128      0.1099     0.2264  
    ## 
    ##     **residual.sugar**       0.3553    -0.08565   0.005527    0.04208    0.01373  
    ## 
    ##       **chlorides**          0.2006     -0.265     0.3713     -0.2211    -0.1289  
    ## 
    ##  **free.sulfur.dioxide**    -0.02195   0.07038     0.05166    -0.06941   -0.05066 
    ## 
    ##  **total.sulfur.dioxide**   0.07127    -0.06649    0.04295    -0.2057    -0.1851  
    ## 
    ##        **density**             1       -0.3417     0.1485     -0.4962    -0.1749  
    ## 
    ##           **pH**            -0.3417       1        -0.1966     0.2056    -0.05773 
    ## 
    ##       **sulphates**          0.1485    -0.1966        1       0.09359     0.2514  
    ## 
    ##        **alcohol**          -0.4962     0.2056     0.09359       1        0.4762  
    ## 
    ##        **quality**          -0.1749    -0.05773    0.2514      0.4762       1     
    ## ----------------------------------------------------------------------------------

#### 1.葡萄酒的品质和alcohol、volatile acidity、sulphates以及citric.acid有比较大的相关性。这个需要在后面的双变量中逐个分析

#### 2. free.sulfur.dioxide和 total.sulfur.dioxide 之间相关性强，这个显而易见，total.sulfur.dioxide中包含free.sulfur.dioxide的含量。所以当free.sulfur.dioxide含量增加时，总的含量自然也会增加，

#### 3. PH值与fixed.acidity、citric.acid、density有较强的相关性。需要在后面的双变量逐个分析。

#### 4. density 与fixed.acidity有很强的相关性（相关系数为0.668）

### （二）

#### 从前面初步分析，在这个数据集中，有如下几个重要的特征变量：

#### 1. quality 代表葡萄酒的品质

#### 2. alcohol 代表酒精含量

#### 3. fixed.acidity 代表固定酸度含量

#### 4. citric.acid 代表柠檬酸的含量

#### 5. PH 代表酸碱值

#### 6. volatile.acidity 代表醋酸的含量

#### 7. density 代表密度值

### （三）

#### 通过观察各个特征变量的箱线图，发现residual.sugar、chlorides、sulphates有大量的离群值存在。

#### Citric acid 存在很多0值。估计是收集数据时丢失该值或者本身就是错误的数据。

双变量部分
==========

### 根据上面确定的7个重要的特征变量，先分析一下其中6个与葡萄酒品质之间的关系图：

##### 下图显示的是alcohol（酒精）含量和品质的箱线图，从图中可以看出，葡萄酒的品质随着酒精度的增加而提升。（相关系数为0.4762 ）

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-15-1.png)

##### 下图显示的是citric.acid（柠檬酸）的含量与品质的箱线图，从图中可以看出，葡萄酒的品质随着citric.acid的增加而提升。（相关系数为0.2264）

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-16-1.png)

##### 下图显示的是volatile.acidity（醋酸）的含量与品质的箱线图，从图中可以看出，葡萄酒的品质随着volatile.acidity的增加而降低。说明对葡萄酒的品质有负面的影响。从相关性分析也能看出，这两个特征变量的相关系数是负的（-0.3906）。

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-17-1.png)

##### 下面显示的是fixed.acidity（固定的酸度）的含量与品质的箱线图，从图中可以看出，他们之间的相关性低，随着fixed.acidity的增加，品质提升不大。（相关性系数为0.1241）

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-18-1.png)

##### 下面显示的是sulphates（硫酸盐）的含量与品质的箱线图，品质好的葡萄酒有高的sulphates值。（相关性系数为0.2514）

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-19-1.png)

##### 下面显示的是density（密度）的含量与品质的箱线图，从图中可以看出，品质好的有低的密度，可能是由于较高的酒精度所导致。（相关性系数为-0.1749）

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-20-1.png)

##### 下面显示的是PH（酸碱值）的含量与品质的箱线图，品质高的葡萄酒的PH值低。（相关性系数为-0.05773）

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-21-1.png)

##### 下面显示的是 density（密度） 与fixed.acidity（固定酸度） 的箱线图，随着固定酸度的增加，密度也会增加。（相关性系数为0.668）。这也说明，fixed.acidity对品质影响不大，因为品质好的葡萄酒有低的密度，

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-22-1.png)

##### 下面显示的是 density（密度） 与alcohol（酒精度） 的箱线图，随着alcohol的增加，密度会减少。（相关性系数为-0.4962）。这也说明，alcohol对品质影响大，因为品质好的葡萄酒有较高的酒精度。这和前面的分析是一致的。

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-23-1.png)

### 下面分析一下PH值与各种酸度之间的关系图。因为化学知识告诉我们，PH值代表的就是酸碱值，所以有必要看一下它们之间的关系。

##### 下图显示fixed.acidity（固定酸度）与PH值之间的趋势关系图。可以看出随着固定酸度的增加，PH变小，

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-24-1.png)

##### 下图显示citric.acid（柠檬酸）与PH值之间的趋势关系图。可以看出随着citric.acid的增加，PH变小，

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-25-1.png)

##### 下图显示volatile.acidity（醋酸）与PH值之间的趋势关系图。可以看出随着volatile.acidity的增加，PH却反而变大，由于醋酸是葡萄酒中唯一具有挥发性的有机酸，正是由于这种特性导致PH反而变大。

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-26-1.png)

双变量分析
==========

### （一）

#### 影响葡萄酒品质的特征变量有如下：

#### 1 alcohol（酒精度）

#### 2 volatile.acidity（醋酸）

#### 3 citric.acid（柠檬酸）

#### 4 sulphates（硫酸盐）

#### 更好的葡萄酒似乎有更高的酒精含量。但是还会受到其他因素的影响，比如醋酸的含量。

#### 更好的葡萄酒似乎有较低的密度。可能是由于它们含有较高的酒精含量。

#### 更好的葡萄酒似乎更酸。

### （二）

#### 醋酸的含量变大时，PH值反而也会变大，这是由于醋酸是葡萄酒中唯一具有挥发性的有机酸，对PH值有逆转的作用，这一点从趋势图中也得到验证。

### （三）

#### 1. density 与fixed.acidity有最强的相关性（相关系数为0.668）

#### 2. 葡萄酒的品质和alcohol有最强的相关性，（相关系数为0.4762）

#### 3. alcohol（酒精度）和density（密度）之间有最强的负相关性 （相关系数为-0.4962）

多变量部分
==========

#### 下面显示醋酸、酒精度和葡萄酒的品质之间的关系。说明醋酸起到反作用，挥发性酸浓度越低，酒精浓度越高，葡萄酒就越好。

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-27-1.png)

#### 下面显示醋酸、柠檬酸和葡萄酒的品质之间的关系。说明醋酸浓度越低，柠檬酸浓度越高，葡萄酒就越好。

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-28-1.png)

#### 下面显示硫酸盐、酒精度和葡萄酒的品质之间的关系。说明硫酸盐含量高，酒精浓度越高，葡萄酒就越好。

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-29-1.png)

多变量分析
==========

#### 1. 酒精含量高和硫酸盐的含量似乎能产生更好的葡萄酒。

#### 2. 柠檬酸虽然弱相关，但在提高葡萄酒质量方面起着重要作用。

总结及图表
==========

#### 第一张图

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-30-1.png)

##### 上面是alcohol（酒精）含量和品质的箱线图，从图中可以看出，葡萄酒的品质随着酒精度的增加而提升。（相关系数为0.4762 ），酒精的含量起到了很大的作用，但从前面的分析来看，这并不是影响酒的品质的唯一因素。

#### 第二张图

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-31-1.png)

##### 上面显示硫酸盐、酒精度和葡萄酒的品质之间的关系。可以看出好的葡萄酒对酒精含量和硫酸盐浓度都有很高的要求，这意味着高酒精含量和高硫酸盐浓度会产生更好的葡萄酒。

#### 第三张图

![](projectTemplate_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-32-1.png)

##### 上面显示volatile.acidity（醋酸）与PH值之间的趋势关系图。可以看出随着volatile.acidity的增加，PH却反而变大，由于醋酸是葡萄酒中唯一具有挥发性的有机酸，正是由于这种特性导致PH反而变大。

反思
====

#### 首先确定分析的目标，就是要看哪些特征变量会影响红葡萄酒的品质。第一步先分析了单个不同变量与品质之间的关系，观察每个特征对品质的影响，最终选择酒精度、硫酸盐、柠檬酸和醋酸四个特征值。 然后又分析了PH值和各种酸之间的关系，发现醋酸具有反向逆转的特性，这和它是挥发性酸的特性有关。接着又分析了多个变量之间的关系，发现密度对品质的影响不是很大，醋酸对品质有反向影响。柠檬酸虽然相关系数不大，属于弱相关，但是对品质影响还是比较大的，所以最后确定对红酒品质影响的三个特征变量：酒精含量、柠檬酸含量以及硫酸盐的含量。这些值越高，越能酿出高品质的红葡萄酒。

#### 对于数据集，我觉得还应该加上红酒的外观特征作为变量，用于进一步的分析，比如香气、颜色、口味等。这些感官上的特征也会对定位红酒的品质起到作用。
