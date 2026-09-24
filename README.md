# Training Your First Network in PyTorch

A small two-layer neural network trained on a toy dataset using PyTorch. The notebook trains the baseline model first, then retrains a variation with an increased learning rate. It also displays the loss curves for comparison.

## Setup

```bash
python -m venv .venv
```

Windows:

```bash
.venv\Scripts\activate
```

Install the required packages:

```bash
pip install -r requirements.txt
```

## Run
Open the Jupyter Notebook
Open the `.ipynb` file and run the cells from top to bottom.

## Example

Baseline (lr=0.01) final loss: 0.2184
Variation (lr=0.05) final loss: 0.2236

The exact loss values may vary slightly depending on the environment.

## What changed and why

The only change between the baseline and variation was the learning rate. The baseline used a learning rate of 0.01, while the variation used 0.05. I expected the larger learning rate to make the model learn faster because the optimizer takes larger steps when updating the model's weights. And this is exactly what we see in the chart for the loss. The variation reaches a low loss relatively fast (around 3 epochs), whereas the baseline takes longer to reach that point (around 10 epochs). Since the number of epochs is so low and the toy dataset is so simple (2x + 1 with noise) they both stablize at a final loss of around 0.22.

## Known Limitations

The dataset is a small, artificially generated toy dataset, so the results do not necessarily represent how a neural network would perform on a larger real world dataset. The network is also intentionally small because the purpose of the lab is to demonstrate the PyTorch training loop. With more time I would probably use an actual larger dataset to reflect the real world.
