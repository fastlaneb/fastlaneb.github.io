---
title: "Creating a LinkedIn Headshot"
date: 2023-01-15 
categories: [Practical AI]
tags: [text-to-image, stablediffusion, training, finetuning, models, prompting]
---

<h3>Our Goal: Create an AI generated LinkedIn Headshot that makes our lil heart sing.</h3>

To accomplish this goal, we want to use an AI "Text-to-Image" model. You may have heard of the OpenAI DALL-E models. We're going to be using the most popular Open Source Model, Stable Diffusion. 

To train our model we are going to be using Google's Colaboratory platform: <https://colab.research.google.com/>

Our last tool will come from ["TheLastBen"](https://github.com/TheLastBen/) and his publicly available Jupyter notebook:

<h4> Preparation </h4>
1. Create a Google account if you don't have one. Login.
2. Go here: <https://colab.research.google.com/github/TheLastBen/fast-stable-diffusion/blob/main/fast-DreamBooth.ipynb>
3. Click the "Copy to Drive" button in the horizontal bar under the drop down menus. Rename by clicking "Copy of fast-DreamBooth.ipynb" at the top. I chose "Headshot1.ipynb".

<h4> Running the Jupyter Notebook </h4>
1. We run things in the Jupyter notebook by clicking the the "play" button to the left of the task(you may have to hover over the brackets). Our first task will be to Import Google Drive. Click "play". <b>~30 seconds</b>
2. Import the dependencies by clicking the "play" button to the left of "Dependencies". Now we're running Python. If it fails you can check the GitHub Issues Page: <https://github.com/TheLastBen/fast-stable-diffusion/issues> or the support page: <https://ko-fi.com/thelastben> <b>~30 seconds</b>
3. Model Download. If you simply leave this on 1.5 you will get [Runway's Stable Diffusion 1.5](https://huggingface.co/runwayml/stable-diffusion-v1-5) from Hugging face. This will suffice for us. All we have to do is hit the play button to download. This can take a minute or two as the model is over 6 GB. ~1 minute
4. Now it's time to "Dreambooth". We'll start with "Create/Load a Session" - Enter a session name of your choosing here. This is important as we can come back to this session later. I named mine "HeadshotSession1". Click "play".
5. "Instance Images" Now we'll reference the images that will train our model with our likeness. The most effective training is done with pictures of just you. The clearer you and your likeness are the better. I chose 18 pictures of myself. You can use the "Smart Crop" feature, or you can use a service like [Birme](https://www.birme.net) to resize your photos(I resized myself). One key thing to note here is that all of your photos need to be of the same type i.e. jpg, png, etc. They also need to all start with the same word - this is how we will tell our model what to generate in the future. For me it looked like lanehead(1).jpg, lanehead(2).jpg, etc. Click "play" and you will be presented with an interface to select your photos.
6. We do not need "Captions".
7. Training: Click "play" on "Start DreamBooth" with the default options. Our hamster is now running, we're training our model! This is by far our most intensive step: <b>~25 minutes</b>
8. "Test The Trained Model" - We simply need to click play. This is where I encountered my first error: Error! "ModuleNotFoundError: No module named 'cchardet'. I clicked "Show Code" and added the following code at the top:\
```
    import importlib

    try:
        importlib.import_module("cchardet")
    except ImportError:
        !pip install cchardet
```
<b>~2 minutes</b>
9. We now have a hosted interface of [Automatic1111's Stable Diffusion Web UI](https://github.com/AUTOMATIC1111/stable-diffusion-webui). At the bottom, a link is displayed with the URL to the interface, click it. Our trained model has been loaded into it(see top left). For me, the model is "HeadshotSession1.ckpt" - this will also reside in your Google Drive and it is ~2GB. See My Drive/Fast-Dreambooth/Sessions. 
10. In the "txt2img" prompt enter the keyword you used for your photos. For me it's "lanehead". I created the image you see on the top left with "lanehead headshot with a fancy purple shirt, pompadour haircut". You may or may not get the results you want with a simple prompt like this. Experiment around until you get what you want. There are also options to further train the model and refine the parameters in the Automatic1111 interface - if you have some good tips for this please comment below!


<h4> Random Tidbits </h4>

* If you're using the free version of Google's Colab environment you <b>will</b> be disconnected at some point. This is why it's important to document our session name. When recreating a session, we must simply rerun the first two steps in the Jupyter Notebook and then enter the session name in the "Previous_Session" section of "Test The Trained Model". If you forgot the name of your session check your Google Drive: My Drive/Fast-Dreambooth/Sessions.
* If you click "Show code", you can double click in the section to the right of the code to hide it.
* The session sometimes loses track of your model. If it prompts you, you can find the reference to it in your Google Drive: My Drive/Fast-Dreambooth/Sessions/SessionName/MyModel.ckpt
* You can download your model and run [Automatic1111's Stable Diffusion Web UI](https://github.com/AUTOMATIC1111/stable-diffusion-webui) locally. 