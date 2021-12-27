# Software Installation (Mac on Apple Metal M1)

With the introduction of the M1 chip, Apple introduced a system on a chip. The new Mac M1 contains CPU, GPU, and deep learning hardware support, all on a single chip. The Mac M1 can run software created for the older Intel Mac's using an emulation layer called Rosetta). To leverage the new M1 chip from Python, you must use a special Python distribution called Miniforge. Miniforge replaces other Python distributions that you might have installed, such as Anaconda or Miniconda. Apple instructions suggest that you remove Anaconda or Miniconda before installing Miniforge. Because the Mac M1 is a very different architecture than Intel, the Miniforge distribution will maximize your performance. Be aware that once you install Miniforge, it will become your default Python interpreter.

# Installing Python and TensorFlow
Is your Mac Intel or Apple Metal (ARM)? The newer Mac ARM M1-based machines have considerably better deep learning support than their older Intel-based counterparts. Mac has not supported NVIDIA GPUs since 2016; however, the new M1 chips offer similar capabilities that will allow you to run most of the ML applications.

# Procedure
# Install Brew Mac
This installation is based and tested for **macOS Monterey**:
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
 
