---
layout: page
title: "Baseline"
permalink: /baseline
order : 1
---

# Baseline System
We have released a baseline system that fine-tunes the XLM-RoBERTa base model for each of the dataset.

[This code repository](https://github.com/amzn/multiconer-baseline) provides the baseline approach for Named Entity Recognition (NER). In this repository the following functionalities are provided:

* CoNLL data readers
* Usage of any HuggingFace pre-trained transformer models
* Training and Testing through Pytorch-Lightning


We expect, this baseline can be the starting point from where the participants can start building their own systems. 

# Baselines Results
For the baseline model performance in the development set, please check the <a href="https://competitions.codalab.org/competitions/36044#results" target="_blank">Codalab leaderboard</a>. Baseline submissions are made with the team name "MultiCoNER Baseline".

**Results on test set**

| **Track** | **Macro F1** |
|---|---|
| English | 0.612 |
| German | 0.634 |
| Spanish | 0.574 |
| Russian | 0.591 |
| Dutch | 0.616 |
| Korean | 0.546 |
| Farsi | 0.518 |
| Turkish | 0.457 |
| Chinese | 0.511 |
| Hindi | 0.469 |
| Bangla | 0.391 |
| Multi | 0.541 |
| Mix | 0.581 |

<!--
The following table presents the NER performance in different languages using the baseline system. For each language, we report the Precision (P), Recall (R), and F1 score in identifying each of the entity class label. Then we provide the micro averaged perforance on all the classes. 
Additionally, we report the performance on Mention Detection (MD), where the task is to only identify an entity boundaries regardless of the entity type.
Note that these results are for the development set.
-->

<br>

<!--table>
	<tr>
		<td></td>
        <td></td>
        <td><b>BN</b></td>
		<td><b>DE</b></td>
		<td><b>ES</b></td>
		<td><b>TR</b></td>
		<td><b>FA</b></td>
		<td><b>RU</b></td>
		<td><b>ZH</b></td>
		<td><b>NL</b></td>
		<td><b>KO</b></td>
		<td><b>EN</b></td>
		<td><b>HI</b></td>
	</tr>
	<tr>
        <td rowspan="3"><b>PROD</b></td>
		<td><b>P</b></td>
		<td>0.568</td>
		<td>0.77</td>
		<td>0.647</td>
		<td>0.651</td>
		<td>0.569</td>
		<td>0.675</td>
		<td>0.669</td>
		<td>0.639</td>
		<td>0.703</td>
		<td>0.643</td>
		<td>0.58</td>
	</tr>
	<tr>
		<td><b>R</b></td>
		<td>0.577</td>
		<td>0.805</td>
		<td>0.773</td>
		<td>0.701</td>
		<td>0.554</td>
		<td>0.733</td>
		<td>0.707</td>
		<td>0.717</td>
		<td>0.715</td>
		<td>0.687</td>
		<td>0.58</td>
	</tr>
	<tr>
		<td><b>F1</b></td>
		<td>0.572</td>
		<td>0.787</td>
		<td>0.704</td>
		<td>0.675</td>
		<td>0.561</td>
		<td>0.703</td>
		<td>0.687</td>
		<td>0.676</td>
		<td>0.709</td>
		<td>0.664</td>
		<td>0.58</td>
	</tr>
	<tr>
        <td rowspan="3"><b>GRP</b></td>
		<td><b>P</b></td>
		<td>0.722</td>
		<td>0.808</td>
		<td>0.698</td>
		<td>0.76</td>
		<td>0.718</td>
		<td>0.708</td>
		<td>0.667</td>
		<td>0.798</td>
		<td>0.776</td>
		<td>0.797</td>
		<td>0.806</td>
	</tr>
	<tr>
		<td><b>R</b></td>
		<td>0.703</td>
		<td>0.737</td>
		<td>0.702</td>
		<td>0.76</td>
		<td>0.762</td>
		<td>0.801</td>
		<td>0.48</td>
		<td>0.822</td>
		<td>0.733</td>
		<td>0.805</td>
		<td>0.703</td>
	</tr>
	<tr>
		<td><b>F1</b></td>
		<td>0.712</td>
		<td>0.771</td>
		<td>0.7</td>
		<td>0.76</td>
		<td>0.74</td>
		<td>0.752</td>
		<td>0.558</td>
		<td>0.81</td>
		<td>0.754</td>
		<td>0.801</td>
		<td>0.751</td>
	</tr>
	<tr>
        <td rowspan="3"><b>CORP</b></td>
		<td><b>P</b></td>
		<td>0.647</td>
		<td>0.741</td>
		<td>0.794</td>
		<td>0.833</td>
		<td>0.743</td>
		<td>0.779</td>
		<td>0.75</td>
		<td>0.841</td>
		<td>0.717</td>
		<td>0.794</td>
		<td>0.629</td>
	</tr>
	<tr>
		<td><b>R</b></td>
		<td>0.693</td>
		<td>0.782</td>
		<td>0.794</td>
		<td>0.845</td>
		<td>0.706</td>
		<td>0.799</td>
		<td>0.796</td>
		<td>0.779</td>
		<td>0.816</td>
		<td>0.777</td>
		<td>0.624</td>
	</tr>
	<tr>
		<td><b>F1</b></td>
		<td>0.669</td>
		<td>0.761</td>
		<td>0.794</td>
		<td>0.839</td>
		<td>0.724</td>
		<td>0.789</td>
		<td>0.772</td>
		<td>0.809</td>
		<td>0.763</td>
		<td>0.785</td>
		<td>0.626</td>
	</tr>
	<tr>
        <td rowspan="3"><b>CW</b></td>
		<td><b>P</b></td>
		<td>0.627</td>
		<td>0.73</td>
		<td>0.691</td>
		<td>0.694</td>
		<td>0.665</td>
		<td>0.719</td>
		<td>0.656</td>
		<td>0.696</td>
		<td>0.673</td>
		<td>0.644</td>
		<td>0.479</td>
	</tr>
	<tr>
		<td><b>R</b></td>
		<td>0.533</td>
		<td>0.688</td>
		<td>0.641</td>
		<td>0.679</td>
		<td>0.7</td>
		<td>0.732</td>
		<td>0.664</td>
		<td>0.731</td>
		<td>0.736</td>
		<td>0.597</td>
		<td>0.504</td>
	</tr>
	<tr>
		<td><b>F1</b></td>
		<td>0.577</td>
		<td>0.708</td>
		<td>0.665</td>
		<td>0.686</td>
		<td>0.682</td>
		<td>0.726</td>
		<td>0.66</td>
		<td>0.713</td>
		<td>0.703</td>
		<td>0.619</td>
		<td>0.491</td>
	</tr>
	<tr>
        <td rowspan="3"><b>PER</b></td>
		<td><b>P</b></td>
		<td>0.862</td>
		<td>0.913</td>
		<td>0.914</td>
		<td>0.822</td>
		<td>0.678</td>
		<td>0.744</td>
		<td>0.85</td>
		<td>0.871</td>
		<td>0.787</td>
		<td>0.912</td>
		<td>0.746</td>
	</tr>
	<tr>
		<td><b>R</b></td>
		<td>0.91</td>
		<td>0.922</td>
		<td>0.862</td>
		<td>0.857</td>
		<td>0.881</td>
		<td>0.802</td>
		<td>0.919</td>
		<td>0.892</td>
		<td>0.757</td>
		<td>0.928</td>
		<td>0.774</td>
	</tr>
	<tr>
		<td><b>F1</b></td>
		<td>0.885</td>
		<td>0.918</td>
		<td>0.887</td>
		<td>0.839</td>
		<td>0.766</td>
		<td>0.772</td>
		<td>0.883</td>
		<td>0.881</td>
		<td>0.771</td>
		<td>0.92</td>
		<td>0.76</td>
	</tr>
	<tr>
        <td rowspan="3"><b>LOC</b></td>
		<td><b>P</b></td>
		<td>0.745</td>
		<td>0.874</td>
		<td>0.827</td>
		<td>0.798</td>
		<td>0.809</td>
		<td>0.717</td>
		<td>0.89</td>
		<td>0.893</td>
		<td>0.783</td>
		<td>0.844</td>
		<td>0.636</td>
	</tr>
	<tr>
		<td><b>R</b></td>
		<td>0.812</td>
		<td>0.916</td>
		<td>0.836</td>
		<td>0.843</td>
		<td>0.849</td>
		<td>0.733</td>
		<td>0.856</td>
		<td>0.87</td>
		<td>0.798</td>
		<td>0.88</td>
		<td>0.786</td>
	</tr>
	<tr>
		<td><b>F1</b></td>
		<td>0.777</td>
		<td>0.894</td>
		<td>0.831</td>
		<td>0.82</td>
		<td>0.828</td>
		<td>0.725</td>
		<td>0.873</td>
		<td>0.881</td>
		<td>0.791</td>
		<td>0.862</td>
		<td>0.703</td>
	</tr>
    <tr>
        <td rowspan="3"><b>Micro Avg.</b></td>
		<td><b>P</b></td>
		<td>0.69</td>
		<td>0.825</td>
		<td>0.773</td>
		<td>0.767</td>
		<td>0.71</td>
		<td>0.724</td>
		<td>0.76</td>
		<td>0.803</td>
		<td>0.746</td>
		<td>0.794</td>
		<td>0.645</td>
	</tr>
	<tr>
		<td><b>R</b></td>
		<td>0.697</td>
		<td>0.83</td>
		<td>0.777</td>
		<td>0.792</td>
		<td>0.76</td>
		<td>0.766</td>
		<td>0.771</td>
		<td>0.814</td>
		<td>0.762</td>
		<td>0.8</td>
		<td>0.663</td>
	</tr>
	<tr>
		<td><b>F1</b></td>
		<td>0.694</td>
		<td>0.827</td>
		<td>0.775</td>
		<td>0.779</td>
		<td>0.734</td>
		<td>0.744</td>
		<td>0.765</td>
		<td>0.809</td>
		<td>0.754</td>
		<td>0.797</td>
		<td>0.654</td>
	</tr>
	<tr>
        <td rowspan="3"><b>MD</b></td>
		<td><b>P</b></td>
		<td>0.802</td>
		<td>0.912</td>
		<td>0.838</td>
		<td>0.802</td>
		<td>0.741</td>
		<td>0.767</td>
		<td>0.829</td>
		<td>0.857</td>
		<td>0.792</td>
		<td>0.864</td>
		<td>0.78</td>
	</tr>
	<tr>
		<td><b>R</b></td>
		<td>0.81</td>
		<td>0.917</td>
		<td>0.842</td>
		<td>0.828</td>
		<td>0.793</td>
		<td>0.811</td>
		<td>0.841</td>
		<td>0.869</td>
		<td>0.81</td>
		<td>0.871</td>
		<td>0.8</td>
	</tr>
	<tr>
		<td><b>F1</b></td>
		<td>0.806</td>
		<td>0.914</td>
		<td>0.84</td>
		<td>0.815</td>
		<td>0.766</td>
		<td>0.788</td>
		<td>0.835</td>
		<td>0.863</td>
		<td>0.801</td>
		<td>0.867</td>
		<td>0.79</td>
	</tr>
</table-->


### Communication
* Join us in <a href="https://join.slack.com/t/multiconer/shared_invite/zt-vi3g97cx-MpqTvS07XX22S78nRC2s0Q">Slack</a>

* Subscribe to the [task mailing list](mailto:multiconer-semeval@googlegroups.com)

* [Contact the organizers](mailto:multiconer-semeval-organizers@googlegroups.com)