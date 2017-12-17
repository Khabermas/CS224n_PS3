# Named Entity Recognition

## Assignment 3 from Stanford NLP class Spring 2017



## **1. A Window Model**

Works as it is supposed to.



## **2. Recurrent neural nets for NLP**


The tests work fine.
 - python q2_rnn_cell.py test
 - python q2_rnn.py test1
 - python q2_rnn.py test2


**Training the model** ( python q2_rnn.py train)

> Train your model using the command python q2_rnn.py train. Training
should take about 2 hours on your CPU and 10–20 minutes if you use the GPUs provided by
Microsoft Azure. You should get a development F 1 score of at least 85%.


On my _old_ computer (running on CPU of course, but with TensorFlow installed from source) it takes about 45 minutes.
Using the default parameters it trains for 10 epochs, tests on the dev set after each, and saves the best parameters (typically those from epoch 10).


The development entity-level F<sub>1</sub> score reaches 85%.
See results/rnn/<timestamp>/log


Then the program proceeds to the test set -- and 'freezes'.  Python continues to consume much of the machine's paltry 6 GB RAM, and some process seems to be running (but uses negligible CPU.  (The computer is so unresponsive it takes minutes just to open a new terminal and investigate with, e.g., top ).

The program can easily be aborted by closing the terminal window.  Anything that happens during that final aberrant phase is not recorded in the standard log.


## **3. GRU models**

Coded this.  Ran learning curves for RNN & GRU models with and without gradient clipping.  Generated .png images that will later be discussed in this README.  

Following 3(f) ran NER model from question 2 using GRU cell ( python q2_rnn.py train -c gru ).
Training ran, with some fits and starts, and not improving much after the 5th or 6th epoch -- then generated a process killed as it started the 9th epoch.  Another mystery to be explored.









