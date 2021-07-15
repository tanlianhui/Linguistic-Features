# Explanations

## entity_count (result1)
Count how many entities there are in the context.

> Logistic Regression Model
>  
>  lrm(formula = isCorrect ~ entity_count, data = all_table, x = T, 
>      y = T)
>  
>                        Model Likelihood    Discrimination    Rank Discrim.    
>                              Ratio Test           Indexes          Indexes    
>  Obs           588    LR chi2     12.96    R2       0.032    C       0.579    
>   0            152    d.f.            5    g        0.331    Dxy     0.158    
>   1            436    Pr(> chi2) 0.0237    gr       1.392    gamma   0.261    
>  max |deriv| 0.001                         gp       0.061    tau-a   0.061    
>                                            Brier    0.187                     
>  
>                 Coef    S.E.    Wald Z Pr(>|Z|)
>  Intercept       1.3698  0.1434  9.55  <0.0001 
>  entity_count=1 -0.5698  0.2024 -2.82  0.0049  
>  entity_count=2 -0.5674  0.3633 -1.56  0.1183  
>  entity_count=3 -1.0333  0.6028 -1.71  0.0865  
>  entity_count=4 -0.6766  1.2331 -0.55  0.5832  
>  entity_count=5 -8.2753 31.6201 -0.26  0.7935  
>  
> entity_count=1 entity_count=2 entity_count=3 entity_count=4 entity_count=5 
>       1.114813       1.088053       1.031909       1.007573       1.000011

## word_count (result2)
Count how many words there are in the context. Without factorizing.

>Logistic Regression Model
 
> lrm(formula = isCorrect ~ word_count, data = all_table, x = T, 
>	  y = T)
> 
>                       Model Likelihood    Discrimination    Rank Discrim.    
>                             Ratio Test           Indexes          Indexes    
> Obs           588    LR chi2      0.17    R2       0.000    C       0.585    
>  0            152    d.f.            1    g        0.031    Dxy     0.170    
>  1            436    Pr(> chi2) 0.6758    gr       1.031    gamma   0.175    
> max |deriv| 2e-08                         gp       0.006    tau-a   0.065    
>                                           Brier    0.192                     
> 
>            Coef    S.E.   Wald Z Pr(>|Z|)
> Intercept   1.0908 0.1291  8.45  <0.0001 
> word_count -0.0017 0.0040 -0.42  0.6722 
>
> word_count 
>         1

## above43 (result3)
See if word count of a context exceeds 43, found by factorizing word_count and finding a gap between 43 and 44.

> Logistic Regression Model
>  
>  lrm(formula = isCorrect ~ above43, data = all_table, x = T, y = T)
>  
>                        Model Likelihood    Discrimination    Rank Discrim.    
>                              Ratio Test           Indexes          Indexes    
>  Obs           588    LR chi2      0.03    R2       0.000    C       0.502    
>   0            152    d.f.            1    g        0.010    Dxy     0.005    
>   1            436    Pr(> chi2) 0.8538    gr       1.010    gamma   0.030    
>  max |deriv| 4e-14                         gp       0.002    tau-a   0.002    
>                                            Brier    0.192                     
>  
>               Coef    S.E.   Wald Z Pr(>|Z|)
>  Intercept     1.0592 0.0988 10.72  <0.0001 
>  above43=TRUE -0.0607 0.3279 -0.19  0.8532  
>  
> above43=TRUE 
>            1

## ifQuestion (result4)
See if context contains rhetorical questions; only annotated ones are considered, while unannotated ones are zero-filled.

> Logistic Regression Model
>  
>  lrm(formula = isCorrect ~ ifQuestion, data = all_table, x = T, 
>      y = T)
>  
>                         Model Likelihood    Discrimination    Rank Discrim.    
>                               Ratio Test           Indexes          Indexes    
>  Obs           588    LR chi2      19.18    R2       0.047    C       0.523    
>   0            152    d.f.             1    g        0.212    Dxy     0.046    
   1            436    Pr(> chi2) <0.0001    gr       1.236    gamma   1.000    
>  max |deriv| 0.003                          gp       0.018    tau-a   0.018    
>                                             Brier    0.185                     
>  
>                  Coef    S.E.    Wald Z Pr(>|Z|)
>  Intercept        1.1009  0.0959 11.48  <0.0001 
>  ifQuestion=TRUE -9.0075 19.7017 -0.46  0.6475  
>  
> ifQuestion=TRUE 
>               1

