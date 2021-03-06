# wyset: the ideal set cardinality estimator

What we do is to obtain a 3X larger Bloom Filter by utilizating wasted bits in a byte.

high 5 bits   low 3 bits

10110         010

HyperLogLog   Bloom Filter

--------------------------

16 bytes register:

|set_size|wyset_error%|Flajolet_error%|error_ratio|
|----|----|----|----|
|1|0|3.20957|0|
|2|10.2863|17.5831|0.58501|
|4|10.4262|18.4793|0.564208|
|7|10.4607|19.288|0.542341|
|11|10.619|20.4045|0.520426|
|17|10.8856|22.5151|0.483478|
|26|11.2606|25.6566|0.438895|
|40|13.0163|22.0571|0.590119|
|61|20.8891|22.7856|0.916768|
|92|21.4764|24.3478|0.882066|
|139|24.8171|25.0956|0.988904|
|209|25.542|25.603|0.99762|
|314|25.9419|25.9988|0.997812|
|472|25.9692|26.0785|0.995812|
|709|26.2222|26.3069|0.99678|
|1064|26.2889|26.3634|0.997174|
|1597|26.2849|26.3861|0.996164|
|2396|26.3565|26.4837|0.9952|
|3595|26.3352|26.4238|0.99665|
|5393|26.2305|26.3535|0.995331|
|8090|26.3317|26.4603|0.995139|
|12136|26.3735|26.4978|0.995311|
|18205|26.4044|26.5481|0.994586|
|27308|26.4763|26.6035|0.995219|
|40963|26.4077|26.51|0.996142|
|61445|26.406|26.4827|0.997107|

1024 bytes register

|set_size|wyset_error%|Flajolet_error%|error_ratio|
|----|----|----|----|
|1|0|0.048848|0|
|2|1.3539|2.24964|0.601829|
|4|1.30994|2.36349|0.554241|
|7|1.27686|2.19678|0.581242|
|11|1.22325|2.2209|0.55079|
|17|1.27305|2.21773|0.574033|
|26|1.28484|2.22506|0.577442|
|40|1.27046|2.22415|0.571212|
|61|1.27974|2.22132|0.576115|
|92|1.28481|2.24848|0.571412|
|139|1.28573|2.25903|0.569153|
|209|1.294|2.29182|0.564616|
|314|1.29725|2.33021|0.55671|
|472|1.31051|2.38936|0.54848|
|709|1.31952|2.50442|0.526876|
|1064|1.35198|2.67172|0.506033|
|1597|1.39879|2.9618|0.472277|
|2396|1.46661|3.77302|0.38871|
|3595|1.57978|2.769|0.570525|
|5393|1.78578|2.95171|0.604996|
|8090|3.00911|3.03044|0.992961|
|12136|3.13332|3.13899|0.998193|
|18205|3.15267|3.15958|0.997815|
|27308|3.18822|3.19666|0.99736|
|40963|3.20428|3.21115|0.997861|
|61445|3.20169|3.20875|0.997801|
