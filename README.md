# Lipsync Assignment for OpenInApp

This repository contains the code and instructions to use a pretrained model for lipsyncing audio to a video.

## Prerequisites

To execute the pretrained model, you will need the following:

1. Python environment (preferably Google Colab).
2. Clone of the repository containing the [pretrained model](https://github.com/Rudrabha/Wav2Lip).

## Step-by-Step Instructions

Follow these steps to execute the pretrained model and lipsync the audio with the provided YouTube video:

1. Clone the Pretrained Model Repository:

   ```
   git clone https://github.com/Rudrabha/Wav2Lip.git
   ```
   ```
   cd Wav2Lip
   ```


2. Install Dependencies:

   Ensure that you have all the necessary dependencies installed. If you are using Google Colab, you can install the required dependencies by running the following commands:

   ```
   !pip install -r requirements.txt
   ```
   or install independently
   ```
    !pip install librosa==0.8.0
    !pip install numpy
    !pip install opencv-contrib-python
    !pip install opencv-python
    !pip install torch
    !pip install torchvision
    !pip install tqdm
    !pip install numba
  
   ```

4. Prepare Input Files:

   First, create a directory called `media` in parent directory and place the input video in the `media` directory with the filename `video_8s.mp4`. Similarly, place the audio file in the `media` directory with the filename `audio_8s.wav`.
   
   _NOTE_: file name could be anything for input audio and video.

6. Execute the Pretrained Model:

   Use the following command to execute the pretrained model and lipsync the audio with the video:

   ```
   !python inference.py --checkpoint_path /path/to/wav2lip.pth --face media/video_8s.mp4 --audio media/audio_8s.wav --nosmooth --pads 0 9 0 0
   ```

   Replace `/path/to/wav2lip.pth` with the absolute path to the pretrained model checkpoint file (`wav2lip.pth`) available in the cloned repository.

   This command will process the video and audio files, perform lipsyncing, and store the result in the `results` folder of the cloned directory.

7. Access the Result:

   Once the execution is complete, you can find the lipsynced video in the `results` folder of the cloned repository.

## Acknowledgements

We acknowledge the contribution of the original creators of the pretrained lipsync model. The pretrained model used in this assignment is available in the repository cloned from [URL_of_the_cloned_repository.git]. We thank them for their efforts in making this model available to the public.

If you find the pretrained model useful, please consider citing their original work to give credit to the creators. You can find the details of the original model in the cloned repository.

## Contact Information

For any questions or clarifications regarding the assignment or this repository, please feel free to contact the repository owner or the assigned team at OpenInApp.

Thank you for considering this assignment. We hope you find this readme helpful in understanding and completing the task. Good luck!
