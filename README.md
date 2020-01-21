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

![Image](/img1.png)

![Image](/img2.png)

### The `SELECT` statement shows which columns between the two tables are going to be included in the output:
```
SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
```
![Image](/img4.png)

![Image](img42.png)

### In the code below . . .
```
FROM Orders LEFT JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
```
. . . **All records** from the **left** table and **matching rows** from the **right** table are highlighted below

![Image](/img5.png)


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


### Continuing the example from before, in the code below . . .
```
FROM Orders RIGHT JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
```
. . . **All records** from the **right** table and **matching rows** from the **left** table are highlighted below

![Image](https://lh3.googleusercontent.com/-Bko_5vSw9O0TyAhO_1mH_4Gm54fiLISZLniYXDyp-DUaOimGjUjcc-4bmA1FHwDrS-zjCToTxtO9vta3Ku4cz_kwvj-MMeV-n0Z241yer3aht_MXLYEny83QMXDPnC7-ed24XW-8lsh76btQkGOpMuv0EZOAIU9pMCLfq1gue41jHeTL9JGyczpRtZXTpSFNFfVs9mlvgGrilF2XGvEYz52m0wVQsZuyGyxiSlIvn7SvNPsF8j2CPIMRAeS1iw5mQElPf91FMub3LMQaXIi6EWhU3ZJTOm0faix_SJha3JcGFjI__HuB98bkKzWnBFt21SHkrBQsBXTE54UtMLEQcHst6mFzxHxf_02UJLveKJggm-UeLjw4FqgfAKUCSwOD_htncjWEWtAAsZ_JfiEWmSKORxSB0Y-aUAD43OyW84JZxBE3663APmu5IiqlHoMWIFPiNXYjDZtglYUodpUv1tbGV5qDktmnLimEFxvHBNsbwtNL9bfIVnv3WJ2qtTHHVKjut6JFBHXMU6eGtGjtSjXigd7p5fG1REenguk0nrTOS1JeDDQD5lCIlGVUmmnAt852NbKlJuDPwWQDwDuqiVYaoz7ic9_ziGi1UBayILg-CqqNiXUKYZgqUhv8RLPBejIWHO5BoeWXN-T9vu7qUQ3y0bYsgkr=w1399-h173-no)

### Together, the query below . . .
```
SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
FROM Orders RIGHT JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
```
### . . . results in the following output:

![Image](https://lh3.googleusercontent.com/hIMRaROa9uoIewcCIaZUU16QHtMnnJN60P3gfCJGTavQxdrOgM8h7rxjrw_gRW_rgCoJ6UnXChRjAJpAbLqOMtQSYGtA2amzSQ7hLujOKANcajQ_R7daRyA2YVueajS0dBN3unf2884YTj1ay0eceDyu6ohDnaDQBqvjBK9t8-Acg8xxKUfAJ8yhFyoNPyabCNc6kMUnxpW0oRVKWdTNBAw_Y2P8NgB02yuuTCuH971lwUwDT0rfHQu6G-v-g8Bu7c4z7ewRKZXikugo9f4tiLI1vasQw11jpa5kuIrLRrUe4ere8KAEQPHMyOXj1vQ-2PtrG6Jfi8DaImNc3gQKjlAIHMALx4ej_CA8rOI1B-xsWzAZsG--Rwm93wFc3gZcRpKKLo8HigXr24eUUBsMKgMZoMi88pDH0fWCpUQ2rMwP-e9Sc4Qi9udiU15gNlHgu5Fyili9m_knNlPBzODQpu5hjJQAWbFdMqbUU_EKnfrFkwnTgAOoIh0LEpffBEaEk1zSStmretDL1xmY7T-l-FfFmznE_tMUeU0rY_3_P1DLm-Vp490Lj9N-3izKW3L_fb0nFrdGxPOcu6ZzZnwD0Hc_dWRXcurJ6AotEQQuWRpKe7yiVukprSxinPwwu3XffwRfygX5pV9cgSJCuU4F3Iyfwyj3kc-K=w966-h199-no)

