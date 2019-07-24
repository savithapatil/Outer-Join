# The Outer Join
- All the records of one table along with the matching records of another table make up the output
- Types:
  - Left Outer Join
  - Right Outer Join

## Left Outer Join
### The output is comprised of. . .  
- **All rows** of the **left** table, _even if they do not satisfy the matching condition_
- The **matching rows** of the **right** table 
- `NULL` in the spaces that come from the **right** table _where the matching condition is not satisfied_

## Here's an example

### Given two tables, called Orders and Customers, below


### In the code below. . .
```
FROM Orders LEFT JOIN Customers ON Orders.CustomerID=Customers.CustomerID;
```
. . .**All records** from the **left** table and **matching rows** from the **right** table are highlighted below

![Image](https://lh3.googleusercontent.com/-juqthadVSLm8fIrH0kzDSB67dQKFp0vwHmK4_-na6joD7d-zF-aTA752G9O-FEmsnTXJP7Zeq9sIsTwyLAYZeu5ZyUk1aapI7DP2die_vkZ2pC12as_UyNgQ1E1dTM2r7EqhRx1ci5W68DrEDmoUalEUoivDIc5FQ-zUwxBOU2AYgHkr4UfisVu2VDvKX_5eJC-Am5KmNAssWK3ehMbcY_TF0cE2oiGwwVCzCERplKA1rqJHXZw29BU72sYt0c4GhT3ACPxZGxLMXdENFRJcuBDSxnjR78tTJ6LbfUwPDSpWEgDm3CSDngIWhrcGdzbdXE93re1F48YaAX3eA_eEY-b0RRo7nrMd-m3WC0R0nFdCHVW4FOAne7AXFojFhyCMU68ftRbLbokiho0Ny3yNPEHrMuJC50kQbf3369oDv9tCAsCiChhJXjk82zlavBU90VedHfMIyZGGEfOOyLghAWk_5priDijvG2aFds_lD6JPenwmIQ78FnG1yCrk22Sylvc6BJGMMSAto1a-mhoMuFQgzX9CZf5MblMyaD7A6cs_EYWN6Zizdd8XBXLJP8lRSeDJV19C26FMoX6cMYHSmIhlsQ15O1fmwkDl-bUPWTUmUgM9u-0WV8FvRkD_ukyeyIE6_f1Hg6nIqjFe5eBa3JGb0fovsHf=w1395-h173-no)


### The query below. . .
``` 
SELECT Orders.OrderID, Customers.CustomerName, Orders.OrderDate
```
### . . .results in the following output:

![Image]()

## Right Outer Join
### The output is comprised of. . .  
- **All rows** of the **right** table, _even if they do not satisfy the matching condition_
- The **matching rows** of the **left** table 
- `NULL` in the spaces that come from the **left** table _where the matching condition is not satisfied_

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/savithapatil/Outer-Join/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
