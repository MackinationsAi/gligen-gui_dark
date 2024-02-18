# DARK_GLIGEN GUI

[GLIGEN](https://gligen.github.io/) is a novel way to specify the precise location of objects in text-to-image models. I present here an intuitive DARK GUI that makes it significantly easier to use GLIGEN with ComfyUI.

![GLIGEN GUI screenshot](gligen_gui/docs/ui_update.png)

![GLIGEN Example Image](gligen_gui/docs/example_w-Boxes.png)

![GLIGEN Example Image](gligen_gui/docs/example.png)

## Getting Started

First of all make sure you have [ComfyUI](https://github.com/comfyanonymous/ComfyUI) successfully installed and running.

Next, download the [gligen_sd14_textbox_pruned.safetensors](https://huggingface.co/comfyanonymous/GLIGEN_pruned_safetensors/blob/main/gligen_sd14_textbox_pruned.safetensors) GLIGEN model file and place it in the ComfyUI/models/gligen directory.

## Install

Clone this repository.

    git clone https://github.com/MackinationsAi/gligen-gui_dark.git
    cd gligen-gui_dark/gligen_gui
    
Now you are going to want to create a Virtual Environment.

    python -m venv venv
    venv\Scripts\activate
    pip install flask

You are now ready to start the GUI, double click on the gligenBoot_.bat (this will only work if you have ComfyUi already running in the background).

Note that this assumes your ComfyUI instance is using port 8188. If not, replace 8188 with the correct port number.

Finally, open http://127.0.0.1:5001 in your browser to start using the GUI. However change 8188 in the URL to the port used by ComfyUI if it is different.

## How To Use

Make sure you have a Stable Diffusion 1.5 **checkpoint** selected. Usage is pretty simple and straightforward! Envision your image by drawing grounding boxes on the blank canvas with your mouse, and labeling them by entering your desired prompt in the corresponding text input in the table on the right.

You can further describe your image in the text input labelled **POSITIVE** but in my experience it works better if you only enter tags relating to the style and quality of your desired image.

If there are any LORAs you wish to use, press the **+** button in the LORA section. Then, select the name of the LORA and adjust its strength, You can add mulitple LORAs.

Finally, press the Queue Prompt to submit the prompt to ComfyUI. Once the image is generated, it will appear on the canvas.

## Cred

This is my DARK forked version of mut-ex's great work. The original repo can be found [here](https://github.com/mut-ex/gligen-gui).

(My primary coding language is Python so these edits are quick & dirty, if you all like the changes enough perhaps mut-ex & I can partner up on future versions!)
