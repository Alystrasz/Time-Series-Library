# Long-term forecast (ECL script)

## Vanilla performances

* mse:0.2044449895620346
* mae:0.30834755301475525
* dtw:not calculated

<details>
  <summary>Log</summary>
  
```text
(Time-Series-Library) remy@chimay:~/Travail/Time-Series-Library$ ./scripts/long_term_forecast/ECL_script/FLI_TSMixer.sh 
False
Args in experiment:
Basic Config
  Task Name:          long_term_forecast  Is Training:        1                   
  Model ID:           ECL_96_96           Model:              TSMixer             

Data Loader
  Data:               custom              Root Path:          ./dataset/electricity/
  Data Path:          electricity.csv     Features:           M                   
  Target:             OT                  Freq:               h                   
  Checkpoints:        ./checkpoints/      

Forecasting Task
  Seq Len:            96                  Label Len:          96                  
  Pred Len:           96                  Seasonal Patterns:  Monthly             
  Inverse:            0                   

Model Parameters
  Top k:              5                   Num Kernels:        6                   
  Enc In:             321                 Dec In:             321                 
  C Out:              321                 d model:            256                 
  n heads:            8                   e layers:           2                   
  d layers:           1                   d FF:               512                 
  Moving Avg:         25                  Factor:             3                   
  Distil:             1                   Dropout:            0.1                 
  Embed:              timeF               Activation:         gelu                

Run Parameters
  Num Workers:        10                  Itr:                1                   
  Train Epochs:       10                  Batch Size:         32                  
  Patience:           3                   Learning Rate:      0.0001              
  Des:                Exp                 Loss:               MSE                 
  Lradj:              type1               Use Amp:            0                   

GPU
  Use GPU:            0                   GPU:                0                   
  Use Multi GPU:      0                   Devices:            0,1,2,3             

De-stationary Projector Params
  P Hidden Dims:      128, 128            P Hidden Layers:    2                   

Compression Params
  Use ratio removal   False
  Use FLI             False

Use CPU
>>>>>>>start training : long_term_forecast_ECL_96_96_TSMixer_custom_ftM_sl96_ll96_pl96_dm256_nh8_el2_dl1_df512_expand2_dc4_fc3_ebtimeF_dtTrue_Exp_0>>>>>>>>>>>>>>>>>>>>>>>>>>
train 18221
val 2537
test 5165
        iters: 100, epoch: 1 | loss: 0.4674883
        speed: 0.1053s/iter; left time: 590.0286s
        iters: 200, epoch: 1 | loss: 0.3289016
        speed: 0.0970s/iter; left time: 533.5125s
        iters: 300, epoch: 1 | loss: 0.2836778
        speed: 0.1027s/iter; left time: 554.6274s
        iters: 400, epoch: 1 | loss: 0.2695191
        speed: 0.1007s/iter; left time: 533.5745s
        iters: 500, epoch: 1 | loss: 0.2393331
        speed: 0.1070s/iter; left time: 556.4313s
Epoch: 1 cost time: 58.612401247024536
Epoch: 1, Steps: 570 | Train Loss: 0.3951464 Vali Loss: 0.2105665 Test Loss: 0.2422090
Validation loss decreased (inf --> 0.210567).  Saving model ...
Updating learning rate to 0.0001
        iters: 100, epoch: 2 | loss: 0.2209990
        speed: 0.2867s/iter; left time: 1442.3997s
        iters: 200, epoch: 2 | loss: 0.2140102
        speed: 0.0981s/iter; left time: 483.6205s
        iters: 300, epoch: 2 | loss: 0.2169814
        speed: 0.0974s/iter; left time: 470.3618s
        iters: 400, epoch: 2 | loss: 0.1929994
        speed: 0.0989s/iter; left time: 467.8589s
        iters: 500, epoch: 2 | loss: 0.1877348
        speed: 0.0989s/iter; left time: 458.1167s
Epoch: 2 cost time: 56.73772835731506
Epoch: 2, Steps: 570 | Train Loss: 0.2169860 Vali Loss: 0.1848402 Test Loss: 0.2200755
Validation loss decreased (0.210567 --> 0.184840).  Saving model ...
Updating learning rate to 5e-05
        iters: 100, epoch: 3 | loss: 0.1954286
        speed: 0.2739s/iter; left time: 1221.8609s
        iters: 200, epoch: 3 | loss: 0.1965872
        speed: 0.0971s/iter; left time: 423.6187s
        iters: 300, epoch: 3 | loss: 0.2086575
        speed: 0.0977s/iter; left time: 416.2981s
        iters: 400, epoch: 3 | loss: 0.1877694
        speed: 0.1183s/iter; left time: 492.3188s
        iters: 500, epoch: 3 | loss: 0.1980827
        speed: 0.1494s/iter; left time: 606.5134s
Epoch: 3 cost time: 65.92135500907898
Epoch: 3, Steps: 570 | Train Loss: 0.1928099 Vali Loss: 0.1765225 Test Loss: 0.2120705
Validation loss decreased (0.184840 --> 0.176523).  Saving model ...
Updating learning rate to 2.5e-05
        iters: 100, epoch: 4 | loss: 0.1729229
        speed: 0.3334s/iter; left time: 1297.1749s
        iters: 200, epoch: 4 | loss: 0.1746062
        speed: 0.1086s/iter; left time: 411.7813s
        iters: 300, epoch: 4 | loss: 0.1821091
        speed: 0.1162s/iter; left time: 428.7509s
        iters: 400, epoch: 4 | loss: 0.1677316
        speed: 0.1093s/iter; left time: 392.4524s
        iters: 500, epoch: 4 | loss: 0.1806628
        speed: 0.1072s/iter; left time: 374.2110s
Epoch: 4 cost time: 63.49603509902954
Epoch: 4, Steps: 570 | Train Loss: 0.1822537 Vali Loss: 0.1715803 Test Loss: 0.2089733
Validation loss decreased (0.176523 --> 0.171580).  Saving model ...
Updating learning rate to 1.25e-05
        iters: 100, epoch: 5 | loss: 0.1744271
        speed: 0.3805s/iter; left time: 1263.7702s
        iters: 200, epoch: 5 | loss: 0.1764892
        speed: 0.1495s/iter; left time: 481.5198s
        iters: 300, epoch: 5 | loss: 0.1921225
        speed: 0.1368s/iter; left time: 426.9026s
        iters: 400, epoch: 5 | loss: 0.1667290
        speed: 0.1294s/iter; left time: 390.8630s
        iters: 500, epoch: 5 | loss: 0.1856193
        speed: 0.1096s/iter; left time: 320.0220s
Epoch: 5 cost time: 76.93206429481506
Epoch: 5, Steps: 570 | Train Loss: 0.1765075 Vali Loss: 0.1693838 Test Loss: 0.2068693
Validation loss decreased (0.171580 --> 0.169384).  Saving model ...
Updating learning rate to 6.25e-06
        iters: 100, epoch: 6 | loss: 0.1920113
        speed: 0.3129s/iter; left time: 860.6637s
        iters: 200, epoch: 6 | loss: 0.1676178
        speed: 0.1116s/iter; left time: 295.8126s
        iters: 300, epoch: 6 | loss: 0.1818456
        speed: 0.1062s/iter; left time: 271.0309s
        iters: 400, epoch: 6 | loss: 0.1872687
        speed: 0.1042s/iter; left time: 255.4944s
        iters: 500, epoch: 6 | loss: 0.1649491
        speed: 0.1149s/iter; left time: 270.1389s
Epoch: 6 cost time: 63.19079637527466
Epoch: 6, Steps: 570 | Train Loss: 0.1734690 Vali Loss: 0.1678917 Test Loss: 0.2057300
Validation loss decreased (0.169384 --> 0.167892).  Saving model ...
Updating learning rate to 3.125e-06
        iters: 100, epoch: 7 | loss: 0.1693511
        speed: 0.3387s/iter; left time: 738.7349s
        iters: 200, epoch: 7 | loss: 0.1638902
        speed: 0.1186s/iter; left time: 246.7732s
        iters: 300, epoch: 7 | loss: 0.1652060
        speed: 0.1258s/iter; left time: 249.2617s
        iters: 400, epoch: 7 | loss: 0.1668597
        speed: 0.1025s/iter; left time: 192.8577s
        iters: 500, epoch: 7 | loss: 0.1660767
        speed: 0.1011s/iter; left time: 180.0048s
Epoch: 7 cost time: 65.82343053817749
Epoch: 7, Steps: 570 | Train Loss: 0.1718821 Vali Loss: 0.1672405 Test Loss: 0.2052243
Validation loss decreased (0.167892 --> 0.167240).  Saving model ...
Updating learning rate to 1.5625e-06
        iters: 100, epoch: 8 | loss: 0.1752539
        speed: 0.2927s/iter; left time: 471.5086s
        iters: 200, epoch: 8 | loss: 0.1560079
        speed: 0.1315s/iter; left time: 198.6786s
        iters: 300, epoch: 8 | loss: 0.1620845
        speed: 0.1075s/iter; left time: 151.7260s
        iters: 400, epoch: 8 | loss: 0.1712993
        speed: 0.1088s/iter; left time: 142.6167s
        iters: 500, epoch: 8 | loss: 0.1601523
        speed: 0.1026s/iter; left time: 124.2224s
Epoch: 8 cost time: 63.63207030296326
Epoch: 8, Steps: 570 | Train Loss: 0.1710863 Vali Loss: 0.1668426 Test Loss: 0.2049192
Validation loss decreased (0.167240 --> 0.166843).  Saving model ...
Updating learning rate to 7.8125e-07
        iters: 100, epoch: 9 | loss: 0.1695109
        speed: 0.2857s/iter; left time: 297.3680s
        iters: 200, epoch: 9 | loss: 0.1856228
        speed: 0.1046s/iter; left time: 98.4667s
        iters: 300, epoch: 9 | loss: 0.1771875
        speed: 0.1025s/iter; left time: 86.1696s
        iters: 400, epoch: 9 | loss: 0.1716313
        speed: 0.1017s/iter; left time: 75.3472s
        iters: 500, epoch: 9 | loss: 0.1658776
        speed: 0.1024s/iter; left time: 65.6473s
Epoch: 9 cost time: 59.044188499450684
Epoch: 9, Steps: 570 | Train Loss: 0.1706322 Vali Loss: 0.1666531 Test Loss: 0.2047767
Validation loss decreased (0.166843 --> 0.166653).  Saving model ...
Updating learning rate to 3.90625e-07
        iters: 100, epoch: 10 | loss: 0.1765422
        speed: 0.3307s/iter; left time: 155.7438s
        iters: 200, epoch: 10 | loss: 0.1650708
        speed: 0.1330s/iter; left time: 49.3448s
        iters: 300, epoch: 10 | loss: 0.1988290
        speed: 0.1098s/iter; left time: 29.7569s
        iters: 400, epoch: 10 | loss: 0.1684498
        speed: 0.1507s/iter; left time: 25.7680s
        iters: 500, epoch: 10 | loss: 0.1863105
        speed: 0.1327s/iter; left time: 9.4221s
Epoch: 10 cost time: 72.63109254837036
Epoch: 10, Steps: 570 | Train Loss: 0.1704728 Vali Loss: 0.1665897 Test Loss: 0.2046863
Validation loss decreased (0.166653 --> 0.166590).  Saving model ...
Updating learning rate to 1.953125e-07
>>>>>>>testing : long_term_forecast_ECL_96_96_TSMixer_custom_ftM_sl96_ll96_pl96_dm256_nh8_el2_dl1_df512_expand2_dc4_fc3_ebtimeF_dtTrue_Exp_0<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
test 5165
test shape: (5165, 96, 321) (5165, 96, 321)
test shape: (5165, 96, 321) (5165, 96, 321)
mse:0.2044449895620346, mae:0.30834755301475525, dtw:not calculated
(Time-Series-Library) remy@chimay:~/Travail/Time-Series-Library$

```

