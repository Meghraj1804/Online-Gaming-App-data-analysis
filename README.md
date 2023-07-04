**Title -- Gaming App Case Study**

**Overview - ABC** is a real-money online gaming company providing multiplayer games such as Ludo. An user can register as a player, deposit money in the platform and play games with other players on the platform. If he/she wins the game then they can withdraw the winning amount while the platform charges a nominal fee for the services.

**Problem Statements --**\
1.Calculating loyalty points\
2.How much bonus should be allocated to leaderboard players?
3.Would you say the loyalty point formula is fair or unfair?

**About Dataset --** In this dataset we have data about users play time, time and amount of deposit and withdrawal of money. In this dataset we have data of whole October month. We have total 1000 users data.

**Import Data --** In this dataset we have 3 different sub dataset. In first dataset contains data regarding users and number of games played and date time of each game, in second dataset information about deposit amount and date time of deposit, in third we have dataset regarding withdrawal amount and date time of transaction.

**Solution --**\
**Part A**\
**1.Calculating loyalty points**\
To calculate loyalty points we already have formula

**Loyalty Point=(0.01 * deposit)+(0.005 * Withdrawal amount)+(0.001 * (max(deposit-withdrawal) or 0))+(0.2 * Number of games played)**                                  


**Part B**\
**After calculating the loyalty points for the whole month find out which 50 players are at the top of the leaderboard. The company has allocated a pool of Rs. 50000 to be given away as bonus money to the loyal players. Now the company needs to determine how much bonus money should be given to the players. Should they base it on the amount of loyalty points? Should it be based on number of games? Or something else? That's for you to figure out. Suggest a suitable way to divide the allocated money keeping in mind the following points: Only top 50 ranked players are awarded bonus**
>
**Ans :- Bonus Calculation**\
I will suggest below formula for bonus calculation

 **((Company allocated pool \ No. of players (50))  X (Games Played * 0.011) X (Loyalty points * 0.001)) / (If withdrawal amount > 0 (Withdrawal amount \* 0.00035))**          

1. This formula is mainly based on \'Games Played\', \'Loyalty Points\' & \'Withdrawal Amount\'
2. According to this formula amount of bonus is directly proportional to the number of games played and loyalty points.
3. Bonus amount is inversely proportional to the amount of withdrawal.
4. Weightage given to the each parameter can be changed according to the market standards.

 
**Part C --**\
**Would you say the loyalty point formula is fair or unfair? Can you suggest any way to make the loyalty point formula more robust?**
>
**Suggestion :-** To calculate Loyalty the weightage given to the \'Withdrawal Amount\' is in \'Direct Proportion\'. But if we can see there are 17% of users are getting more money than the deposit amount and high loyalty points without playing average number of games. In this cases company is paying more money and giving more benefits based on loyalty points without getting more user traffic. To avoid this loyalty points should be in \'Inversely Proportional\' with withdrawal amount.

 **New formula for Loyalty points=((0.01*deposit amt)+(0.001*deposit times)+(0.2*games played))/((0.005*withdrawal amt)+(0.001*withdrawal times))**

