# Image-and-Video-Enhancement-With-Deep-Learning

This project contains two Jupyter notebooks that bring state-of-the-art AI restoration into action:

- **Image Enhancement** → powered by [CodeFormer](https://github.com/sczhou/CodeFormer), wrapped here as `Baseta_Tube_AI_Image_Enhance`.  
- **Video Enhancement** → powered by [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN), wrapped here as `BasetaTube_AI_VideoFace_Enhance`.

The notebooks are written to run smoothly in **Google Colab**, with all installations, pretrained weights, and helper functions included.

---

## 🚀 What these notebooks do

- **Image Notebook**:  
  - Cleans, sharpens, and restores details in uploaded images.  
  - Uses CodeFormer with pre-trained models to enhance facial details.  
  - Provides side-by-side before/after comparisons.

- **Video Notebook**:  
  - Enhances video quality by processing frames with Real-ESRGAN.  
  - Restores sharper details and upscales video resolution.  
  - Outputs a processed MP4 with automatic timestamp in the filename.  
  - Includes inline video preview right inside Colab.

---

## 🛠 Setup (common to both)

1. Open the notebook in **Google Colab**.  
2. Run the **Installations** cell — this will:
   - Clone the enhancement repo (CodeFormer or ESRGAN).  
   - Install Python dependencies (`basicsr`, `ffmpeg-python`, etc.).  
   - Download pretrained models automatically.  

That’s it — no manual setup required.

---

## 📷 How the Image Notebook works (step by step)

1. **Clone and setup**:  
   Clones CodeFormer into `Baseta_Tube_AI_Image_Enhance` and installs dependencies.  

2. **Download pretrained models**:  
   Downloads CodeFormer + facelib weights using provided scripts.  

3. **Helper functions**:  
   - `display(img1, img2)` → shows side-by-side before/after results.  
   - `imread(path)` → reads and converts uploaded images into RGB.  

4. **Upload your image**:  
   Uses Google Colab’s `files.upload()` to let you drag and drop an image into the notebook.  

5. **Enhancement process**:  
   Runs the CodeFormer model on the uploaded image.  

6. **Visualize results**:  
   The notebook automatically displays a large side-by-side comparison:  
   - Left = *Before*  
   - Right = *After*  

---

## 🎥 How the Video Notebook works (step by step)

1. **Clone and setup**:  
   Clones Real-ESRGAN into `BasetaTube_AI_VideoFace_Enhance` and installs dependencies.  

2. **Upload your video**:  
   Drag & drop an MP4 into Colab, which gets stored in `/content/`.  

3. **Process the video**:  
   - Frames are passed through the Real-ESRGAN model.  
   - Enhanced frames are stitched back into an MP4.  
   - File is renamed automatically with a timestamp, thanks to `rename_file_with_timestamp()`.  

4. **Preview results inline**:  
   The function `show_video(video_path)` displays the enhanced video directly inside Colab without downloading.  

---

## ✨ Outputs

- **Image Notebook**:  
  - Enhanced image(s) saved in the output folder.  
  - Side-by-side comparisons rendered inline.  

- **Video Notebook**:  
  - Enhanced MP4 video with `_BasetaTube_TIMESTAMP.mp4` filename.  
  - Inline video preview cell in the notebook.  

---

## 💡 Notes & Tips

- For best performance, run on **GPU runtime in Colab**.  
- Upload high-resolution inputs for best output quality.  
- If the notebook crashes with large videos, try processing shorter clips.  
- CodeFormer is particularly good for **faces**, while Real-ESRGAN is more general-purpose for **video frames**.

---

## 👤 Author
Marwan Gamal

Credits:  
- [CodeFormer](https://github.com/sczhou/CodeFormer)  
- [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN)  