</details>

## Compression modulo = 10

* mse:0.21192729473114014
* mae:0.3221282362937927
* dtw:not calculated

<details>
<summary>Log</summary>

```text
(Time-Series-Library) remy@chimay:~/Travail/Time-Series-Library$ ./scripts/long_term_forecast/ECL_script/FLI_TSMixer.sh 
False
Args in experiment:
Basic Config
  Task Name:          long_term_forecast  Is Training:        1                   
  Model ID:           ECL_96_96           Model:              TSMixer             

Data Loader
  Data:               custom              Root Path:          ./dataset/electricity/
  Data Path:          electricity.csv     Features:           M                   
  Target:             OT                  Freq:               h                   
  Checkpoints:        ./checkpoints/      

Forecasting Task
  Seq Len:            96                  Label Len:          96                  
  Pred Len:           96                  Seasonal Patterns:  Monthly             
  Inverse:            0                   

Model Parameters
  Top k:              5                   Num Kernels:        6                   
  Enc In:             321                 Dec In:             321                 
  C Out:              321                 d model:            256                 
  n heads:            8                   e layers:           2                   
  d layers:           1                   d FF:               512                 
  Moving Avg:         25                  Factor:             3                   
  Distil:             1                   Dropout:            0.1                 
  Embed:              timeF               Activation:         gelu                

Run Parameters
  Num Workers:        10                  Itr:                1                   
  Train Epochs:       10                  Batch Size:         32                  
  Patience:           3                   Learning Rate:      0.0001              
  Des:                Exp                 Loss:               MSE                 
  Lradj:              type1               Use Amp:            0                   

GPU
  Use GPU:            0                   GPU:                0                   
  Use Multi GPU:      0                   Devices:            0,1,2,3             

De-stationary Projector Params
  P Hidden Dims:      128, 128            P Hidden Layers:    2                   

Compression Params
  Use ratio removal   True
  Removal modulo      10
  Use FLI             False

Use CPU
>>>>>>>start training : long_term_forecast_ECL_96_96_TSMixer_custom_ftM_sl96_ll96_pl96_dm256_nh8_el2_dl1_df512_expand2_dc4_fc3_ebtimeF_dtTrue_Exp_0>>>>>>>>>>>>>>>>>>>>>>>>>>
Dataset length before removal: 26304
Dataset length after removal: 23673
train 16380
Dataset length before removal: 26304
Dataset length after removal: 23673
val 2273
Dataset length before removal: 26304
Dataset length after removal: 23673
test 4639
        iters: 100, epoch: 1 | loss: 0.5363364
        speed: 0.0956s/iter; left time: 479.9248s
        iters: 200, epoch: 1 | loss: 0.3294132
        speed: 0.0975s/iter; left time: 479.6474s
        iters: 300, epoch: 1 | loss: 0.2746231
        speed: 0.1223s/iter; left time: 589.6232s
        iters: 400, epoch: 1 | loss: 0.2645397
        speed: 0.1146s/iter; left time: 540.9572s
        iters: 500, epoch: 1 | loss: 0.2454984
        speed: 0.1079s/iter; left time: 498.5876s
Epoch: 1 cost time: 55.09390735626221
Epoch: 1, Steps: 512 | Train Loss: 0.4199416 Vali Loss: 0.2256629 Test Loss: 0.2565744
Validation loss decreased (inf --> 0.225663).  Saving model ...
Updating learning rate to 0.0001
        iters: 100, epoch: 2 | loss: 0.2345424
        speed: 0.2313s/iter; left time: 1042.8316s
        iters: 200, epoch: 2 | loss: 0.2570868
        speed: 0.1118s/iter; left time: 493.1008s
        iters: 300, epoch: 2 | loss: 0.2322805
        speed: 0.1108s/iter; left time: 477.5086s
        iters: 400, epoch: 2 | loss: 0.2261664
        speed: 0.1136s/iter; left time: 478.2817s
        iters: 500, epoch: 2 | loss: 0.2161244
        speed: 0.1095s/iter; left time: 449.8407s
Epoch: 2 cost time: 58.31097149848938
Epoch: 2, Steps: 512 | Train Loss: 0.2338044 Vali Loss: 0.1993367 Test Loss: 0.2315472
Validation loss decreased (0.225663 --> 0.199337).  Saving model ...
Updating learning rate to 5e-05
        iters: 100, epoch: 3 | loss: 0.2118713
        speed: 0.2325s/iter; left time: 929.3773s
        iters: 200, epoch: 3 | loss: 0.1957972
        speed: 0.1105s/iter; left time: 430.4850s
        iters: 300, epoch: 3 | loss: 0.2196974
        speed: 0.1116s/iter; left time: 423.6432s
        iters: 400, epoch: 3 | loss: 0.1962884
        speed: 0.1104s/iter; left time: 408.2629s
        iters: 500, epoch: 3 | loss: 0.1984086
        speed: 0.1131s/iter; left time: 406.7699s
Epoch: 3 cost time: 56.86673021316528
Epoch: 3, Steps: 512 | Train Loss: 0.2084865 Vali Loss: 0.1894401 Test Loss: 0.2204113
Validation loss decreased (0.199337 --> 0.189440).  Saving model ...
Updating learning rate to 2.5e-05
        iters: 100, epoch: 4 | loss: 0.1845084
        speed: 0.2249s/iter; left time: 783.7082s
        iters: 200, epoch: 4 | loss: 0.1958526
        speed: 0.1096s/iter; left time: 371.1030s
        iters: 300, epoch: 4 | loss: 0.2229709
        speed: 0.1343s/iter; left time: 441.0340s
        iters: 400, epoch: 4 | loss: 0.1894036
        speed: 0.1150s/iter; left time: 366.3577s
        iters: 500, epoch: 4 | loss: 0.2038686
        speed: 0.1085s/iter; left time: 334.8714s
Epoch: 4 cost time: 58.988473653793335
Epoch: 4, Steps: 512 | Train Loss: 0.1964421 Vali Loss: 0.1845717 Test Loss: 0.2161328
Validation loss decreased (0.189440 --> 0.184572).  Saving model ...
Updating learning rate to 1.25e-05
        iters: 100, epoch: 5 | loss: 0.1862674
        speed: 0.2488s/iter; left time: 739.6175s
        iters: 200, epoch: 5 | loss: 0.1819067
        speed: 0.1191s/iter; left time: 342.0442s
        iters: 300, epoch: 5 | loss: 0.1838557
        speed: 0.1209s/iter; left time: 335.1477s
        iters: 400, epoch: 5 | loss: 0.1963688
        speed: 0.1228s/iter; left time: 328.2003s
        iters: 500, epoch: 5 | loss: 0.1861570
        speed: 0.1081s/iter; left time: 278.1768s
Epoch: 5 cost time: 60.9259250164032
Epoch: 5, Steps: 512 | Train Loss: 0.1907575 Vali Loss: 0.1831946 Test Loss: 0.2143253
Validation loss decreased (0.184572 --> 0.183195).  Saving model ...
Updating learning rate to 6.25e-06
        iters: 100, epoch: 6 | loss: 0.1948710
        speed: 0.2391s/iter; left time: 588.4804s
        iters: 200, epoch: 6 | loss: 0.1853953
        speed: 0.1085s/iter; left time: 256.1102s
        iters: 300, epoch: 6 | loss: 0.1868706
        speed: 0.1140s/iter; left time: 257.7515s
        iters: 400, epoch: 6 | loss: 0.1778338
        speed: 0.1075s/iter; left time: 232.3383s
        iters: 500, epoch: 6 | loss: 0.1713787
        speed: 0.1056s/iter; left time: 217.6920s
Epoch: 6 cost time: 56.49040222167969
Epoch: 6, Steps: 512 | Train Loss: 0.1879884 Vali Loss: 0.1821435 Test Loss: 0.2131545
Validation loss decreased (0.183195 --> 0.182144).  Saving model ...
Updating learning rate to 3.125e-06
        iters: 100, epoch: 7 | loss: 0.1775076
        speed: 0.2676s/iter; left time: 521.5074s
        iters: 200, epoch: 7 | loss: 0.1971138
        speed: 0.1422s/iter; left time: 263.0118s
        iters: 300, epoch: 7 | loss: 0.2015523
        speed: 0.1202s/iter; left time: 210.3149s
        iters: 400, epoch: 7 | loss: 0.1888995
        speed: 0.1257s/iter; left time: 207.2490s
        iters: 500, epoch: 7 | loss: 0.1918594
        speed: 0.1158s/iter; left time: 179.3567s
Epoch: 7 cost time: 66.98510146141052
Epoch: 7, Steps: 512 | Train Loss: 0.1866369 Vali Loss: 0.1805069 Test Loss: 0.2121310
Validation loss decreased (0.182144 --> 0.180507).  Saving model ...
Updating learning rate to 1.5625e-06
        iters: 100, epoch: 8 | loss: 0.1909852
        speed: 0.2444s/iter; left time: 351.1941s
        iters: 200, epoch: 8 | loss: 0.1810270
        speed: 0.1335s/iter; left time: 178.4541s
        iters: 300, epoch: 8 | loss: 0.1974450
        speed: 0.1242s/iter; left time: 153.6326s
        iters: 400, epoch: 8 | loss: 0.1905089
        speed: 0.1330s/iter; left time: 151.1905s
        iters: 500, epoch: 8 | loss: 0.1973506
        speed: 0.1136s/iter; left time: 117.8513s
Epoch: 8 cost time: 64.5753755569458
Epoch: 8, Steps: 512 | Train Loss: 0.1859255 Vali Loss: 0.1801888 Test Loss: 0.2119123
Validation loss decreased (0.180507 --> 0.180189).  Saving model ...
Updating learning rate to 7.8125e-07
        iters: 100, epoch: 9 | loss: 0.1935965
        speed: 0.2794s/iter; left time: 258.4862s
        iters: 200, epoch: 9 | loss: 0.1924506
        speed: 0.1230s/iter; left time: 101.4907s
        iters: 300, epoch: 9 | loss: 0.1826755
        speed: 0.1252s/iter; left time: 90.7787s
        iters: 400, epoch: 9 | loss: 0.1690192
        speed: 0.1179s/iter; left time: 73.6620s
        iters: 500, epoch: 9 | loss: 0.1839802
        speed: 0.1239s/iter; left time: 65.0542s
Epoch: 9 cost time: 62.94557571411133
Epoch: 9, Steps: 512 | Train Loss: 0.1855854 Vali Loss: 0.1801235 Test Loss: 0.2119324
Validation loss decreased (0.180189 --> 0.180124).  Saving model ...
Updating learning rate to 3.90625e-07
        iters: 100, epoch: 10 | loss: 0.1889835
        speed: 0.2786s/iter; left time: 115.0497s
        iters: 200, epoch: 10 | loss: 0.1918574
        speed: 0.1164s/iter; left time: 36.4455s
        iters: 300, epoch: 10 | loss: 0.2086816
        speed: 0.1288s/iter; left time: 27.4250s
        iters: 400, epoch: 10 | loss: 0.1977678
        speed: 0.1353s/iter; left time: 15.2854s
        iters: 500, epoch: 10 | loss: 0.1680569
        speed: 0.1239s/iter; left time: 1.6106s
Epoch: 10 cost time: 66.84992289543152
Epoch: 10, Steps: 512 | Train Loss: 0.1853927 Vali Loss: 0.1799102 Test Loss: 0.2119397
Validation loss decreased (0.180124 --> 0.179910).  Saving model ...
Updating learning rate to 1.953125e-07
>>>>>>>testing : long_term_forecast_ECL_96_96_TSMixer_custom_ftM_sl96_ll96_pl96_dm256_nh8_el2_dl1_df512_expand2_dc4_fc3_ebtimeF_dtTrue_Exp_0<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
Dataset length before removal: 26304
Dataset length after removal: 23673
test 4639
test shape: (4639, 96, 321) (4639, 96, 321)
test shape: (4639, 96, 321) (4639, 96, 321)
mse:0.21192729473114014, mae:0.3221282362937927, dtw:not calculated
(Time-Series-Library) remy@chimay:~/Travail/Time-Series-Library$
```

