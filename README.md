# Charity Analysis (Neural Network)
## Overview
The purpose of this analysis is to try to predict if an organization that receives funding a company called  Alphabet Soup (a charity funds organization) is prone to use properly the money received.

The used database comprises of 36000 rows and 12 features, and a Deep Neural Network was chosen to try to predict this outcome.

## Results
Below is a snapshot of the database:

![Screen Shot 2021-03-14 at 10 42 57 PM](https://user-images.githubusercontent.com/72593264/111100833-a0e3f200-8516-11eb-9289-83737582bc5c.png)

Here are some of the proceess and results:

### Data Preprocessing
- The variable that was chosen as the target was the fetaure "IS_SUCCESSFUL", that indicated applicants that properly managed the funds directed to them.
- The features that were chosen as significants to the predicition were: 

    APPLICATION_TYPE  
AFFILIATION           
CLASSIFICATION        
USE_CASE              
ORGANIZATION          
INCOME_AMT            
ASK_AMT
STATUS
SPECIAL_CONSIDERATION

- Two categorical features were dismissed as they did not have relevant information (NAME and EIN).


### Compiling, Training and Evaluating the Model
- For this Deep Learning model, these were the main characteristics:

    - Neurons used: 130, divided in 3 layers (80, 30, 20), plus one output layer.
    
    - The activation functions used were the ReLU on the first three layers, and a Sigmoid function on the output layer. The ReLU was chosen for the first layers it is a efficient activation formula. The Sigmoid was chosen for the output layer for its capacity in giving a yes or no result.

    - The target model performance was of **75%** of accuracy.
    Unfortunately, this model only reached **73%** of accuracy.

    ![Screen Shot 2021-03-14 at 11 05 56 PM](https://user-images.githubusercontent.com/72593264/111102341-d8a06900-8519-11eb-9e7d-86e039b8345b.png)

## Optimization 

Some steps were made to improve the model's accuracy, to no avail.
- Two additional features - STATUS and SPECIAL_CONSIDERATIONS - were removed because were found not to have a statistical value, as shown below by their values counts.

    ![Screen Shot 2021-03-14 at 10 51 21 PM](https://user-images.githubusercontent.com/72593264/111101406-d0472e80-8517-11eb-859d-b1dbfabb270f.png)

    ![Screen Shot 2021-03-14 at 10 51 53 PM](https://user-images.githubusercontent.com/72593264/111101433-e05f0e00-8517-11eb-84b3-2eda4260e2d5.png)

- The number of interactions inside the neural network (Epochs) were increased from 50 to 100.

- Other activation functions were used to give more accuracy to the model, such as changing the Sigmoid function with the TanH function.

All these efforts resulted, when applied separetly, in actually a small decrease in accuracy, and combined, reached the same plateau as the original model: **73%** accuracy, as below:


![Screen Shot 2021-03-14 at 11 15 38 PM](https://user-images.githubusercontent.com/72593264/111102914-31bccc80-851b-11eb-9cd8-3e08dc6e2a3b.png)

## Summary
Overall, the results of the Neural Network model projected were close to achieve the expectation. 
Ususal optimizations to the model falied to improve accuracy.
Since this a tabular database, I suggest trying other classification methods, such as Random Forest, to see if it achieves the expected accuracy.


