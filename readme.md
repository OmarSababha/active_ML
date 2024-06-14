# Lumos5G: Active vs Passive Experiment

## Overview

This code is used in a manuscript submission under the title: **"Active ML for 6G: Towards Efficient Data Generation, Acquisition, and Annotation"**. The pre-print of the manuscript is available on arXiv: 2406.03630v1 [https://arxiv.org/abs/2406.03630v1].

As part of a manuscript submission, this repository contains the code and data for an active machine learning case study performed on the Lumos5G dataset. We compare the performance of uncertainty sampling (active ML) to the passive ML approach. The main script `lumos5g_active_many_to_many.ipynb` can be used to run an experiment, and `plot.ipynb` generates comparative plots of the results after running multiple experiments.

## Files

- `lumos5g_active_many_to_many.ipynb`: Main script for running an experiment.
- `plot.ipynb`: Script for plotting the results.
- `Lumos5G-v1.0.csv`: Dataset used for the experiments.

## Requirements

- TensorFlow 2.16.1
- Keras 3.2.0

## Usage

### Running the Experiments

1. **Setup**: Open `lumos5g_active_many_to_many.ipynb` and configure the parameters at the top of the notebook:
   - `base_dir`: Set this to your own directory where the results will be saved.
   - `experiment_type`: Choose either `"active"` or `"passive"` depending on the type of experiment.
   - `output_folder`: Specify the name of the folder where results will be saved. For example, if your experiment_type is "active", then you can name set the output_folder to "run1_active".

2. **Execution**: Run the notebook (`lumos5g_active_many_to_many.ipynb`). Repeat this process multiple times to produce several folders with different configurations (e.g., `run1_active`, `run2_active`, `run1_passive`, `run2_passive`). This process takes time. Therefore, we have also saved some folders that were used to produce the figure in the manuscript.


### Plotting the Results

1. **Setup**: Open `plot.ipynb`.

2. **Execution**: Run the notebook to generate comparative plots of the performance of the active and passive runs. Note, you need to select the folders that are part of the "active" strategy and the folders that are part of the "passive" strategy.

## Example

1. Run `lumos5g_active_many_to_many.ipynb` with the following configurations:
   - `base_dir = "/your/base/directory"`
   - `experiment_type = "active"`
   - `output_folder = "run1_active"`
   
2. Change `experiment_type` to `"passive"` and `output_folder` to `"run1_passive"` and rerun the notebook.

3. Repeat the above steps to create additional runs (e.g., `run2_active`, `run2_passive`).

4. Open and run `plot.ipynb` to compare the results of active and passive experiments.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or issues, please contact Omar Alhussein. You can find my email in the paper.
