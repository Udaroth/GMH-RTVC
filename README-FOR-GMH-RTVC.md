# GE2E Mellotron Hifi-GAN - Real Time Voice Cloning (GMH-RTVC)
## Setting up the python virtual environment for GMH-RTVC
It is best to use the program in a virtual environment in order to keep the dependency of the projects isolated from other versions installed on your device. Perform the following steps to

1. Open a command prompt in the root of the repository
2. Run `python3 -m venv gmhrtvc`, which creates a virtual env with the name gmhrtvc
3. Run ` gmhrtvc\Scripts\activate.bat` on Windows or `source gmhrtvc/bin/activate` on macOS
4. From here onwards, refer to the Quick Start section of the README.md

## Running the toolbox
1. Make sure that the virtual environment is activated
2. Run `python demo_toolbox.py -d <datasets_root>`
> Note: `<datasets_root>` is the folder where your dataset is stored, it is also an optional parameter, you can select input manually in the toolbox.

## Performing voice cloning using the Mellotron Synthesizer
The performance of the Mellotron synthesizer has yet to be optimized and is one of the key suggested future works, but this how to perform inference using the existing Mellotron implementation. After the demo toolbox is started using the steps described in "Running the Toolbox", a text box can be seen on the right with a series of parameters. The only one that is of concern is the `audio`. Replace the path here with the path to your desired audio input. A suggested improvement here would be to use the same input as the file browser implemented on the left side of the toolbox. After the path has been replaced, click on `Synthesize and vocode with Mellotron`.

## Performing voice cloning using the original synthesizer (Tacotron2)
1. Click `Browse` and select the desired input audio file.
2.  Select the desired model in the `Synthesizer` dropdown
3.  Select `g_hifigan` in the `Vocoder` dropdown
4.  Select the desired audio output in the `Audio Output` dropdown
4.  Click `Synthesize and vocode`

## Including pretrained models into the toolbox
In order to use a pretrained model, you would need to place it in the followiing path

`GMH-RTVC/synthesizer/saved_models/<your_pretrained_model.pt>`

Similarly, if you are trying to use the model in the MockingBird directly

`MockingBird/synthesizer/saved_models/<your_pretrained_model.pt>`

