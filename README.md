# video-upscaling
Video Upscaling using Real-ESRGAN

Steps to upscale a video:
1. Upload the video
2. Create a folder *output_frames* and extract the frames there
3. Extract the frames in 3 parts because Inference was failing on upscaling with approx 1800+ frames.
4. Clone the *Real-ESRGAN* repo for upscaling the video.
5. Create a folder *results* for storing the extracted frames. Create 3 different subfolder named part_1, part_2 and part_3 to store outputs in 3 different directories.
6. Convert approx 600+ frames at a single time and upscale their resolution using **RealESRGAN_x4plus** model.
7. I have upscaled each part of frames (approx 1/3 of total frames) using different parameters.

   Part1: Outscaled by 3.5 and Used Face Enhancing

   Part2: Without Face Enhancing and outscaled by 3.5
   
   Part3: Without face Enhancing and Outscaled by 4

   Wanted to try more multiple combinations for best results but GPU utilization exceeded on Colab.

8. Copied all the enhanced frames from 3 diffrent locations and pasted into a single folder to merge all the frames into a video.
9. Merged all the frames to form a video with upscaled frames keeping in mind about the sequence of the frames.
10. Also created another video with audio by copying audio from input and pasting it in the upscaled output.
11. Finally, the resolution is checked and the higher resolution image is the upscaled one.
