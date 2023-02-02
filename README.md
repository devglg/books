# books
Spreadsheet to keep track of financial data for small businesses

Created in LibreOffice, may work with MS Office, but will definitely NOT work with OpenOffice because of an Array formula bug

Intended for cash accounting, it may be difficult to do accrual since I only use one account per transaction.
I recommend using quickbooks for your accounting, but if you're starting and need just something free and fast, you can use this.

TO DO:
1. Liabilities do not work completely, need a page for interest tracking.
2. Asset tracking is very simple, and only straight line, you can use double declining if you want but the formula needs to change:
```
=2*C5/E5   for year 1
=IF(H5>1,2*(C5-I5)/E5,0)   for year 2
=IF(H5>2,2*(C5-SUM(I5:J5))/E5,0)  for year 3
=IF(H5>3,2*(C5-SUM(I5:K5))/E5,0)   for year 4
=IF(H5>4,2*(C5-SUM(I5:L5))/E5,0)   for year 5
=IF(H5>5,IF(H5<=E5,E2*(C5-SUM(I5:M5))/E5,0),0)  for year 6
=IF(H5>5,IF(H5<=E5,E2*(C5-SUM(I5:N5))/E5,0),0)  for year 7
...
```

If you need any other depreciation schedule, just change the formula

The file is given as is, with no warranty, under the Apache 2 License so, you can do almost anything you want with it. If you find it useful and wouldn't mind sending me a tip my cashapp is $GLGracia  :)
