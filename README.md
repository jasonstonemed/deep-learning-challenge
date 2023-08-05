# Alphabet Soup Neural Network Project

Overview of the analysis: Alphabet Soup is a non-profit organization that has funded more than 34,000 organizations. The goal is to develop a neural network model that can produce a binary outcome, predicting success of its philanthropic efforts.

Data Preprocessing:
Target value for the model: ‘IS_SUCCESSFUL’
Features of the model: AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZARION, INCOME_AMT, ASK_AMT, and IS_SUCCESSFUL
Variables removed: EIN, NAME, STATUS, and SPECIAL_CONSIDERATIONS

Compiling, Training, and Evaluating the Model
  o	The model consisted of three layers. The layers were included with the starter code and this was used as a starting point in the model.
    1.	Input later – 5 neurons, relu activation, with dim_input= 14574 (after reducing the data set to 25,000 rows)
    2.	Hidden layer - 5 neurons, relu activation
    3.	Output layer – 1 neuron with sigmoid activation
   
Were you able to achieve the target model performance? Yes, my model performed at 0.774  accuracy and 0.77 loss.
  
What steps did you take in your attempts to increase model performance? 

After several crashes in Google Collab, I gradually reduced the sample size of approximately 34,000 to 25,000 where the model would no longer crash. I started just by playing with neurons and layers to see the effect without making major changes otherwise. The effects were unpredictable and not close to the target, so columns STATUS, and SPECIAL_CONSIDERATIONS were removed.
Once the columns were removed, I ran the model at 100 epochs. The accuracy was still increasing so the model was ran again at 105 epochs resulting in 0.774  accuracy with 0.72 loss. Attempts at manipulating the neuron layers after obtaining 0.772 only introduced volatility into the model, so neuron/layer configuration remained at the original levels from the starter_code as described previously.

Summary: After dropping columns and experimenting with number of epochs, I was able to achieve 77.4% accuracy with 0.72 loss. I changed no other hyperparameters were modified from the starter_code.Based upon the relatively small data set size (25000x8), I suggest that that a neural network model is too complex for a data set of this size and complexity. A supervised learning model such as RandomForest would appear to provide sufficient capacity necessary to run the analysis with increased reproducability and a decreased tendency to overfit. This would also be much more efficient in terms of time and computational resources.

