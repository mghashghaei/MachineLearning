# MachineLearning
Machin Learning Course
Neural Networks: Handwritten Digit Recognition Lab
Embarking on my second narrative in the Machine Learning class, I aim to share my exploration into the fascinating world of neural networks, particularly focusing on the challenge of recognizing handwritten digits. This assignment marks a pivotal point in my learning journey, pushing the boundaries of my knowledge and skills in machine learning.

Experiment Objective
The core objective of this experiment is to delve into the complexities of neural networks and apply them to the task of recognizing handwritten digits from 0 to 9. Through this, we aim to understand the mechanisms that enable machines to interpret human handwriting, a task that involves pattern recognition, learning, and a deep understanding of neural network architectures.

Experiment Steps
Problem Statement: We begin by defining the challenge at hand—developing a neural network capable of identifying handwritten digits. This involves understanding the nuances of how digits are represented and the variability in human handwriting.

Dataset Exploration: The next step involves loading and exploring the dataset comprising images of handwritten digits. We'll analyze the characteristics of the data, understanding the input that will be fed into our neural network.

 # Load data stored in arrays X, y from data folder (ex3data1.mat)
 data = loadmat(os.path.join('Data', 'ex3data1.mat'))
 X, y = data['X'], data['y']
 # set the zero digit to 0, rather than its mapped 10 in this dataset
 # This is an artifact due to the fact that this dataset was used in 
 # MATLAB where there is no index 0
 y[y == 10] = 0
Data Visualization: Visualizing the dataset is crucial. It allows us to see the diversity in handwriting styles and to grasp the challenge that our neural network must overcome to accurately recognize these digits.

Neural Network Theory: Before implementing the neural network, we'll revisit the theoretical foundations that underpin neural networks, including activation functions like ReLU and softmax, which are essential for our model's learning process.

 # UNQ_C2
 # GRADED CELL: Sequential model
 tf.random.set_seed(1234) # for consistent results
 model = Sequential(
     [               
         ### START CODE HERE ### 
         
         tf.keras.layers.InputLayer((400,)),
         Dense(25, activation = 'relu', name="L1"),
         Dense(15, activation = 'relu', name="L2"),
         Dense(10, activation = 'linear', name="L3"),        
 
         ### END CODE HERE ### 
     ], name = "my_model" 
 )
Model Implementation: With a solid theoretical foundation, we proceed to implement the neural network model. This includes defining the architecture, layers, and activation functions to be used in our model.

Training the Model: The most exciting phase—training the neural network. We'll iteratively adjust the model's parameters based on the feedback from the cost function, aiming to improve the accuracy of our digit recognition.

Model Evaluation: After training, we'll evaluate the model's performance, visualizing its ability to recognize handwritten digits on unseen data. This step allows us to assess the effectiveness of our neural network.

Making Predictions: Finally, we'll use our trained model to make predictions on new, unseen handwritten digits. This will showcase the practical applicability of our model in real-world scenarios.

Conclusion
Through this experiment, I've gained a deeper understanding of neural networks and their powerful application in recognizing handwritten digits. This journey has not only enhanced my technical skills but also sparked a curiosity to explore more complex machine learning challenges. The foundational knowledge gained here paves the way for future explorations into the vast and evolving field of machine learning.
