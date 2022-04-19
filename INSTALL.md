The source codes and the results are placed in this repository.
- The source codes are categorized based on the experimental setup. We have proposed three different approaches to decompose a convolutional neural network (CNN) into modules. The source code of each technique has been carefully placed under the corresponding folder. For example, for `CI+TI+MC`, the code is in `Approach 1`. However, for the followup experiments, we use the second approach or 'Approach 2'. Within each folder, there are codes for all the datasets, CIFAR-10, CIFAR-100, and ImageNet-200. Since, for each dataset, we have used three different structure of the models, e.g., for CIFAR-10, ResNet-20, ResNet-32, and ResNet-56. For each experiment, we have the trained model and the decomposed modules saved. Since the training and decomposing takes significant time, the trained model and the modules can be reused by simply using the corresponding files. 
To rerun the result, one can use the scripts given in the `Scripts` folder. Please use the [requirements](./requirements.txt) to sync with the correct version of the library to execute the code.
- The experiments related to the [reuse](./Reuse) and the [replacement](./Replacement) are kept under the corresponding directory. Scripts have been provided to rerun the results; In may take a couple of hours to run the modules as there are cases where 200 modules will be running at a time (ImageNet-200 dataset).

## Example 1: Intra Reuse for CIFAR-10:
- Step 1: Go to the `Scripts` folder.
- Step 2: Execute `./Reuse.sh` on the terminal. It gives you the below options.
```
(base) user$ ./Reuse.sh.sh
Please choose the correct option for the experiment
1- CIFAR-10 Intra Reuse
2- CIFAR-100 Intra Reuse
3- ImageNet-200 Intra Reuse
4- CIFAR-10 vs. CIFAR-100 Reuse
```
- Step 3: Choose the right experiments from the list. For example, if we chose `CIFAR-10 Intra Reuse`, then please insert `1` for that option.

Once you choose the right option, e.g., `1` for our example, the code will execute for some time (it may be hours, based on the type of experiments chosen). At the end of the execution, the accuracy of the modules will be notified.
```
Modularized Accuracy: 0.9885
Completed: 1

It will keep on providing the output as it finishes the experiments.
