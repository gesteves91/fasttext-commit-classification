# fastText Commit Classification

This replication repository is designed to offer an architecture to classify commits into software categories.

## Important Notes about this Replication Repository

1. Running your classifier using fastText

    You can run your fastText classifier using the labeled data. The data is stored inside the folder **data** named **commits-labeled.txt**. Keep in mind you need to have fastText installed in your machine.

    For Linux and Mac distributions, you may execute the following command in the terminal as long as pip is ready:

    ```text
    pip install fasttext
    ```

    For more details about fastText installation, you can point to this [link](https://github.com/facebookresearch/fastText). There, Facebook provides many installation possibilities you can use to have fastText ready in your machine. We always recommend the latest version, as new features are constantly being introduced to the project.

    After the proper installation of fastText, you may execute the following steps to create your classifier:

    * Preprocess the data

    ```text
    cat commits-labeled.txt | sed -e "s/\([.\!?,'/()]\)/ \1 /g" | tr "[:upper:]" "[:lower:]" > commits.preprocessed.total.txt
    ```

    * Create the classifier

    ```text
    ./fasttext supervised -input commits.train -output commits -autotune-validation commits.valid
    ```

    By default, the command above uses the f-score as the evaluation metric.

    The tests with the provided dataset and fastText has proven to very effective to the commit problem, as the f-score achieved on average as around **91%**. 

    *Note that you may experience different f-score numbers per execution. It is recommended to run the script a certain number of times and then extract the average of the executions. The numbers are not expected to disperse a lot from the reported number though.*

2. Classification using fastText

    Inside the folder **notebooks**, there is the main notebook called **classification.ipynb** in which shows an example of how to use fastText to classify software commits. In the specific example, the data can be downloaded from this [link](www.google.com). Then, we may store the downloaded dataset into the **data** folder.

If you have any questions do not hesitate on contacting me at geanderson@dcc.ufmg.br




