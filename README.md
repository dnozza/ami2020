# ami2020
Official repository of [AMI](https://amievalita2020.github.io/#about), the shared task on Automatic Misogyny Identification at [Evalita 2020](http://www.evalita.it/).

Training and testing set available filling in this [form](https://forms.gle/uFF3sAtMMqayiDiz9); an email notification will be sent with instructions and details about how to download the data.

For more information on the task, see the guidelines available in this repository, and the [task web page](https://amievalita2020.github.io/#about).

## Evaluation Script Installation

### Dependencies

To install the required python packages, run:

```
pip install -r requirements.txt
```

In the case of problems, try to run ```pip install --upgrade pip setuptools```
first.

## Evaluation Script Usage

The evaluation script can be used for evaluating the results both of Subtask A and B given a zip file containing submission files as input. For submission files formats check the [AMI 2020 Guidelines](https://github.com/dnozza/ami2020/blob/master/AMI%202020%20-%20Guidelines.pdf).

### Subtask A - Misogyny & Aggressive Behaviour Identification

For running the evaluation script for Subtask A, you can run something like the following:

```bash
python evaluation_submission.py \
--submission_path teamName.zip \
--gold_path_raw AMI2020_TrainingSet/AMI2020_TrainingSet.tsv \
--task a \
--output_path result.tsv 
```


### Subtask B - Unbiased Misogyny Identification

For running the evaluation script for Subtask B, you can run something like the following:

```bash
python evaluation_submission.py \
--submission_path teamName.zip \
--gold_path_raw AMI2020_TrainingSet/AMI2020_TrainingSet.tsv \
--gold_path_synt AMI2020_TrainingSet/AMI2020_training_synt.tsv \
--identityterms_path AMI2020_TrainingSet/AMI2020_training_identityterms.txt \
--task b \
--output_path result.tsv
```

## References

::

    @inproceedings{Fersini2020, 
      author = {Elisabetta Fersini, Debora Nozza, Paolo Rosso},
      title = {AMI @ EVALITA2020: Automatic Misogyny Identification},
      booktitle = {{Proceedings of the 7th evaluation campaign of Natural Language Processing and Speech tools for Italian (EVALITA 2020)}},
      editor = {Basile, Valerio and Croce, Danilo and Di Maro, Maria and Passaro, Lucia C.},
      year = {2020},
      publisher = {CEUR.org},
      address = {Online}
    }


## Contacts

If you find issues on the evaluation script, please contact **Debora Nozza**: [Twitter](https://twitter.com/debora_nozza) | [Github](https://github.com/dnozza) | [Webpage](https://dnozza.github.io)


[![licensebuttons by-nc-sa](https://licensebuttons.net/l/by-nc-sa/3.0/88x31.png)](https://creativecommons.org/licenses/by-nc-sa/4.0)
