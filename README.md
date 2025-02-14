# Encrypted decision tree implementation on FPGA with sequential circuit

This repository contains the source code to reproduce the results of our paper:

`Karn, Rupesh Raj, Kashif Nawaz, and Ibrahim Abe M. Elfadel. "Securing Decision Tree Inference Using Order-Preserving Cryptography." In 2023 IEEE 5th International Conference on Artificial Intelligence Circuits and Systems (AICAS), pp. 1-5. IEEE, 2023.`.

Four folders are provided, two for the encrypted and another two for the unencrypted decision tree, where one is for combinational and another is for sequential circuit. The video demonstration is attached in each folder to showcase the steps used in the confidential inference. 

A Jupyter notebook file titled `OPE _ ORE MNIST Decision Tree <sequential/combinational>.ipynb` in the each folder shows the source code to for encryption using order-preserving cryptography. 

The source code to generate HDL (Verilog) and do the software verification post encryption is in notebook file `OPE MNIST Decision Tree FSM Generator.ipynb`.

Dependency:
- MNIST dataset (or Tensorflow/Keras)
- Sklearn
- Quartus Design suite
- DE-10 Standard FPGA
- USB to serial converter
- Anaconda


The process is as follows:
1. Start from the Jupyter Notebook to train the decision tree model with Sklearn.
2. Extract the `combination/sequential` circuit's HDL (Verilog) source code.
3. Transport the HDL to Quartus and do synthesis.
4. Upload the sof file in FPGA.
5. Test the inference using the jupyter notebook (serial library). 


![alt text](https://github.com/rkarn/Encrypted-Decision-Tree-Sequential/blob/main/DecisionTree_Comb_ENC_GPIO_UART/OPE/Setup.jpg)
