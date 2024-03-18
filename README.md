# 2024 Resources

Code and tools used/shared/created in the 2024 edition of AI4SG Dagstuhl, divided by challenge.

## Time Series Forecasting
#### Context
Can we have a generalizable approach to forecasting time series, e.g. demand of medical equipment?

#### Code and tools
See [Lennart Purucker's GitHub Gist](https://gist.github.com/LennartPurucker/a015edf88733a22996e492e387b8831f) based on [AutoGluon](https://auto.gluon.ai/stable/index.html) and tabular baselines.


## Improving Crisis Communication
#### Context
Especially in the hours and days during and after major natural disasters (or crises with comparable humanitarian consequences), humanitarian organizations receive numerous calls and messages from the civilian population: people offer their help and resources and ask for help for themselves or their relatives. They praise or criticize the work of the humanitarian organization and discuss it with other people in posts. Although not particularly likely, it is also conceivable that deliberately manipulative actors, possibly also with the help of so-called bots, are trying to slow down the work of the humanitarian organization through various messages.
In some cases, the number of requests sent to us via social media exceeds our response capacities. The staff trained for crisis communication can only to a certain extent and for limited periods of time be supported by colleagues from other teams and departments. Support staff must also first be briefed by the crisis communication team, which takes additional time.
Another challenge in the communication process is the triage of messages. Although the underlying software offers filter options, it is necessary to manually scan the messages and decide which ones are more urgent to answer than others.

#### Code and tools
* A pretrained [`paraphrase-multilingual-mpnet-base-v2`](https://huggingface.co/sentence-transformers/paraphrase-multilingual-mpnet-base-v2) sentence transformer was used to obtain message embeddings.
* Small, open-source versions of [Google's Gemini](https://blog.google/technology/ai/google-gemini-ai/) (a.k.a. [Gemma](https://blog.google/technology/developers/gemma-open-models)) might be valuable
* Found a model on Huggingface that was trained on data related to social media posts on disasters: [`CT-M2-Complete`](https://huggingface.co/crisistransformers/CT-M2-Complete)

## Fairness-aware Face Recognition
#### Context
Humanitarian organizations need to register people into their programs. In some contexts, people do not hold any proof of their legal identity (e.g. passport, national ID).
Yet, in each program it is imperative to verify that people are not registered twice (i.e. they’re duplicate), whether caused by error or fraud.
The only possible identifiers are therefore biometrical: fingerprint, iris/retina, voice, or face.  Face pictures are the least complex and most inexpensive form of biometric,
as they can be collect with feature phones and smartphones using openly available mobile data collection technology (e.g. [Kobo](https://www.kobotoolbox.org/)).
The problem: how do we ensure that the model accuracy is _fair_, i.e. consistent across e.g. gender and ethnicity?

#### Code and tools
* A simple API-based tool to check for duplicates: [dedupliface](https://github.com/rodekruis/dedupliface)
* A [theoretical workflow](https://docs.google.com/presentation/d/1Jk-YyoFrbRWyBN20zf_ykCJwZjD6lkULALW_XwK2_zU/edit#slide=id.p) to monitor fairness in production

 ## Legal advice to vulnerable people
 #### Context
The aim is to profile elderly people in order to give them legal personalized information on loss of autonomy. In order to profile them, we collect data (personal situation, family situation, estate, health situation). Language is French.

#### Code and tools
* We decided to focus on the more complicated part: health situation and more precisely, is the person has cognitive impairment (or assimilated as severe anxiety/tiredness). See [the notebook](https://drive.google.com/file/d/1fCl14qeEqoOxtzuhj__Z4Z0T3xiCYlW8/view?usp=sharing).
* [`FlauBERT`](https://huggingface.co/docs/transformers/model_doc/flaubert) was the most performing model (0,80 accuracy).

## Tracking Narrative Changes
#### Context
To more effectively measure the results of _narrative work_, i.e. communication campaigns, through tracking and analysing shifts in narratives around specific issues and subjects, harnessing the power of artificial intelligence. By achieving this aim, this pilot shall contribute to enhancing the effectiveness of our narrative change strategies/interventions, thanks to the provision of information and data that support adaptive management and evidence-based decision-making.  Ultimately, we want our narrative work to align with the needs and lived realities of the people we work with and the targeted audiences.

#### Code and tools
See [dedicated repo](https://github.com/ginic/oxfam-text-analysis)



  
