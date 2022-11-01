# EE746-Project
This repository contains the code and the relavant material for the course project
| Group Number | Members                 |                     |                      | Allotment                                                    | Mentor |
| ------------ | ----------------------- | ------------------- | -------------------- | ------------------------------------------------------------ | ------ |
| 6            | Akshay Ganesh Iyer Iyer | Abhiram Naidu Mullu | Harsh Vinayak Borkar | 4- time/order sensitive readout layer in LSMs (HMMs, one/two layer BPTT etc.) | Anmol  |

Background :

* Liquid State Machines are a naturally recurrent form of neural network processing that is especially suitable for time-series data
* The decision is made by a linear readout layer that typically takes spike-rates of the liquid/reservoir neurons as input
* The can be enhanced by implementing modulated STDP in the input and recurrent connections
* The LSM is takes time-series of spikes as input and produces time-series of spikes as output, however there is not really an established method to take advantage of the “ordered” nature of the output for classification

**Stage I** 

Code LSM + STDP (ref 1) and verify idea on a small speech dataset - by partitioning the output time-series into a given number of partitions and concatenating the output spike-rates into an expanded number of output features(GPU-compatible tf code for simple LSM processing is available as a starting point)

**Stage II:**

Expand to other methods of readout like Hidden Markov Models, 1 or 2 layer shallow recurrent spiking network with Backprop through time (ref 3) etc., work on the larger google speech dataset

References :

1. https://arxiv.org/abs/2111.01760
2. https://www.frontiersin.org/articles/10.3389/fnins.2018.00524/full
3. https://arxiv.org/pdf/1803.09574.pdf

