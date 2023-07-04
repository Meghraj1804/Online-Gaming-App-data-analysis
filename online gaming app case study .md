**Title -- Gaming App Case Study**

**Overview - ABC** is a real-money online gaming company providing
multiplayer games such as Ludo. An user can register as a player,
deposit money in the platform and play games with other players on the
platform. If he/she wins the game then they can withdraw the winning
amount while the platform charges a nominal fee for the services.

**Problem Statements --**\
1.Calculating loyalty points\
2.How much bonus should be allocated to leaderboard players?

> 3.Would you say the loyalty point formula is fair or unfair?

**About Dataset --** In this dataset we have data about users play time,
time and amount of deposit and withdrawal of money. In this dataset we
have data of whole October month. We have total 1000 users data.

**Import Data --** In this dataset we have 3 different sub dataset. In
first dataset contains data regarding users and number of games played
and date time of each game, in second dataset information about deposit
amount and date time of deposit, in third we have dataset regarding
withdrawal amount and date time of transaction.

**Solution --**\
**Part A**\
**1.Calculating loyalty points**\
To calculate loyalty points we already have formula

+-----------------------------------------------------------------------+
| > **Loyalty Point = ( 0.01 \* deposit ) + ( 0.005 \* Withdrawal       |
| > amount ) + ( 0.001 \* ( max ( #deposit - #withdrawal) or 0 ) ) + (  |
| > 0.2 \* Number of games played )**                                   |
+=======================================================================+
+-----------------------------------------------------------------------+

> **a.Player wise loyalty points for 2nd October Slot S1**

![](vertopal_65eabab59e3d44f1af7fc160d321cb6d/media/image1.png){width="7.638888888888889in"
height="2.9097222222222223in"}

> **b.Player wise loyalty points for 16th October Slot S2**

![](vertopal_65eabab59e3d44f1af7fc160d321cb6d/media/image2.png){width="7.673611111111111in"
height="2.5555555555555554in"}

> **c.Player wise loyalty points for 18th October Slot S1**

![](vertopal_65eabab59e3d44f1af7fc160d321cb6d/media/image3.png){width="7.625in"
height="2.9375in"}

> **d.Player wise loyalty points for 26th October Slot S2**

![](vertopal_65eabab59e3d44f1af7fc160d321cb6d/media/image4.png){width="7.625in"
height="3.076388888888889in"}

> **2.Calculate overall loyalty points earned and rank players on the
> basis of loyalty points in the month of October. In case of tie,
> number of games played should be taken as the next criteria for
> ranking.**

![](vertopal_65eabab59e3d44f1af7fc160d321cb6d/media/image5.png){width="7.722222222222222in"
height="3.6638888888888888in"}

> **3.What is the average deposit amount?**
>
> Average deposit amount is **Rs, 5,492.18**\
> **4.What is the average deposit amount per user in a month?**
>
> ![](vertopal_65eabab59e3d44f1af7fc160d321cb6d/media/image6.png){width="6.25in"
> height="3.5902777777777777in"}
>
> **5.What is the average number of games played per user?** Every
> player play 355 games per month.
>
> **Part B**\
> **After calculating the loyalty points for the whole month find out
> which 50 players are at the top of the leaderboard. The company has
> allocated a pool of Rs. 50000 to be given away as bonus money to the
> loyal players. Now the company needs to determine how much bonus money
> should be given to the players. Should they base it on the amount of
> loyalty points? Should it be based on number of games? Or something
> else? That's for you to figure out. Suggest a suitable way to divide
> the allocated money keeping in mind the following points: Only top 50
> ranked players are awarded bonus**
>
> **Ans :- Bonus Calculation**\
> I will suggest below formula for bonus calculation

+-----------------------------------------------------------------------+
| > **Company allocated pool**\                                         |
| > **\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_ X (Games Played \* |
| > 0.011) X (Loyalty points \* 0.001)**                                |
| >                                                                     |
| > **No. of players (50)**                                             |
| >                                                                     |
| > **\_\_\_\_\_\_\_\_                                                  |
| \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\ |
| _\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_** |
|                                                                       |
| **If withdrawal amount \> 0 (Withdrawal amount \* 0.00035)**          |
+=======================================================================+
+-----------------------------------------------------------------------+

> 1\. This formula is mainly based on \'Games Played\', \'Loyalty
> Points\' & \'Withdrawal Amount\' 2.According to this formula amount of
> bonus is directly proportional to the number of games played and
> loyalty points.
>
> 3.Bonus amount is inversely proportional to the amount of withdrawal.

4.Weightage given to the each parameter can be changed according to the
market standards.

  ---------------------------------------------------------------------------------------------------------------------------------------
  **User   **Games    **dep_amt**   **withdraw_amt**   **dep_times**   **withdraw_times**   **loyalty_points**   **rank**   **Bonus**
  ID**     Played**                                                                                                         
  -------- ---------- ------------- ------------------ --------------- -------------------- -------------------- ---------- -------------
  634      24         515000.0      15737705.0         8.0             67.0                 83843.39             1          4.018494

  99       10         1164800.0     2403141.0          47.0            15.0                 23665.75             2          3.095036

  672      10         2158700.0     233750.0           35.0            5.0                  22757.78             3          30.598696

  212      1          1924981.0     589850.0           26.0            4.0                  22199.29             4          1.182829

  740      2          1738490.0     365288.0           91.0            7.0                  19211.83             5          3.305887

  566      183        1819175.0     185071.0           53.0            3.0                  19153.76             6          595.239030

  714      6          1676300.0     0.0                34.0            0.0                  16764.23             7          1106.439180

  421      1557       878600.0      1269809.0          99.0            84.0                 15446.54             8          595.259131

  369      37         650000.0      1586208.0          13.0            9.0                  14438.45             9          10.584901

  30       13         1329000.0     152145.0           51.0            1.0                  14053.38             10         37.739062

  587      734        671700.0      1355000.0          89.0            8.0                  13638.89             11         232.199047

  222      10         1285000.0     99358.0            16.0            3.0                  13348.81             12         42.224484

  352      313        1083034.0     429518.0           128.0           8.0                  13040.66             13         298.666960
  ---------------------------------------------------------------------------------------------------------------------------------------

  -----------------------------------------------------------------------------------------
  365     3667    311000.0    1802335.0   10.0    33.0    12855.11   14      822.007597
  ------- ------- ----------- ----------- ------- ------- ---------- ------- --------------
  920     932     367700.0    1734480.0   41.0    52.0    12535.85   15      211.702040

  162     2       68320.0     2360000.0   7.0     23.0    12483.62   16      0.332494

  415     26      350000.0    1759843.0   6.0     6.0     12304.42   17      5.713276

  569     38      1227780.0   0.0         23.0    0.0     12285.42   18      5135.305560

  786     7       661500.0    1096160.0   27.0    11.0    12097.23   19      2.427922

  2       97      567000.0    1270215.0   20.0    20.0    12040.50   20      28.897725

  238     899     923400.0    445000.0    45.0    7.0     11638.84   21      738.982271

  992     2483    804978.0    616278.0    18.0    11.0    11627.79   22      1472.386665

  28      37      1061500.0   0.0         49.0    0.0     10622.45   23      4323.337150

  538     29      1025000.0   8558.0      27.0    1.0     10298.62   24      1096.804921

  208     507     644934.0    657928.0    35.0    9.0     9840.41    25      238.323805

  989     3471    240000.0    1339000.0   12.0    20.0    9789.22    26      797.529518

  978     74      794358.0    288114.0    69.0    14.0    9399.02    27      75.870784

  915     8       780028.0    307609.0    84.0    7.0     9340.01    28      7.634189

  678     12      379000.0    1100000.0   22.0    1.0     9292.42    29      3.185973

  78      602     159000.0    1484900.0   32.0    47.0    9134.95    30      116.393868

  909     1       679745.0    454060.0    125.0   5.0     9068.08    31      0.627663

  182     2446    795000.0    80339.0     16.0    4.0     8840.91    32      8459.635312

  93      487     616000.0    511474.0    76.0    24.0    8814.85    33      263.781884

  200     4       539998.0    593000.0    8.0     5.0     8365.79    34      1.773523

  259     126     824020.0    0.0         115.0   0.0     8265.52    35      11456.010720

  306     4       826000.0    0.0         57.0    0.0     8260.86    36      363.477840

  344     3       311900.0    1024000.0   18.0    10.0    8239.62    37      0.758670

  601     33      692144.0    240000.0    23.0    1.0     8128.06    38      35.124831

  515     413     580000.0    400000.0    14.0    6.0     7882.61    39      255.790694

  294     5       607700.0    311187.0    41.0    3.0     7633.98    40      3.854999

  681     8       689000.0    132000.0    65.0    1.0     7551.66    41      14.384114

  950     4       732000.0    35500.0     99.0    4.0     7498.40    42      26.553690

  675     639     662500.0    70000.0     50.0    1.0     7102.85    43      2037.793169

  663     6401    425000.0    290200.0    52.0    35.0    6981.25    44      4839.586431
  -----------------------------------------------------------------------------------------

  -------------------------------------------------------------------------------------
  438     1       400000.0   594851.0   2.0     1.0     6974.46   45      0.368491
  ------- ------- ---------- ---------- ------- ------- --------- ------- -------------
  619     2       697000.0   0.0        13.0    0.0     6970.41   46      153.349020

  245     3       209450.0   912200.0   25.0    10.0    6656.12   47      0.687982

  547     1248    493200.0   245863.0   41.0    14.0    6410.96   48      1022.749125

  612     1543    554800.0   109081.0   53.0    8.0     6402.06   49      2846.172356

  949     1       409100.0   434171.0   64.0    7.0     6262.12   50      0.453299
  -------------------------------------------------------------------------------------

> **Part C --**\
> **Would you say the loyalty point formula is fair or unfair? Can you
> suggest any way to make the loyalty point formula more robust?**
>
> **Suggestion :-** To calculate Loyalty the weightage given to the
> \'Withdrawal Amount\' is in \'Direct Proportion\'. But if we can see
> there are 17% of users are getting more money than the deposit amount
> and high loyalty points without playing average number of games. In
> this cases company is paying more money and giving more benefits based
> on loyalty points without getting more user traffic. To avoid this
> loyalty points should be in \'Inversely Proportional\' with withdrawal
> amount.

+-----------------------------------------------------------------------+
| **New formula for (0.01 \* deposit amt) + (0.001 \* deposit times) +  |
| (0.2 \* games played) Loyalty points =                                |
| \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\                     |
| _\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_** |
|                                                                       |
| **(0.005 \* withdrawal amt) + (0.001 \* withdrawal times)**           |
+=======================================================================+
+-----------------------------------------------------------------------+

> The list of top 10 users who withdraws more money than deposited and
> play less than average number of games and have high loyalty points

+--------+--------+--------+--------+--------+--------+--------+--------+
|        | *      | >      | **wi   | *      | **with | **loya | **ne   |
|        | *Games |  **dep | thdraw | *dep_t | draw_t | lty_po | w_loya |
|        | Pl     | _amt** | _amt** | imes** | imes** | ints** | lty_po |
|        | ayed** |        |        |        |        |        | ints** |
+========+========+========+========+========+========+========+========+
| *      | 24     | > 51   | 1573   | 8.0    | 67.0   | 83     | 0.     |
| *634** |        | 5000.0 | 7705.0 |        |        | 843.39 | 654540 |
+--------+--------+--------+--------+--------+--------+--------+--------+
| **99** | 10     | 116    | 240    | 47.0   | 15.0   | 23     | 9.     |
|        |        | 4800.0 | 3141.0 |        |        | 665.75 | 694138 |
+--------+--------+--------+--------+--------+--------+--------+--------+
| *      | 37     | > 65   | 158    | 13.0   | 9.0    | 14     | 8.     |
| *369** |        | 0000.0 | 6208.0 |        |        | 438.45 | 196572 |
+--------+--------+--------+--------+--------+--------+--------+--------+
| *      | 2      | 6      | 236    | 7.0    | 23.0   | 12     | 0.     |
| *162** |        | 8320.0 | 0000.0 |        |        | 483.62 | 579016 |
+--------+--------+--------+--------+--------+--------+--------+--------+
| *      | 26     | > 35   | 175    | 6.0    | 6.0    | 12     | 3.     |
| *415** |        | 0000.0 | 9843.0 |        |        | 304.42 | 978216 |
+--------+--------+--------+--------+--------+--------+--------+--------+
| *      | 7      | > 66   | 109    | 27.0   | 11.0   | 12     | 12.    |
| *786** |        | 1500.0 | 6160.0 |        |        | 097.23 | 069642 |
+--------+--------+--------+--------+--------+--------+--------+--------+
| **2**  | 97     | > 56   | 127    | 20.0   | 20.0   | 12     | 8.     |
|        |        | 7000.0 | 0215.0 |        |        | 040.50 | 930652 |
+--------+--------+--------+--------+--------+--------+--------+--------+
| *      | 12     | > 37   | 110    | 22.0   | 1.0    | 9      | 6.     |
| *678** |        | 9000.0 | 0000.0 |        |        | 292.42 | 891348 |
+--------+--------+--------+--------+--------+--------+--------+--------+
| *      | 4      | > 53   | 59     | 8.0    | 5.0    | 8      | 18.    |
| *200** |        | 9998.0 | 3000.0 |        |        | 365.79 | 212653 |
+--------+--------+--------+--------+--------+--------+--------+--------+
| *      | 3      | > 31   | 102    | 18.0   | 10.0   | 8      | 6.     |
| *344** |        | 1900.0 | 4000.0 |        |        | 239.62 | 091906 |
+--------+--------+--------+--------+--------+--------+--------+--------+
