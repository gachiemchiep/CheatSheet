Conda CheatSheet
====================

.. code-block:: sh

  # Save packages for future use:
  $ conda list --export > package-list.txt

  #Install Requirement.txt
  $ conda install --yes --file requirements.txt
  $ while read requirement; do conda install --yes $requirement; done < requirements.txt

  # Remove environtment
  conda remove --name myenv --all

  # Create environment file
  conda env export > environment.yml

  # Create environment from file
  conda env create -f environment.yml
  
  # Clone environment
  conda create --name myclone --clone myenv

