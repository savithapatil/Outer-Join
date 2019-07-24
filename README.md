# The Outer Join
- All the records of one table along with the matching records of another table make up the output
- Types:
  - Left Outer Join
  - Right Outer Join

# Left Outer Join
### The output is comprised of . . .  
- **All rows** of the **left** table, _even if they do not satisfy the matching condition_
- The **matching rows** of the **right** table 
- `NULL` in the spaces that come from the **right** table _where the matching condition is not satisfied_

## Here's an example

### Two tables, Orders and Customers, are shown below

![Image](https://lh3.googleusercontent.com/ljyc3gbta35hTijzIMhrS1B52L3jCPA1tSopR3COVvd9aTN97Khf32mcIiVIKZiBSYlZcaepNBaSxSMWgfOLf_XdRXIl6n5qOuMtw82PFTm1coisVisQ_DTjJsz6tbjG0t1pJBM27eRC_O7w3JMDzROx6tQsDdDRuHCHT5SAicjSXeh9ufsADKfBh-R2zINW21PJLV5T-Y4bIIesqiWsYfZZmjCKNm6ISVqw-sJJvjibeG9bU2QpNYK4DMLSlAAap1EwwYvu5KmnWRsWGqrbjo37DFy4bs3dKuMsNA0HFMsVSBBywaINyawI_Ab-iYjuL5zkrq5wPrslbBNVNl81Dfg-fw06CDpceWGk0Vnm1d3TgZqpjez22qHoXsHTXCYkQuXiebIk_VYzsozJNYLBPHBAwB7pPYdTu0uvTVBQXkC-bajZyGRNW4DMW2ID0uTA_nBWShObOppvSxsmff21JSSBK5AFXiG_eJ_xzpM_8TwmT8pP_lsMBLtNRR77XUMSNB028xfBm0kM1htBejDX4rtwEc5YcANQd--Wm6KBciU9Y2nnCqVOM1XQoJ0oEJdpD_CQlaAPMtt-YxJY4anZWtXwBCHkBXQ2o_5Q5Qu3QaTeQKiv1pgPCOtpry9aLBa5NKYNoukBiAlckfV2fCsqNYna1zJGtCFu=w364-h147-no)

![Image](https://lh3.googleusercontent.com/RisAPk3UDtQktyGgNwKC8KqY_dfp1MMqpsqnISzfyL8BxvPUgeTHjezev5Layw0GRl2oUS1E_Z2KrTCb-RbAgWGz8aDIPEMebjpiWsWyp3SVUXEGsF0sUoxbZgJdQBVsLJpHk-SArV1MkLnXb82n4zs1OIo9rXz-_Bv1YsXvpIERbfYDQmXq6FKe8_s6oYMklafgdjZixIuzKvCXOB-3RRzB-RxadMyfhPOLZBJkBee2HMqE3gIOanoJyeRiyo_weItqtedZezE3iBDc9omMjr3um3QtFrb5dbWIXzRyoPGISPdbiB38ksIh2Oa8gZAY_03xLqnNw_jSV5vG9tzXJxr0fn2LCD_Zn6x9SLCORH4dSsSW_BxffwEH0JijkOwAb-zXZo4F-JqfgTPATmrBOJ5hTXZ3vcHzzjVCrdZdKkmR52SCO-tOD47-Ct4bx-D4gCNNG8AdXVYv9ahm6UZQrlbD6zxXLp1cCRrPJ6OH0pTipk6rvZAWAsYHvhZ-40u0aQ_cTxyvH1iw2pTcucEvLxipkMer_dSUdQ0ZxEp46IBxPoBOiNTaFatZArECoqGUYy28vhBcyohJCY_QYjEwEPHujw9Xzty_3HmjMoq2StvYiMOehqk7UMPYBVd5gSpPaEEflUZIzyR1XeuONIDyw2taqWbKUPDC=w812-h147-no)

### The `SELECT` statement shows which columns between the two tables are going to be included in the output:
```
SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
```
![Image](https://lh3.googleusercontent.com/-_ReRnvFzoj7bSNTJimjs0_xD-4uVbWX5NsUI5w39CYM2HMBlzYVPFnaDBvdb44NsGuQS2oeFKsQZ5jmUq2NEB2PLe48dnTO7Lec7T26CORnnZmPJpXG1TGHfQkz4YVqU-b9bqDtU4NgsjL9w5YeaBSz3fYGenQ96uPvYG_BIzB3r3Vz6zs9kyqSaXtWGB56bQ2NXh2wusMhLCBSyyh-rLTJIemN3DE6FGJ6VylsfBXCbkOR6nSKUYp2n3OJqceTVQm2DhaRy31gwEAWB335PxMZCAdXAClKfA3YeTTdOl3J-6-Nr0-uW4hjCvv2KT6g-Wh9kK0bY9334DZ484Cco92ozfB3D3ieWxuS2x8lFtKN4fQrA5zFECzW9bYp9xvDl1usucrKIwHKSevkVxK6To887KnZAQQ221IaRlxQMLf1Qz7dskW8dBI4uxBSSdtmQe9PisbC1Rt5wtZMZyMSi0Hr6ekDTy4s_MB1FwrHqNhqbzfSuxYVH8eAoy7ufpNIWuNaDuarPZAb2J6lLwa2ZUO424kyQ6CDwwh-Q3bRanFB3HVXca1_IKqUWUloTHrhQs-mngBnrr6U40FUQy4qQUu-IZmwPYS3QdjA3qHzs0wcEilAcLw2E0R1YjHfiOld01aNcbaqCF6LTiilFBiaRCVajz0avj6d=w376-h147-no)

![Image](https://lh3.googleusercontent.com/xuDlVE8arBCH7VaX0arAaXPJWFiC86iqdZAlKLVGfyoEBD6HPHdFqKUXvTj8acankhQPz78iM766CB9RTqNw9SRNvBRX-iLw9ZFFu9iO2a73VXvbwgwt9jGToe8_3dRTnTAI6baE6b69KzGKaKH-izqrU7Q3ZnxEx7iy8OFV6U_YYL8benMcBqsXTHxFSZ1PMmd1Xc-_74hI4_gmO0QgNJdEeBAS9y3D52tt3sGpHPdsfoZd4V2xf1yk_69pLcfMwQqFYqTD2EU5coNODwdzcpm94JfPEj0Cnc6fqODh6GavR-5xP9sbI8osfJNCqo1e-XH6oS_eBBsVKI75kmO9w3Km_6X5WsHfrBdn3e-r3qFNdhSPIaobdrK63uOChT-pf9MelPK3GUz9nZuaqtZ7h2qenGWJFUB99IFfeRNQgxTIsS0kHRMAtfuxKtTx7QcbUpqoVMuwktO5z92Hl1qkKjUEaNNn0dDRiws4T4K182AXdNDEwMljV2KpmZS8Anr35IWmIGKeRgNbzQt1OFFrWJ3lpffPmSDSKkRESo8W3wnlA7w7UTDh9zV4u0V-KpJugR7WbuFDA0bozlz-18-2W7eTwqaLFI4Hr1rY1ZPi96VYT4DkJcS_2yL6aTUHbkdx1w0Q3omiFJEGviWmIzPqCUh-PwibyNaJ=w797-h145-no)

### In the code below . . .
```
FROM Orders LEFT JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
```
. . . **All records** from the **left** table and **matching rows** from the **right** table are highlighted below

![Image](https://lh3.googleusercontent.com/-juqthadVSLm8fIrH0kzDSB67dQKFp0vwHmK4_-na6joD7d-zF-aTA752G9O-FEmsnTXJP7Zeq9sIsTwyLAYZeu5ZyUk1aapI7DP2die_vkZ2pC12as_UyNgQ1E1dTM2r7EqhRx1ci5W68DrEDmoUalEUoivDIc5FQ-zUwxBOU2AYgHkr4UfisVu2VDvKX_5eJC-Am5KmNAssWK3ehMbcY_TF0cE2oiGwwVCzCERplKA1rqJHXZw29BU72sYt0c4GhT3ACPxZGxLMXdENFRJcuBDSxnjR78tTJ6LbfUwPDSpWEgDm3CSDngIWhrcGdzbdXE93re1F48YaAX3eA_eEY-b0RRo7nrMd-m3WC0R0nFdCHVW4FOAne7AXFojFhyCMU68ftRbLbokiho0Ny3yNPEHrMuJC50kQbf3369oDv9tCAsCiChhJXjk82zlavBU90VedHfMIyZGGEfOOyLghAWk_5priDijvG2aFds_lD6JPenwmIQ78FnG1yCrk22Sylvc6BJGMMSAto1a-mhoMuFQgzX9CZf5MblMyaD7A6cs_EYWN6Zizdd8XBXLJP8lRSeDJV19C26FMoX6cMYHSmIhlsQ15O1fmwkDl-bUPWTUmUgM9u-0WV8FvRkD_ukyeyIE6_f1Hg6nIqjFe5eBa3JGb0fovsHf=w1395-h173-no)


### Together, the query below . . .
``` 
SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
FROM Orders LEFT JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
```
### . . . results in the following output:
![Image](https://lh3.googleusercontent.com/rzRj4Rz3xntcvhdz8Ervtfk6qWme6ASXthcNhgDzj3X04-4HcObgS9MnePxMjLQ4nDnTesc4RVUThjsHqmexF-6XoJIwwEZjOJB5m1c1_GpgCYBsH9Dw7tVTVhK2o3fWvOtJHar1a_Gi_wTE4HwsoS6noWdUHBRFdBExZ8QLFFImGbWpccoZ8tjfpRDl7EEddmBmryOsW0Rlc3o5UpHweIuFqiPHSTh0mbY3nj7NbNnytKM8rvsAyFpz3ckVvmqbNgB4LqxZOYRlZAcMC0Erqa-xcG3speXJlB5jSNPh1KpI2oN9Ou01acsMBpD9g-JoBRDh25ignXP43uSYiQkz7_2Z--5fT5_OjIbhtW69sDuJ0LOw1_cZ_gvf4k2nesPCQ3A01EBJpKPUdLVmxAfHN0KNvX87TMyQmZFHKzQl-_MkclGOHyXKxOvPvmzQhTbB7d96WitVth_ALgiCh-3J4z4rzHEsGsHQXdJ8ahzSBLu70fk7g75KTn5VZ-DPYrfQq4aU3yosA0YSNzg39EyY1x1pXDCBz09cwji4FlYX3db6WsisxhTlv7ZYw1EjHbMQ2OlzIx4uaQdCOb6j0XvsQDwBgZOIuUdALm4rs2yEkK9JClxB_9F2onReIgDsFoEZdQAtsnph9eTQj7nrQ6hBJ7Egf5vlnQSk=w954-h198-no)

# Right Outer Join
### The output is comprised of . . .  
- **All rows** of the **right** table, _even if they do not satisfy the matching condition_
- The **matching rows** of the **left** table 
- `NULL` in the spaces that come from the **left** table _where the matching condition is not satisfied_


### In the code below . . .
```
FROM Orders RIGHT JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
```
. . . **All records** from the **right** table and **matching rows** from the **left** table are highlighted below
![Image](https://lh3.googleusercontent.com/-Bko_5vSw9O0TyAhO_1mH_4Gm54fiLISZLniYXDyp-DUaOimGjUjcc-4bmA1FHwDrS-zjCToTxtO9vta3Ku4cz_kwvj-MMeV-n0Z241yer3aht_MXLYEny83QMXDPnC7-ed24XW-8lsh76btQkGOpMuv0EZOAIU9pMCLfq1gue41jHeTL9JGyczpRtZXTpSFNFfVs9mlvgGrilF2XGvEYz52m0wVQsZuyGyxiSlIvn7SvNPsF8j2CPIMRAeS1iw5mQElPf91FMub3LMQaXIi6EWhU3ZJTOm0faix_SJha3JcGFjI__HuB98bkKzWnBFt21SHkrBQsBXTE54UtMLEQcHst6mFzxHxf_02UJLveKJggm-UeLjw4FqgfAKUCSwOD_htncjWEWtAAsZ_JfiEWmSKORxSB0Y-aUAD43OyW84JZxBE3663APmu5IiqlHoMWIFPiNXYjDZtglYUodpUv1tbGV5qDktmnLimEFxvHBNsbwtNL9bfIVnv3WJ2qtTHHVKjut6JFBHXMU6eGtGjtSjXigd7p5fG1REenguk0nrTOS1JeDDQD5lCIlGVUmmnAt852NbKlJuDPwWQDwDuqiVYaoz7ic9_ziGi1UBayILg-CqqNiXUKYZgqUhv8RLPBejIWHO5BoeWXN-T9vu7qUQ3y0bYsgkr=w1399-h173-no)

