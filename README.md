## ComfyUI-to-Python-Extension

The `ComfyUI-to-Python-Extension` lets you translates
[ComfyUI](https://github.com/comfyanonymous/ComfyUI) workflows into executable
Python code. Designed to bridge the gap between ComfyUI's visual interface and
Python's programming environment, this script facilitates the seamless
transition from design to code execution. Whether you're a data scientist, a
software developer, or an AI enthusiast, this tool streamlines the process of
implementing ComfyUI workflows in Python.


3. Navigate to the `ComfyUI-to-Python-Extension` folder and install requirements
    ```bash
    pip install -r requirements.txt
    ```

4. Launch ComfyUI, click the gear icon over `Queue Prompt`, then check `Enable Dev mode Options`. **THE SCRIPT WILL NOT WORK IF YOU DO NOT ENABLE THIS OPTION!**

![Enable Dev Mode Options](images/dev_mode_options.jpg)

5. Load up your favorite workflows, then click the newly enabled `Save (API Format)` button under Queue Prompt

6. Move the downloaded .json workflow file to your `ComfyUI/ComfyUI-to-Python-Extension` folder

8. Run the script:
   ```bash
   python src/comfyui_to_python.py
   ```
   answer the prompts for input and output file:
   ```
   Using xformers cross attention
   
   > ComfyUI worflow file (.json): workflow_api.json
   > Output to (.py): generated_code.py 
   ```

9. After running `comfyui_to_python.py`, a new .py file will be created in the current working directory. If you made no changes, look for `workflow_api.py`.

10. Now you can execute the newly created .py file to generate images without
    launching a server:
    ```
    python generated_code.py
    ```
