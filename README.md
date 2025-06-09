# Hawthorne Media Analyzer


### Setup: Environment

The Media Analyzer program leverages a portable environment to ensure package compatibility. Follow these steps to create a designated environment for this program:
<br>
On Anaconda:<br>
	&emsp;1) Open Anaconda Prompt (It can be opened from the Windows start menu. Do not confuse with Command Prompt)<br>
	&emsp;2) Change directories to the folder containing the python notebook.<br>
	&emsp;3) Create a designated environment called "Media_Analyzer_Env" and install the required packages with the following script:<br>
		&emsp;&emsp;&emsp;conda create -n Media_Analyzer_Env python=3.10<br>
		&emsp;&emsp;&emsp;conda activate Media_Analyzer_Env<br>
		&emsp;&emsp;&emsp;pip install -r requirements.txt<br>
		&emsp;&emsp;&emsp;python -m ipykernel install --user --name=Media_Analyzer_Env --display-name "Python (Media_Analyzer)"<br>
		&emsp;&emsp;&emsp;conda deactivate<br>
	&emsp;4) In JupyterLab or JupyterNotebook, set the kernel for the to "Python (Media_Analyzer)" before running the code in the notebook.<br>
	&emsp;5) Two of the packages cannot be installed through pip. You must install these directly as follows:<br>
		&emsp;&emsp;a. ffmpeg: Download ffmpeg from https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-full.7z<br>
			&emsp;&emsp;Extract the file. Type the location of the .exe file into the ffmpegPath.txt file in the project folder.<br>
		&emsp;&emsp;b. libsndfile: A block of code for this install was provided at the beginning of the notebook. Uncomment and run the installation.<br>

<br><br>
### Setup: API Key
This program uses an openai API. You will need a key to access the API. This key is linked to the organization's account and API calls will be charged against the account. To protect the key, we recommend storing it as an environmental variable using the steps below. This step only needs to be done once for the computer or environment in which you are working; you never need repeat this step unless you set up a new account with the LLM. Note that the name of the key is case sensitive and must match exactly.<br>


##### If you use Anaconda:<br>
  &emsp;Launch Anaconda Prompt (this is different than the Windows command prompt)<br>
  &emsp;run: conda active base<br>
  &emsp;then run: setx AI_API_Key "your_API_Key"<br>
<br>
##### For Windows (without Anaconda):<br>
  &emsp;From the Windows start menu, select "Settings"<br>
  &emsp;Go to "System" > "Advanced System Settings"<br>
  &emsp;From the "Advanced" tab, select the "Environmental Variables" button<br>
  &emsp;Select "New"<br>
  &emsp;Name the variable "AI_API_Key"<br>
  &emsp;Enter the key as the variable value; click "OK"<br>
		
