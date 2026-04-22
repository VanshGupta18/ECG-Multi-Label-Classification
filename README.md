# ECG Multi-Label Classification

This repository contains a framework for performing multi-label classification of Electrocardiogram (ECG) signals using Graph Neural Networks (GNNs). The project is primarily built to process the **PTB-XL** dataset, a large publicly available ECG dataset containing diverse cardiac pathologies.

## Project Structure

- `gnn-model-ptbxl.ipynb`: The main Jupyter Notebook containing the data-processing pipeline, hyperparameter tuning, model training, and evaluation code.
- `requirements.txt`: A list of all the Python dependencies required to run the code.

## Key Technologies & Libraries

This project uses the following key libraries:
- **[PyTorch Geometric (`torch_geometric`)](https://pytorch-geometric.readthedocs.io/)**: Used to construct and train the Graph Neural Network models for the ECG data.
- **[WFDB (WaveForm DataBase)](https://wfdb.io/)**: For reading and parsing the PTB-XL ECG records.
- **[NeuroKit2](https://neuropsyco.github.io/NeuroKit/)**: For advanced physiological signal processing and feature extraction.
- **[Optuna](https://optuna.org/)**: Used for hyperparameter optimization to find the best configuration for the GNN.
- **[Scikit-Learn](https://scikit-learn.org/)**: For evaluation metrics and data splitting.
- **Pandas, NumPy, Matplotlib & Seaborn**: For data manipulation, arrays processing, and visualizations.

## Getting Started

### Prerequisites

You need Python installed on your system. It is highly recommended to use a virtual environment (`venv` or `conda`).

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/VanshGupta18/ECG-Multi-Label-Classification.git
   cd ECG-Multi-Label-Classification
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
   *Note: For `torch_geometric`, make sure your PyTorch version and CUDA setup matches the requirements detailed in the [PyTorch Geometric installation guide](https://pytorch-geometric.readthedocs.io/en/latest/install/installation.html).*

3. Download the [PTB-XL dataset](https://physionet.org/content/ptb-xl/) from PhysioNet and place it in the respective data directories as referenced in the notebook.

### Usage

1. Launch Jupyter Notebook or JupyterLab:
   ```bash
   jupyter notebook
   ```
2. Open `gnn-model-ptbxl.ipynb` and run the cells sequentially to build the graph representations of the ECG signals, tune hyperparameters with Optuna, and train/evaluate the GNN multi-label classification model.

## Features

- **ECG Graph Construction**: Converts standard 12-lead ECG signals into graph data structures taking spatial-temporal correlations into account.
- **Feature Extraction**: Utilizes NeuroKit2 for extracting crucial physiological characteristics.
- **GNN Modeling**: Uses advanced message passing techniques to predict multiple concurrent cardiac conditions.
- **Automated Hyperparameter Tuning**: Seamlessly iterates over model configurations using Optuna.

## License

This project is licensed under the [MIT License](LICENSE).