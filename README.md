# ML_procurement-spend_efficiency
- Dataset link-->Spend_analytics-->[https://drive.google.com/drive/folders/1k_drkNGurClzJJMQQIYflM3tOx3HBKQr]
## Project Overview
### Project demo -[https://drive.google.com/file/d/1QNijgvDbhtMA7xZK7FV_5Y-uKa4eIVqE/view?usp=sharing]
- This aim of this project is to create the dependent(target) variable by analyzing the dataset and build a ML classification model to classify whether the procurement team has made an efficient(0) or ineffficient(1) spend while procuring materials for a broiler chicken farming company.

- ## Classification ROCAUC score and Accuracy Table for oversampled dataset
|    Model             |  Train(ROC-AUC)   |  Test(ROC-AUC)   |Accuracy |Confusion matrix
| :------------------- | -----------------  |-----------------|-----------------|-----------------:  
| LogisticRegression    |      0.900         |0.868             |0.800|   [[7457  4260]   |
|      -         |-             |-| -|                                           [ 757   12615]]    |
| RandomForestClassifier|      0.995         |0.981              |0.921      |[[9203 2514]| 
|      -        |         -     |   -   |      -|          [ 309  13063]]|
| XGBClassifier             |      0.990         |0.980              |0.922 |[[10078   1639]             |
|     -         |-              |- |-                            | [329   13043]]| 

- **XGBClassifier** has performed well to classify spend efficiency
## Results
- The most important features to optimize when procuring materials are -**'avg_net_price' ,'NCM Code','Material','Net Price', 'Short Text','Non-deductible','Purch.Doc.'**
### Strategies to follow
- Determine the net price of the material that needs to be purchased,inquiring various suppliers and find the average net price, confirm the order to the supplier who quotes the net 
  price below or equal to the average net price.
- Increase the count of suppliers by finding new guys in the market,purchasing from the same supplier may cause the net price to increase over time.
- Purchase materials in bulk,monitoring when that particular material's cost goes lower in a given year.
- Use the **'NCM Code'** to find the cost of material in the market and if it is relatively lower than the **'net price'** quoted by the supplier,try to find and purchase from a new supplier.
- Finally create a purchase document which is optimized considering the above said strategies to make an 'effective spend'
## Hope the results are good!!!


