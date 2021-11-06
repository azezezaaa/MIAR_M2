# MIAR_M2
This repository contains the code for the implementation on Homomorphic Encryption, Federated Learning and Secure Aggregation. Implemented Homomorphic Encryption schemes are Tenseal's CKKS and a simple modfified version of Gentry's HE.

## Brief
There are 4 jupyter notebooks:
<ol>
  <li>server_training.ipynb</li>
    > server_training.ipynb contains the code to generate the base model and saves it in the current directory.
  <li>Bob_training.ipynb</li>
   > Bob_training.ipynb contains the code to generate Bob's part of the MNIST dataset, run the base model, extract, encrypt and serialize weights, and store these weights in a pickle file.
  <li>Alice_training.ipynb</li>
     > Alice_training.ipynb contains the code to generate Alice's part of the MNIST dataset, run the base model, extract, encrypt and serialize weights, and store these weights in a pickle file.
  <li>server_training_new_weights.ipynb</li>
    > server_training_new_weights.ipynb reads the encrypted weights, average the two users' encrypted weights and updates the base model. 
</ol> 
