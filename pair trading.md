# pair trading

1. Find Two Cointegrated Assets

2. Construct a new asset that is mean reverting

   + $p_{1,t}$:the log price of stock 1 at time t
   + $p_{2,t}$:the log price of stock 2 at time t
   + $r(h) = (p_{1,t+h}-p_{1,t})-\beta(p_{2,t+h}-p_{2,t})$
   + ​       $= EWC-\beta EWA$

3. Build a Trading Signal 

   + entry
     + when $w_t = \mu -\beta$， long stock 1, short $p*\beta$ stock 2
     + when $w_t = \mu + \beta$， short stock 1, long $p*\beta$ stock 2

   + exit

     + Exit when the Spread reaches the mean OR After holding for 6 months

   + profit

     + buying a spread $\Delta spread/cost = (spread_{exit}-spread_{entry})/(P_{ewc}+\beta/2*P_{ewa})$

     + selling a spread

        $\Delta spread/cost = -(spread_{exit}-spread_{entry})/(1/2*P_{ewc}+\beta P_{ewa})$

4. backtest

   