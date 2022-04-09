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


### Notes
When serializing tensor proto, there is a hardlimit of 2GB. This issue is obtained when trying to encrypt weights directly. To solve this, use np.dsplit() to split the weights into equal arrays, and then encrypt each array individually. To combine them into the original weights, use np.dstack(). Due to limited RAM, I used a dsplit indice of 16.  
This is applicable for Bob_training.ipynb and Alice_training.ipynb.  

### Dependencies
See requirements.txt. Can be installed with pip.

### Please cite the following if you use the code:
@misc{miarM2DAJR,
  title={Notebook for implementing a simple 2-client model of homomorphic encryption and secure aggregation in Federated Learning},
  author={Dave, Appadoo and Jyotika, Rughoo},
  journal={https://https://github.com/azezezaaa/MIAR_M2/},
  year={2021}
}
