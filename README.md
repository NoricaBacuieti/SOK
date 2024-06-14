# SoK: Practices employed in the neural cryptanalysis of ciphers

This is the GitHub for my thesis **SoK: Practices employed in the neural cryptanalysis of ciphers**.

## Code 
To obtain the results from the thesis:
1. **Question 1 and 2:** Run all cells from top to before the results, as well as the cells in the Question 1 and 2 sections.
2. **Question 3 and 4:**
    - Run all cells from the top until before the results, as well as the cells in the Question 3 and 4 sections in the no-tuning case.
    - For the tuning case, if wished increase the number of max_trials in the tuner in the Train and evaluate section to explore more.
4. **Question 5 and 6:** Run all cells from top to before the results except the Train section, as well as the cells in the Question 5 and 6 sections.
5. **Question 7:**
    - Run all cells from the top to before the results.
    - Start running the cells in Question 7 until the cloning of the repository.
    - After cloning it, go to nnbits/models/org_gohr.py and instead of metrics='acc' modify it to metrics=['acc']
    - The code is written for Simon-9R. To change that, simply modify the cipher, number of rounds, and input difference (which can be taken from the experiments above).
    - If you use the same hardware as mentioned above, you can run the code as is, except for the marked sections where you need to change the names of your files.
    - If you do not use the same hardware, please follow instructions on how to change the hardware specifications in the code by following the explanations in https://github.com/Crypto-TII/nnbits/blob/main/README.md
    - For creating the figures from the thesis, after you obtain the bit-test_acc, you need to introduce them as specified in the test_accuracies_dict - also change the name of your plot as needed.
    - Continue running the code until the final cell to otain the recovered accuracies.

*To (re)compute the input differences obtained with the evolutionary optimizer, please download the repository from https://github.com/Crypto-TII/AutoND and follow the instructions provided in the readme.  

## Hardware requirements 
1. For experiments 1-6:   Use **1 GPU:** 64 CPU cores, 96 GB Sys RAM, 24/48 GB per GPU RAM, 200 GB disk memory 
2. For experiment 7:      Use **6 GPUs:** 128 CPU cores, 516 GB Sys RAM, 24/48 GB per GPU RAM, 200 GB disk memory

* Machines can be rented from VAST.ai for experiments: Image: tensorflow/tensorflow, Template: Tensorflow latest, Image cuda version: 12.3
* For experiments using DBIT, there are library incompatibilities due to the images available, so run the code on Google Colab using the A100 GPU, which can also be rented.

## Libraries
Aside from the libraries used in the two repositories that you will download (specified in their readme's), I have used:
1. Python 3.10.12
2. Tensorflow 2.15.0
3. Keras 3.0.5
4. Keras-tuner 1.4.7
5. Scipy 1.13.1
6. Pandas 2.2.2
7. Tqdm 4.66.4
8. Click 8.1.7
9. Numpy 1.26.4
10. Scikit-learn 1.5.0
11. H5py 0.0.7

