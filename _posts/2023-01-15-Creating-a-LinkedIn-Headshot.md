---
title: "Creating a LinkedIn Headshot"
date: 2023-01-15 
categories: [Practical AI]
tags: [text-to-image, stablediffusion, training, finetuning, model]
---

Our Goal: Create an AI generated LinkedIn Headshot that makes our lil heart sing.

To accomplish our goal, we want to use an AI "Text-to-Image" model. You may have heard of the OpenAI DALL-E models. We're going to be using the most popular Open Source Model, Stable Diffusion. 

To train our model we are going to be using Google's Colaboratory platform: https://colab.research.google.com/

Our last tool will come from "TheLastBen" and his publicly available Jupyter notebook:

1. Create a Google account if you don't have one. Login.
2. Go here: https://colab.research.google.com/github/TheLastBen/fast-stable-diffusion/blob/main/fast-DreamBooth.ipynb
3. Click the "Copy to Drive" button towards the top. Rename if you choose, I chose "Headshot1.ipynb".
4. Now we will go through the steps in the Jupyter notebook:
5. Import Google Drive. We will need to do this so that we can access the photos we want to train the model on.
6. Import the dependencies. Now we're running Python. *VERSIONS CHANGE* On 1-11-24 the dependencies successfully imported for me. If they don't you may have to put your debugger hat on. You can also check "TheLastBen"'s GitHub Issues Page: https://github.com/TheLastBen/fast-stable-diffusion/issues or go to his support page: https://ko-fi.com/thelastben
7. Model Download. If you simply leave this on 1.5 you will get Runway's Stable Diffusion 1.5 from Hugging face. This will suffice for us. All we have to do is hit the play button to download. This can take a while as the model is over 6 GB.
8. "Create/Load a Session" - Enter a session name of your choosing here. This is important as we can come back to this session to save time. I named mine "HeadshotSession1".
9. Now it's time to reference the images that will train our model with our likeness. The most effective training is done with pictures of just you. I chose 18 pictures of myself. You can use the "Smart Crop" feature, or you can use a service like Birme https://www.birme.net to resize your photos. One key thing to note here is that all of your photos need to be of the same type i.e. jpg. They also need to all start with the same word - this is how we will tell our model what to generate in the future. For me it looked like lanehead(1..jpg, lanehead(2..jpg, etc.
10. We do not need captions.
11. Start DreamBooth with the default options. We may return to this later if we do not get the output we want. Our hamster is now running, we're training our model! 
12. "Test The Trained Model" - "Previous_Session" is where we can enter our session name if we get disconnected - which will happen if you're on the free version. If you're on the first run you don't need to enter anything here. Error! "ModuleNotFoundError: No module named 'cchardet'. I clicked "Show Code" and added the following line at the top "!pip install cchardet". Success!
13. We now have a third party interface that has our trained model loaded. For me it's "HeadshotSession1.ckpt". A link is displayed with the public URL, click it.
14. We are now on a hosted instance of Automatic1111's Stable Diffusion Web UI. More info: https://github.com/AUTOMATIC1111/stable-diffusion-webui
15. In the "txt2img" prompt enter the keyword you used for your photos. For me it's "lanehead". You can then manipulate the prompt to your heart's desire!
16. Not if, but when you get disconnected, you can restart by running Step 1 and Step 2 again.
