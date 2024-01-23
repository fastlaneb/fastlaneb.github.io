---
title: "Making a Phone Call with AI"
date: 2023-01-23 
categories: [Practical AI]
tags: [text-to-speech, prompting, huggingface,bland.ai]
---

<h3><b>Our Goal:</b> Use the power of AI to make a phone call!</h3>

<h4>Scenario</h4>
My friend recently contacted me requesting support for a petition preventing the reduction of pickleball courts at the Presidio in San Francisco. I'm a pickleball player myself, so I gladly obliged. After agreeing, he informed me that the "support" involved calling into a live city council hearing and giving a 2 minute speech on why removing these courts would be pyschologically destructive. Just wow!

<h4>Plan</h4>
The window to call the council happened to overlap with a meeting for my day job. I couldn't call in myself, so I needed another plan. I remembered an oh so funny experience the creators of my favorite podcast staged. They used an AI tool to call into a pet shop and attempt to schedule a pet grooming for their pig: [EP46: Prank Calls with AI, Rabit r1, GPT Store Released, ChatGPT Teams & LUMA Genie](https://www.thisdayinai.com/episodes/ep46-prank-calls-with-ai-rabit-r1-gpt-store-released-chatgpt-teams-luma-genie) The tool: [Bland.ai](https://www.bland.ai)

<h4>Execution</h4>
1. Create an account on [Bland.AI](https://www.bland.ai): don't worry, they give you free credits to experiment with.
2. On the Welcome Dashboard click "Send Phone Call".
3. Select the options of your choosing - I entered the dial in phone number of the city council and chose "Basic American woman" as my voice. I left the "Voice Speed" and "Interruption Threshold" on their defaults.
4. The Prompt! This is where the magic comes in. Mine looked like this:\
You're a 35 year old pickleball player named Karen Frech that lives in San Francisco, California. Your favorite place to play is the pickeball courts at the Presidio. You have met a lot of your closest friends there and you even met your current boyfriend there. They are about to significantly reduce the amount of courts. You are calling in to the city council to give a 2 minute speech on why the removal of these courts will be detrimental to your social life, you mental health and your physical health. Once you are done with the speech hang up.
5. There are many other options below the prompt that you can configure at your leisure. This is how the call went:\
USER Hello. This is the San Francisco City Council. Please state your name, address, and the reason why you support the petition. Thank you for your time and cooperation. Please proceed.\
ASSISTANT Hi my name is Karen Frech, I live at 123 Main Street in San Francisco. Im calling about the proposed removal of the pickleball courts at the Presidio. As a 35 year old player who uses those courts several times a week, I cannot express how detrimental removing them would be to my physical and mental health, as well as my social life.\
ASSISTANT Thank you. Ive been playing pickleball at the Presidio for years now and its become incredibly important to my daily routine. The physical activity I get from playing a few times a week has been life changing for my health. Ive lost weight, lowered my blood pressure, and just feel so much better. But more than that, the social connections Ive made at those courts have become like family to me. Its where Ive made my closest friends and even met my boyfriend. If those courts are removed it will completely upend my social support system. I know Im not the only one who relies on them both physically and mentally. Since the pandemic started the courts have seen more players than ever seeking community and exercise safely outside. Please reconsider removing this invaluable community resource, the negative impacts would be too great. Thank you for your time.

<h4>Conclusion</h4>

The results weren't perfect...but I'm hoping it did the in the job in this use case. This technology can only get better, and it won't be long before these interactions are seamless. If nothing else, playing with this technology offers oodles of lolz!

If you want to learn more, check out some of the text-to-speech models on hugging face: [Hugging Face text-to-speech models](https://huggingface.co/models?pipeline_tag=text-to-speech&sort=downloads)