## ifSign (result5)
See if context contains signs such as >=<^❤️🤔🤔🤣🥺😂.

> Logistic Regression Model
>  
>  lrm(formula = isCorrect ~ ifSign, data = all_table, x = T, y = T)
>  
>                        Model Likelihood    Discrimination    Rank Discrim.    
>                              Ratio Test           Indexes          Indexes    
>  Obs           588    LR chi2      0.80    R2       0.002    C       0.520    
>   0            152    d.f.            1    g        0.081    Dxy     0.040    
>   1            436    Pr(> chi2) 0.3716    gr       1.085    gamma   0.089    
>  max |deriv| 9e-11                         gp       0.015    tau-a   0.015    
>                                            Brier    0.191                     
>  
>              Coef   S.E.   Wald Z Pr(>|Z|)
>  Intercept   0.9929 0.1154 8.61   <0.0001 
>  ifSign=TRUE 0.1779 0.2001 0.89   0.3740  
>  
> ifSign=TRUE 
>           1

## adj_count (result6)
Count how many adjectives there are in the context.

> Logistic Regression Model
>  
>  lrm(formula = isCorrect ~ adj_count, data = all_table, x = T, 
>      y = T)
>  
>                        Model Likelihood    Discrimination    Rank Discrim.    
>                              Ratio Test           Indexes          Indexes    
>  Obs           588    LR chi2      9.69    R2       0.024    C       0.541    
   0            152    d.f.            4    g        0.244    Dxy     0.081    
>   1            436    Pr(> chi2) 0.0460    gr       1.277    gamma   0.192    
>  max |deriv| 0.002                         gp       0.031    tau-a   0.031    
>                                            Brier    0.189                     
>  
>              Coef    S.E.    Wald Z Pr(>|Z|)
>  Intercept    1.1421  0.1121 10.19  <0.0001 
>  adj_count=1 -0.2624  0.2210 -1.19  0.2352  
>  adj_count=2 -0.6313  0.5284 -1.19  0.2322  
>  adj_count=3  6.3975 25.0534  0.26  0.7985  
>  adj_count=5 -9.0487 36.8583 -0.25  0.8061  
>  
> adj_count=1 adj_count=2 adj_count=3 adj_count=5 
>    1.011716    1.011709    1.000006    1.000003

## ifSarcasm (result7)
See if context contains sarcasms; only annotated ones are considered, while unannotated ones are zero-filled.

> Logistic Regression Model
>  
>  lrm(formula = isCorrect ~ ifSarcasm, data = all_table, x = T, 
>      y = T)
>  
>                         Model Likelihood    Discrimination    Rank Discrim.    
>                               Ratio Test           Indexes          Indexes    
>  Obs           588    LR chi2      30.37    R2       0.074    C       0.536    
>   0            152    d.f.             1    g        0.369    Dxy     0.072    
   1            436    Pr(> chi2) <0.0001    gr       1.446    gamma   1.000    
>  max |deriv| 0.001                          gp       0.028    tau-a   0.028    
>                                             Brier    0.181                     
>  
>                 Coef     S.E.    Wald Z Pr(>|Z|)
>  Intercept        1.1289  0.0969 11.65  <0.0001 
>  ifSarcasm=TRUE -10.0358 25.9108 -0.39  0.6985  
>  
> ifSarcasm=TRUE 
>              1

## conj_count (result8)
Count how many conjunctives there are in the context.

> Logistic Regression Model
>  
>  lrm(formula = isCorrect ~ conj_count, data = all_table, x = T, 
>      y = T)
>  
>                        Model Likelihood    Discrimination    Rank Discrim.    
>                              Ratio Test           Indexes          Indexes    
>  Obs           588    LR chi2      2.75    R2       0.007    C       0.505    
>   0            152    d.f.            2    g        0.034    Dxy     0.010    
>   1            436    Pr(> chi2) 0.2530    gr       1.034    gamma   0.147    
>  max |deriv| 0.001                         gp       0.004    tau-a   0.004    
>                                            Brier    0.191                     
>  
>               Coef    S.E.    Wald Z Pr(>|Z|)
>  Intercept     1.0638  0.0960 11.08  <0.0001 
>  conj_count=1 -0.1083  0.5349 -0.20  0.8396  
>  conj_count=2 -7.9693 31.6199 -0.25  0.8010  
>  
> conj_count=1 conj_count=2 
>            1            1

