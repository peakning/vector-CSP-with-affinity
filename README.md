# Interpretation of our experiment data 
Here, we give the dataset of the paper **vector cutting stock problem with affinity**.



**All data is placed in the dataset folder.**
- **group1_data** folder to **group10_data** folder contain the randomly generated instances mentioned in the paper. Related parameters are shown on the following Table (**Table 1** and **Table 2** in our paper). 
  
    | Group | Number of micro-service types | Number of micro-service demand |
    |-------|-------------------------------|--------------------------------|
    | 1     | 5                             | [1,5]                          |
    | 2     | 5                             | [1,10]                         |
    | 3     | 10                            | [1,5]                          |
    | 4     | 10                            | [1,10]                         |
    | 5     | 20                            | [1,10]                         |
    | 6     | 20                            | [1,15]                         |
    | 7     | 30                            | [1,10]                         |
    | 8     | 30                            | [1,15]                         |
    | 9     | 40                            | [1,15]                         |
    | 10    | 40                            | [1,20]                         |

    | Parameter                                                  | Value                                 |
    |------------------------------------------------------------|---------------------------------------|
    | Type of physical machine                                   | $K=3$                                 |
    | Type of physical machine resources                         | $R=2$                                 |
    | Resource value of physical machine 1                       | $U_{1}=\{128,256\}$                   |
    | Resource value of physical machine 2                       | $U_{2}=\{64,256\}$                    |
    | Resource value of physical machine 3                       | $U_{3}=\{128,128\}$                   |
    | Cost of physical machine                                   | $C_{k}=\{200,150,150\}$               |
    | Number limitation of physical machine                      | $Q_{k}\in[1.1Z^{CSP}_k,1.3Z^{CSP}_k]$ |
    | Requirements of the resource $r$ for the micro-service $i$ | $b_{ir}\in[0.1U_{1r},0.3U_{1r}]$      |
    | Total invoking flow from micro-services $i$ to $j$     | $W_{ij}\in[0,1000]$                   |


- For each instance, its name follows the structure like **group1_instance_1.txt**, where **group1** means the index of the group and **instance_1** means the index of the instance. 
- Bytedance_cluster_data folder contains 4 clusters mentioned in the paper. Related parameters are shown on the following Table (**Table 9**, **Appendix B** and **Appendix C** in our paper). 

    | Cluster Name   | \# Service types | \# Whole services | \# Variables | \# Constraints |
    |----------------|------------------|-------------------|--------------|----------------|
    | Cluster 1 (M1) | 1739             | 3423              | 3025860      | 6049983        |
    | Cluster 2 (M2) | 2089             | 81380             | 4366010      | 8729933        |
    | Cluster 3 (M3) | 161              | 1367              | 26082        | 52005          |
    | Cluster 4 (M4) | 1702             | 48523             | 2898506      | 5795312        |

    | Cluster Name | M1              | M2              | M3              | M4              |
    |--------------|-----------------|-----------------|-----------------|-----------------|
    | $U_1$        | \{21940,14276\} | \{17005,8528\}  | \{15112,9170\}  | \{30334,22873\} |
    | $U_2$        | \{11043,10749\} | \{17043,17093\} | \{14990,18193\} | \{27095,40583\} |
    | $U_3$        | \{10939,28472\} | \{11495,34036\} | \{7532,9141\}   | \{15021,11327\} |
    | $C_k$        | \{180,100,200\} | \{100,180,200\} | \{180,200,100\} | \{200,180,100\} |
    | $b^{max}_r$  | \{1411,1127\}   | \{1513,832\}    | \{792,294\}     | \{1942,888\}    |
    | $b^{min}_r$  | \{17,4\}        | \{6,1\}         | \{131,128\}     | \{8,2\}         |

    | Subset Index | Number of service types | Number of whole services | Total invoking traffic |
    |--------------|-------------------------|--------------------------|------------------------|
    | M1-Subset1   | 613                     | 1282                     | 37367                  |
    | M1-Subset2   | 29                      | 32                       | 1379                   |
    | M1-Subset3   | 256                     | 532                      | 118139                 |
    | M1-Subset4   | 841                     | 1577                     | 280908                 |
    | M2-Subset1   | 730                     | 29060                    | 639246                 |
    | M2-Subset2   | 356                     | 14116                    | 115464                 |
    | M2-Subset3   | 403                     | 16572                    | 322368                 |
    | M2-Subset4   | 399                     | 8911                     | 47157                  |
    | M2-Subset5   | 154                     | 5230                     | 181812                 |
    | M2-Subset6   | 47                      | 7491                     | 648633                 |
    | M3-Total     | 161                     | 1367                     | 99994                  |
    | M4-Subset1   | 47                      | 532                      | 11892                  |
    | M4-Subset2   | 105                     | 1963                     | 31068                  |
    | M4-Subset3   | 716                     | 21034                    | 284962                 |
    | M4-Subset4   | 257                     | 10861                    | 536096                 |
    | M4-Subset5   | 303                     | 6247                     | 130132                 |
    | M4-Subset6   | 274                     | 7886                     | 90868                  |

- For each cluster, its name follow the structure like **M1_Subset1.txt**, where **M1** means the index of the cluster and **Subset1** means the index of the subset. Futhermore, if it contains **Total**, that means it represents the **whole** cluster.

**For the composition of the data for each instance:**
- **Number of physical machine types** means that there are three physical machines of different specifications
- **Resources for each physical machine type** means available resources on each type of physical machine. Each row represents the available resources for a type of physical machine, and each column represents a specific resource type.
- **Available number for each physical machine type** means the number of activations of each type of physical machine.
- **Activation cost for each physical machine type** means the activation cost incurred by each type of physical machine when it is activated.
- **Number of micro-service types** means the number of types of micro-service.
- **Required number for each micro-service type** means the number of micro-services that need to be allocation for each type.
- **Resource requirements for each micro-service type** means the resources that each type of micro-service needs to consume.
- **Total invoking flow matrix** means the total invoking flow from micro-services *i* to *j*. In this matrix, each value means that the micro-service from the row number invokes the micro-service from the column number. For example, the second column of the first row of the matrix might be 449, which means that the micro-service *1* invokes the micro-service *2* a total of 449 times.

	