</details>


## Compression modulo = 5

* mse:0.20996823906898499
* mae:0.3226729929447174
* dtw:not calculated

<details>
<summary>Log</summary>

```text
(Time-Series-Library) remy@chimay:~/Travail/Time-Series-Library$ ./scripts/long_term_forecast/ECL_script/FLI_TSMixer.sh 
False
Args in experiment:
Basic Config
  Task Name:          long_term_forecast  Is Training:        1                   
  Model ID:           ECL_96_96           Model:              TSMixer             

Data Loader
  Data:               custom              Root Path:          ./dataset/electricity/
  Data Path:          electricity.csv     Features:           M                   
  Target:             OT                  Freq:               h                   
  Checkpoints:        ./checkpoints/      

Forecasting Task
  Seq Len:            96                  Label Len:          96                  
  Pred Len:           96                  Seasonal Patterns:  Monthly             
  Inverse:            0                   

Model Parameters
  Top k:              5                   Num Kernels:        6                   
  Enc In:             321                 Dec In:             321                 
  C Out:              321                 d model:            256                 
  n heads:            8                   e layers:           2                   
  d layers:           1                   d FF:               512                 
  Moving Avg:         25                  Factor:             3                   
  Distil:             1                   Dropout:            0.1                 
  Embed:              timeF               Activation:         gelu                

Run Parameters
  Num Workers:        10                  Itr:                1                   
  Train Epochs:       10                  Batch Size:         32                  
  Patience:           3                   Learning Rate:      0.0001              
  Des:                Exp                 Loss:               MSE                 
  Lradj:              type1               Use Amp:            0                   

GPU
  Use GPU:            0                   GPU:                0                   
  Use Multi GPU:      0                   Devices:            0,1,2,3             

De-stationary Projector Params
  P Hidden Dims:      128, 128            P Hidden Layers:    2                   

Compression Params
  Use ratio removal   True
  Removal modulo      5
  Use FLI             False

Use CPU
>>>>>>>start training : long_term_forecast_ECL_96_96_TSMixer_custom_ftM_sl96_ll96_pl96_dm256_nh8_el2_dl1_df512_expand2_dc4_fc3_ebtimeF_dtTrue_Exp_0>>>>>>>>>>>>>>>>>>>>>>>>>>
Dataset length before removal: 26304
Dataset length after removal: 21043
train 14539
Dataset length before removal: 26304
Dataset length after removal: 21043
val 2010
Dataset length before removal: 26304
Dataset length after removal: 21043
test 4113
        iters: 100, epoch: 1 | loss: 0.4526819
        speed: 0.0964s/iter; left time: 428.8915s
        iters: 200, epoch: 1 | loss: 0.3038739
        speed: 0.0914s/iter; left time: 397.4931s
        iters: 300, epoch: 1 | loss: 0.2843055
        speed: 0.0996s/iter; left time: 423.3015s
        iters: 400, epoch: 1 | loss: 0.2675211
        speed: 0.1113s/iter; left time: 461.8455s
Epoch: 1 cost time: 45.80435585975647
Epoch: 1, Steps: 455 | Train Loss: 0.4159644 Vali Loss: 0.2293215 Test Loss: 0.2599419
Validation loss decreased (inf --> 0.229321).  Saving model ...
Updating learning rate to 0.0001
        iters: 100, epoch: 2 | loss: 0.2530901
        speed: 0.2509s/iter; left time: 1002.5101s
        iters: 200, epoch: 2 | loss: 0.2379164
        speed: 0.1017s/iter; left time: 396.3594s
        iters: 300, epoch: 2 | loss: 0.2116215
        speed: 0.1049s/iter; left time: 398.2645s
        iters: 400, epoch: 2 | loss: 0.2129620
        speed: 0.1013s/iter; left time: 374.3718s
Epoch: 2 cost time: 46.75868248939514
Epoch: 2, Steps: 455 | Train Loss: 0.2320517 Vali Loss: 0.1955924 Test Loss: 0.2252207
Validation loss decreased (0.229321 --> 0.195592).  Saving model ...
Updating learning rate to 5e-05
        iters: 100, epoch: 3 | loss: 0.2140757
        speed: 0.2494s/iter; left time: 883.0949s
        iters: 200, epoch: 3 | loss: 0.1953971
        speed: 0.1129s/iter; left time: 388.5232s
        iters: 300, epoch: 3 | loss: 0.1957671
        speed: 0.1074s/iter; left time: 358.6595s
        iters: 400, epoch: 3 | loss: 0.1952803
        speed: 0.1012s/iter; left time: 327.8444s
Epoch: 3 cost time: 48.099807262420654
Epoch: 3, Steps: 455 | Train Loss: 0.2006285 Vali Loss: 0.1856159 Test Loss: 0.2163996
Validation loss decreased (0.195592 --> 0.185616).  Saving model ...
Updating learning rate to 2.5e-05
        iters: 100, epoch: 4 | loss: 0.1723758
        speed: 0.2420s/iter; left time: 746.9330s
        iters: 200, epoch: 4 | loss: 0.1866489
        speed: 0.1014s/iter; left time: 302.7530s
        iters: 300, epoch: 4 | loss: 0.2004774
        speed: 0.1012s/iter; left time: 292.1176s
        iters: 400, epoch: 4 | loss: 0.1986045
        speed: 0.1036s/iter; left time: 288.6701s
Epoch: 4 cost time: 46.32120084762573
Epoch: 4, Steps: 455 | Train Loss: 0.1896817 Vali Loss: 0.1818346 Test Loss: 0.2129850
Validation loss decreased (0.185616 --> 0.181835).  Saving model ...
Updating learning rate to 1.25e-05
        iters: 100, epoch: 5 | loss: 0.1833375
        speed: 0.2644s/iter; left time: 695.6252s
        iters: 200, epoch: 5 | loss: 0.1812753
        speed: 0.1021s/iter; left time: 258.4311s
        iters: 300, epoch: 5 | loss: 0.1756742
        speed: 0.1017s/iter; left time: 247.1395s
        iters: 400, epoch: 5 | loss: 0.1746496
        speed: 0.1037s/iter; left time: 241.6682s
Epoch: 5 cost time: 48.4705023765564
Epoch: 5, Steps: 455 | Train Loss: 0.1848886 Vali Loss: 0.1797467 Test Loss: 0.2110589
Validation loss decreased (0.181835 --> 0.179747).  Saving model ...
Updating learning rate to 6.25e-06
        iters: 100, epoch: 6 | loss: 0.1630780
        speed: 0.2612s/iter; left time: 568.4547s
        iters: 200, epoch: 6 | loss: 0.1762531
        speed: 0.1109s/iter; left time: 230.2200s
        iters: 300, epoch: 6 | loss: 0.1813252
        speed: 0.1007s/iter; left time: 198.9094s
        iters: 400, epoch: 6 | loss: 0.1898994
        speed: 0.1087s/iter; left time: 203.9184s
Epoch: 6 cost time: 49.36317586898804
Epoch: 6, Steps: 455 | Train Loss: 0.1825772 Vali Loss: 0.1789705 Test Loss: 0.2112614
Validation loss decreased (0.179747 --> 0.178971).  Saving model ...
Updating learning rate to 3.125e-06
        iters: 100, epoch: 7 | loss: 0.1704567
        speed: 0.2787s/iter; left time: 479.5867s
        iters: 200, epoch: 7 | loss: 0.1855661
        speed: 0.1414s/iter; left time: 229.1764s
        iters: 300, epoch: 7 | loss: 0.1830989
        speed: 0.1158s/iter; left time: 176.0591s
        iters: 400, epoch: 7 | loss: 0.1870881
        speed: 0.1256s/iter; left time: 178.4616s
Epoch: 7 cost time: 57.85825276374817
Epoch: 7, Steps: 455 | Train Loss: 0.1813886 Vali Loss: 0.1783540 Test Loss: 0.2102847
Validation loss decreased (0.178971 --> 0.178354).  Saving model ...
Updating learning rate to 1.5625e-06
        iters: 100, epoch: 8 | loss: 0.1808583
        speed: 0.2567s/iter; left time: 325.0436s
        iters: 200, epoch: 8 | loss: 0.1787083
        speed: 0.1169s/iter; left time: 136.2810s
        iters: 300, epoch: 8 | loss: 0.1770150
        speed: 0.1203s/iter; left time: 128.2712s
        iters: 400, epoch: 8 | loss: 0.1896706
        speed: 0.1120s/iter; left time: 108.1693s
Epoch: 8 cost time: 51.60160779953003
Epoch: 8, Steps: 455 | Train Loss: 0.1808117 Vali Loss: 0.1781754 Test Loss: 0.2103850
Validation loss decreased (0.178354 --> 0.178175).  Saving model ...
Updating learning rate to 7.8125e-07
        iters: 100, epoch: 9 | loss: 0.1804914
        speed: 0.2668s/iter; left time: 216.3849s
        iters: 200, epoch: 9 | loss: 0.1720602
        speed: 0.1069s/iter; left time: 76.0236s
        iters: 300, epoch: 9 | loss: 0.1705212
        speed: 0.1111s/iter; left time: 67.9031s
        iters: 400, epoch: 9 | loss: 0.1718170
        speed: 0.1257s/iter; left time: 64.2437s
Epoch: 9 cost time: 52.550280809402466
Epoch: 9, Steps: 455 | Train Loss: 0.1804977 Vali Loss: 0.1779829 Test Loss: 0.2101466
Validation loss decreased (0.178175 --> 0.177983).  Saving model ...
Updating learning rate to 3.90625e-07
        iters: 100, epoch: 10 | loss: 0.1688715
        speed: 0.2688s/iter; left time: 95.6969s
        iters: 200, epoch: 10 | loss: 0.1871803
        speed: 0.1032s/iter; left time: 26.4311s
        iters: 300, epoch: 10 | loss: 0.1931292
        speed: 0.1055s/iter; left time: 16.4560s
        iters: 400, epoch: 10 | loss: 0.1862157
        speed: 0.1019s/iter; left time: 5.7059s
Epoch: 10 cost time: 47.81919622421265
Epoch: 10, Steps: 455 | Train Loss: 0.1803244 Vali Loss: 0.1780487 Test Loss: 0.2101747
EarlyStopping counter: 1 out of 3
Updating learning rate to 1.953125e-07
>>>>>>>testing : long_term_forecast_ECL_96_96_TSMixer_custom_ftM_sl96_ll96_pl96_dm256_nh8_el2_dl1_df512_expand2_dc4_fc3_ebtimeF_dtTrue_Exp_0<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
Dataset length before removal: 26304
Dataset length after removal: 21043
test 4113
test shape: (4113, 96, 321) (4113, 96, 321)
test shape: (4113, 96, 321) (4113, 96, 321)
mse:0.20996823906898499, mae:0.3226729929447174, dtw:not calculated
(Time-Series-Library) remy@chimay:~/Travail/Time-Series-Library$
```