## neg_count (result9)
Count how many negation words there are in the context.

> Logistic Regression Model
>  
>  lrm(formula = isCorrect ~ neg_count, data = all_table, x = T, 
>      y = T)
>  
>                        Model Likelihood    Discrimination    Rank Discrim.    
>                              Ratio Test           Indexes          Indexes    
>  Obs           588    LR chi2      5.28    R2       0.013    C       0.527    
>   0            152    d.f.            4    g        0.252    Dxy     0.054    
>   1            436    Pr(> chi2) 0.2597    gr       1.286    gamma   0.139    
>  max |deriv| 0.001                         gp       0.021    tau-a   0.021    
>                                            Brier    0.191                     
>  
>              Coef    S.E.    Wald Z Pr(>|Z|)
>  Intercept    1.0217  0.1078  9.48  <0.0001 
>  neg_count=1  0.1598  0.2450  0.65  0.5141  
>  neg_count=2 -0.3285  0.4462 -0.74  0.4616  
>  neg_count=3  7.5184 29.2057  0.26  0.7968  
>  neg_count=4  7.5184 71.5386  0.11  0.9163  
>  
> neg_count=1 neg_count=2 neg_count=3 neg_count=4 
>    1.011437    1.011434    1.000003    1.000001

## LRM result as a whole (result)

> Logistic Regression Model
>  
>  lrm(formula = isCorrect ~ entity_count + ifQuestion + ifSign + 
>      above43 + adj_count + ifSarcasm + conj_count + neg_count, 
>      data = all_table, x = T, y = T)
>  
>                          Model Likelihood    Discrimination    Rank Discrim.    
>                                Ratio Test           Indexes          Indexes    
>  Obs            588    LR chi2      81.30    R2       0.190    C       0.671    
>   0             152    d.f.            19    g        1.435    Dxy     0.342    
>   1             436    Pr(> chi2) <0.0001    gr       4.198    gamma   0.366    
>  max |deriv| 0.0006                          gp       0.131    tau-a   0.131    
>                                              Brier    0.165                     
>  
>                  Coef     S.E.     Wald Z Pr(>|Z|)
>  Intercept         1.5004   0.1954  7.68  <0.0001 
>  entity_count=1   -0.5464   0.2194 -2.49  0.0128  
>  entity_count=2   -0.6257   0.3981 -1.57  0.1161  
>  entity_count=3   -1.5442   0.6439 -2.40  0.0165  
>  entity_count=4   -1.8288   1.4580 -1.25  0.2097  
>  entity_count=5  -11.4123 141.6835 -0.08  0.9358  
>  ifQuestion=TRUE -11.2191  52.9817 -0.21  0.8323  
>  ifSign=TRUE       0.2251   0.2409  0.93  0.3501  
>  above43=TRUE      0.2721   0.4605  0.59  0.5546  
>  adj_count=1      -0.2386   0.2409 -0.99  0.3219  
>  adj_count=2      -0.4924   0.6183 -0.80  0.4258  
>  adj_count=3       7.5016  70.0928  0.11  0.9148  
>  adj_count=5     -11.2136 100.1861 -0.11  0.9109  
>  ifSarcasm=TRUE  -11.1634  42.1307 -0.26  0.7910  
>  conj_count=1     -0.4536   0.5606 -0.81  0.4184  
>  conj_count=2    -10.8477 141.6821 -0.08  0.9390  
>  neg_count=1       0.0433   0.2620  0.17  0.8686  
>  neg_count=2      -0.0654   0.5514 -0.12  0.9055  
>  neg_count=3       8.0921  44.9912  0.18  0.8573  
>  neg_count=4       1.8699 137.2068  0.01  0.9891  
>  
>  entity_count=1  entity_count=2  entity_count=3  entity_count=4  entity_count=5 
>        1.155084        1.126437        1.096799        1.054796        1.000025 
> ifQuestion=TRUE     ifSign=TRUE    above43=TRUE     adj_count=1     adj_count=2 
>        1.000003        1.197165        1.327884        1.054938        1.043982 
>     adj_count=3     adj_count=5  ifSarcasm=TRUE    conj_count=1    conj_count=2 
>        1.353272        1.000040        1.000006        1.029835        1.000004 
>     neg_count=1     neg_count=2     neg_count=3     neg_count=4 
>        1.026136        1.215459        1.000074        1.353315