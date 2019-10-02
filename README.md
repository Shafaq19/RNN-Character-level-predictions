# RNN-Character-Prediction  🤖🚧 ➕⏰
IIn this repository, we construct a character-level LSTM with PyTorch. The network will train character by character on some text, then generate new text character by character. 
## Installation 
If you are using pip then you can install the required libraries by:

 `pip install -r requirements.txt`

Conda users can make use of the env.yml file to activate

  `conda env create -f env.yml`

   `conda activate env.yml`

   
## Usage 
- load the network

  `with open('rnn_x_epoch.net', 'rb') as f:
      checkpoint = torch.load(f)
      loaded = CharRNN(checkpoint['tokens'], n_hidden=checkpoint['n_hidden'], n_layers=checkpoint['n_layers'])
      loaded.load_state_dict(checkpoint['state_dict'])  `
- predict  your text with
   `predict(net, ch, h, top_k=top_k)`
   
