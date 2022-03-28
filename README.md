# knapsack_sa
    01 knapsack dealing with simulate annealing algorithm

# pseudocode

    while(T > T_min):
       x = 隨意設定一個取法
       loop:
         任意找一個鄰居y (可能高可能低)
         if y 較高 or random(0,1) < exp(-diff/k*T)
       return max of values

# process
1. 隨機一個重量<=capacity的解
2. 將此解輸出成01 bitstring, 0:物品有拿 1:物品沒拿

        ex: 10個物品,只有物品3有拿
        bitstring 為 0010000000
3. 溫度下降
        
        while(溫度還沒下降到指定溫度):
          隨機改變一個物品狀態從0->1 or 1->0
          if 新價值較高 or 機率符合條件:
             允許改變
             紀錄是否為最大價值
          溫度下降
