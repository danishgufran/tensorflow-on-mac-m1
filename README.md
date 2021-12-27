# Software Installation (Mac on Apple Metal M1)

With the introduction of the M1 chip, Apple introduced a system on a chip. The new Mac M1 contains CPU, GPU, and deep learning hardware support, all on a single chip. The Mac M1 can run software created for the older Intel Mac's using an emulation layer called Rosetta). To leverage the new M1 chip from Python, you must use a special Python distribution called Miniforge. Miniforge replaces other Python distributions that you might have installed, such as Anaconda or Miniconda. Apple instructions suggest that you remove Anaconda or Miniconda before installing Miniforge. Because the Mac M1 is a very different architecture than Intel, the Miniforge distribution will maximize your performance. Be aware that once you install Miniforge, it will become your default Python interpreter.

# Installing Python and TensorFlow
Is your Mac Intel or Apple Metal (ARM)? The newer Mac ARM M1-based machines have considerably better deep learning support than their older Intel-based counterparts. Mac has not supported NVIDIA GPUs since 2016; however, the new M1 chips offer similar capabilities that will allow you to run most of the ML applications.

# Procedure
# Install Brew Mac
This installation is based and tested for **macOS Monterey**:
```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
 # Install Miniforge
 
 **Once you have installed Homebrew, I suggest closing the terminal window and opening a new one to complete the installation.**
Next, you should install the xcode-select command-line utilities. Use the following command to install:
```shell
xcode-select --install
```
If the above command gives an error, you should install XCode from the App Store.

You will now use Homebrew to install Miniforge with the following command:

```shell
brew install miniforge
```
# Initiate Conda
```shell
conda
```

This will set the python PATH to the Miniforge base in your profile (~/.bash_profile if bash or ~/.zshenv if zsh) and create the base virtual environment.

Also, check for your python path

```shell
which python
```
# Install Jupyter and Create Environment

Next, lets install Jupyter.
```shell
conda install -y jupyter
```
First, we deactivate the base environment.
```shell
conda deactivate
```

Next, we will install the Mac M1 tensorflow-apple-metal.yml file that I provide. Run the following command from the same directory that contains tensorflow-apple-metal.yml.

```shell
conda env create -f tensorflow-apple-metal.yml -n tensorflow
```
# Activating New Environment
To enter this environment, you must use the following command:
```shell
conda activate tensorflow
```

For now, let's add Jupyter support to your new environment.
```shell
conda install nb_conda
```

# Register your Environment
```shell
python -m ipykernel install --user --name tensorflow --display-name "Python 3.9 (tensorflow)"
```
# Testing your Environment

You can now start Jupyter notebook. Use the following command.

```shell
jupyter notebook
```
Then finally, lets test tensorflow by running the test_tensorflow.ipynb.