</details>

## Compression modulo = 2

* mse:0.2056574523448944
* mae:0.3166302442550659
* dtw:not calculated

<details>

<summary>Log</summary>

```text
(Time-Series-Library) remy@chimay:~/Travail/Time-Series-Library$ ./scripts/long_term_forecast/ECL_script/FLI_TSMixer.sh 
False
Args in experiment:
Basic Config
  Task Name:          long_term_forecast  Is Training:        1                   
  Model ID:           ECL_96_96           Model:              TSMixer             

Data Loader
  Data:               custom              Root Path:          ./dataset/electricity/
  Data Path:          electricity.csv     Features:           M                   
  Target:             OT                  Freq:               h                   
  Checkpoints:        ./checkpoints/      

Forecasting Task
  Seq Len:            96                  Label Len:          96                  
  Pred Len:           96                  Seasonal Patterns:  Monthly             
  Inverse:            0                   

Model Parameters
  Top k:              5                   Num Kernels:        6                   
  Enc In:             321                 Dec In:             321                 
  C Out:              321                 d model:            256                 
  n heads:            8                   e layers:           2                   
  d layers:           1                   d FF:               512                 
  Moving Avg:         25                  Factor:             3                   
  Distil:             1                   Dropout:            0.1                 
  Embed:              timeF               Activation:         gelu                

Run Parameters
  Num Workers:        10                  Itr:                1                   
  Train Epochs:       10                  Batch Size:         32                  
  Patience:           3                   Learning Rate:      0.0001              
  Des:                Exp                 Loss:               MSE                 
  Lradj:              type1               Use Amp:            0                   

GPU
  Use GPU:            0                   GPU:                0                   
  Use Multi GPU:      0                   Devices:            0,1,2,3             

De-stationary Projector Params
  P Hidden Dims:      128, 128            P Hidden Layers:    2                   

Compression Params
  Use ratio removal   True
  Removal modulo      2
  Use FLI             False

Use CPU
>>>>>>>start training : long_term_forecast_ECL_96_96_TSMixer_custom_ftM_sl96_ll96_pl96_dm256_nh8_el2_dl1_df512_expand2_dc4_fc3_ebtimeF_dtTrue_Exp_0>>>>>>>>>>>>>>>>>>>>>>>>>>
Dataset length before removal: 26304
Dataset length after removal: 13152
train 9015
Dataset length before removal: 26304
Dataset length after removal: 13152
val 1221
Dataset length before removal: 26304
Dataset length after removal: 13152
test 2535
        iters: 100, epoch: 1 | loss: 0.4944516
        speed: 0.0967s/iter; left time: 263.1822s
        iters: 200, epoch: 1 | loss: 0.3360328
        speed: 0.0912s/iter; left time: 239.1461s
Epoch: 1 cost time: 26.762113094329834
Epoch: 1, Steps: 282 | Train Loss: 0.5406183 Vali Loss: 0.2522286 Test Loss: 0.2801394
Validation loss decreased (inf --> 0.252229).  Saving model ...
Updating learning rate to 0.0001
        iters: 100, epoch: 2 | loss: 0.2562513
        speed: 0.2394s/iter; left time: 583.8615s
        iters: 200, epoch: 2 | loss: 0.2260643
        speed: 0.1227s/iter; left time: 287.0964s
Epoch: 2 cost time: 33.17653822898865
Epoch: 2, Steps: 282 | Train Loss: 0.2536972 Vali Loss: 0.2070762 Test Loss: 0.2352139
Validation loss decreased (0.252229 --> 0.207076).  Saving model ...
Updating learning rate to 5e-05
        iters: 100, epoch: 3 | loss: 0.2116764
        speed: 0.2741s/iter; left time: 591.3060s
        iters: 200, epoch: 3 | loss: 0.2080075
        speed: 0.1072s/iter; left time: 220.5146s
Epoch: 3 cost time: 30.65452814102173
Epoch: 3, Steps: 282 | Train Loss: 0.2159021 Vali Loss: 0.1912096 Test Loss: 0.2209025
Validation loss decreased (0.207076 --> 0.191210).  Saving model ...
Updating learning rate to 2.5e-05
        iters: 100, epoch: 4 | loss: 0.1993403
        speed: 0.2475s/iter; left time: 464.1360s
        iters: 200, epoch: 4 | loss: 0.1951761
        speed: 0.1070s/iter; left time: 189.8703s
Epoch: 4 cost time: 31.306031465530396
Epoch: 4, Steps: 282 | Train Loss: 0.2008523 Vali Loss: 0.1834760 Test Loss: 0.2140392
Validation loss decreased (0.191210 --> 0.183476).  Saving model ...
Updating learning rate to 1.25e-05
        iters: 100, epoch: 5 | loss: 0.2071504
        speed: 0.2729s/iter; left time: 434.7632s
        iters: 200, epoch: 5 | loss: 0.1887508
        speed: 0.1096s/iter; left time: 163.7061s
Epoch: 5 cost time: 31.043497562408447
Epoch: 5, Steps: 282 | Train Loss: 0.1941675 Vali Loss: 0.1802365 Test Loss: 0.2111318
Validation loss decreased (0.183476 --> 0.180236).  Saving model ...
Updating learning rate to 6.25e-06
        iters: 100, epoch: 6 | loss: 0.1929080
        speed: 0.2579s/iter; left time: 338.1293s
        iters: 200, epoch: 6 | loss: 0.2051821
        speed: 0.1089s/iter; left time: 131.9338s
Epoch: 6 cost time: 30.794340133666992
Epoch: 6, Steps: 282 | Train Loss: 0.1909036 Vali Loss: 0.1792975 Test Loss: 0.2091824
Validation loss decreased (0.180236 --> 0.179298).  Saving model ...
Updating learning rate to 3.125e-06
        iters: 100, epoch: 7 | loss: 0.1878544
        speed: 0.2563s/iter; left time: 263.6880s
        iters: 200, epoch: 7 | loss: 0.1820252
        speed: 0.1041s/iter; left time: 96.6886s
Epoch: 7 cost time: 30.516685724258423
Epoch: 7, Steps: 282 | Train Loss: 0.1892805 Vali Loss: 0.1790006 Test Loss: 0.2086824
Validation loss decreased (0.179298 --> 0.179001).  Saving model ...
Updating learning rate to 1.5625e-06
        iters: 100, epoch: 8 | loss: 0.2005111
        speed: 0.2524s/iter; left time: 188.5586s
        iters: 200, epoch: 8 | loss: 0.1787743
        speed: 0.1096s/iter; left time: 70.8927s
Epoch: 8 cost time: 30.71825885772705
Epoch: 8, Steps: 282 | Train Loss: 0.1884159 Vali Loss: 0.1791074 Test Loss: 0.2084339
EarlyStopping counter: 1 out of 3
Updating learning rate to 7.8125e-07
        iters: 100, epoch: 9 | loss: 0.1801910
        speed: 0.2873s/iter; left time: 133.6020s
        iters: 200, epoch: 9 | loss: 0.2106225
        speed: 0.1112s/iter; left time: 40.6045s
Epoch: 9 cost time: 33.0668830871582
Epoch: 9, Steps: 282 | Train Loss: 0.1879667 Vali Loss: 0.1784551 Test Loss: 0.2083215
Validation loss decreased (0.179001 --> 0.178455).  Saving model ...
Updating learning rate to 3.90625e-07
        iters: 100, epoch: 10 | loss: 0.1838259
        speed: 0.2495s/iter; left time: 45.6631s
        iters: 200, epoch: 10 | loss: 0.1983419
        speed: 0.1067s/iter; left time: 8.8575s
Epoch: 10 cost time: 29.617989540100098
Epoch: 10, Steps: 282 | Train Loss: 0.1877759 Vali Loss: 0.1790435 Test Loss: 0.2081630
EarlyStopping counter: 1 out of 3
Updating learning rate to 1.953125e-07
>>>>>>>testing : long_term_forecast_ECL_96_96_TSMixer_custom_ftM_sl96_ll96_pl96_dm256_nh8_el2_dl1_df512_expand2_dc4_fc3_ebtimeF_dtTrue_Exp_0<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
Dataset length before removal: 26304
Dataset length after removal: 13152
test 2535
test shape: (2535, 96, 321) (2535, 96, 321)
test shape: (2535, 96, 321) (2535, 96, 321)
mse:0.2056574523448944, mae:0.3166302442550659, dtw:not calculated
(Time-Series-Library) remy@chimay:~/Travail/Time-Series-Library$
```

</details>
