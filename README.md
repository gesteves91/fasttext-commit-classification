# fastText Commit Classification

This replication repository is designed to offer an architecture to classify commits into software categories.

## Important Notes about this Replication Repository

1. Running your classifier using fastText

    You can run your fastText classifier using the labeled data. The data is stored inside the folder **data** named **commits-labeled.txt**. Keep in mind you need to have fastText installed in your machine.

    For UNIX-based distributions, you may execute the following command to extract the latest fastText version:

    ```bash
    wget https://github.com/facebookresearch/fastText/archive/v0.9.2.zip
    ```

    Then, extract the archive with the following command:

    ```bash
    unzip v0.9.2.zip
    ```

    After extracting the zip file, you can execute the following command to install fastText:

    ```bash
    cd fastText-0.9.2
    make
    pip install .
    ```
    For more details about fastText installation, you can point to this [link](https://github.com/facebookresearch/fastText). There, Facebook provides many installation possibilities you can use to have fastText ready in your machine. We always recommend the latest version, as new features are constantly being introduced to the project.

    **Data file**

    The data file is stored in the **data** folder. The file is called **commits-labeled.txt**.

    **Machine Learning Model**

    The machine learning model is stored in the **model** folder. The model is called **model.bin**. 

    **Recommended Package**

    We recommend the following packages for testing the model:

    ```bash
    pip install pandas
    pip install fasttext
    ```

    *Note that you may experience different f-score numbers per execution. It is recommended to run the script a certain number of times and then extract the average of the executions. The numbers are not expected to disperse a lot from the reported number though.*

    *We strongly recommend to auto-tuning the hyper-parameters of the model.*

2. Classification using fastText

    Inside the folder **notebooks**, there is the main notebook called **classification.ipynb** in which shows an example of how to use fastText to classify software commits. In the specific example, the complete data can be downloaded from this [link](https://bit.ly/commitsfile). Then, we may store the downloaded dataset into the **data** folder. Otherwise, we can use the commits.csv file provided in the data folder. Note that the available file has only 50000 commits, as GitHub does not allow files bigger than 10 MB. 

If you have any questions do not hesitate on contacting me at geanderson@dcc.ufmg.br




