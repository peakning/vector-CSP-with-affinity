# Interpretation of the data 
Here, we give the dataset of the paper *vector cutting stock problem with affinity*.

All data is placed in the *dataset* folder. *group1_data* folder to *group10_data* folder contain the randomly generated instances mentioned in the paper. 

For each instance, its name follow the structure like *group1_instance_1.txt*, where *group1* means the index of the group and *instance_1* means the index of the instance. 

For the composition of the data for each instance:
- *Number of physical machine types* means that there are three physical machines of different specifications
- *Resources for each physical machine type* means available resources on each type of physical machine. Each row represents the available resources for a type of physical machine, and each column represents a specific resource type.
- *Available number for each physical machine type* means the number of activations of each type of physical machine.
- *Activation cost for each physical machine type* means the activation cost incurred by each type of physical machine when it is activated.
- *Number of micro-service types* means the number of types of micro-service.
- *Required number for each micro-service type* means the number of micro-services that need to be allocation for each type.
- *Resource requirements for each micro-service type* means the resources that each type of micro-service needs to consume.
- *Total invoking flow matrix* means the total invoking flow from micro-services *i* to *j*. In this matrix, each value means that the micro-service from the row number invokes the micro-service from the column number. For example, the second column of the first row of the matrix might be 449, which means that the micro-service *1* invokes the micro-service *2* a total of 449 times.

	