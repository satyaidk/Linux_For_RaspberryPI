
```
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
echo '[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(pyenv init - bash)"' >> ~/.bashrc

```
Downgrading the system's default Python version on a Raspberry Pi is strongly discouraged as it can break system dependencies and the OS itself. The recommended and safer approach is to install Python 3.10 alongside your existing Python version using a tool like  and use a virtual environment for your projects that require it. [1, 2, 3, 4]  
Step 1: Install System Dependencies for Building Python [5]  
 builds Python from source, which requires several dependencies. Open a terminal and run the following commands: [4, 6, 7]  
Step 2: Install  [4, 8]  
You can install  using the automatic installer script: [4]  
Step 3: Configure Your Shell [9]  
After installation, you need to add  to your shell's environment variables. Add the following lines to your  file (or  if you use Zsh): [10, 11]  
Apply the changes by restarting your terminal or running: [12]  
Step 4: Install Python 3.10 [13, 14]  
Now you can install Python 3.10 using . You can list available versions with : [3, 15, 16]  
Step 5: Create and Use a Virtual Environment [17]  
Instead of changing the system's default Python, create a project-specific virtual environment: 

1. Navigate to your project directory (or create a new one):  
2. Create a virtual environment using Python 3.10: 
3. Activate the virtual environment for that directory. This creates a  file that tells  to use this version automatically when you are in this directory: [10, 20, 21, 22]  

When the environment is active, your shell prompt should change, and running  (or just ) will show Python 3.10.10. This method is safe and avoids conflicts with system components that rely on the default Python version. [3, 23, 24]  

AI responses may include mistakes.
