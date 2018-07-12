# wek-mid-ware

For this session, we are going to step outside of the world of Python and Tensorflow to experiment with machine learning in a perhaps more immediately accessible way. We will explore how machine learning can be used as a "middle ware" for a variety of creative and/or technical (as in "technique") purposes. This will all be done through a wonderful software called Wekinator, which was developed by Rebecca Fiebrink of Goldsmiths, University of London. Most of the material we will experiment with is adapted from her [online Kadenze course](https://www.kadenze.com/courses/machine-learning-for-musicians-and-artists-v/info), which is naturally recommended. 

Wekinator particularly adept at training for gesture recognition, or "gesture following". To exemplify this, we will use it with a sensor called Leap Motion which tracks the position of the joints in our fingers, hands and lower arm. Together, we can train Wekinator to recognize hand signals or movements, such as sign language or hand gestures. However, once we have trained Wekinator to recognize (or "classify") our hand signals or gestures, we will want to do something with this data. This is where another software comes in (hence the term "middleware"). [Max MSP](https://cycling74.com/) is a audiovisual programming environment, and we will use Wekinator and Leap Motion to control the **parameters** of a digital instrument designed in Max MSP. Oh, one more thing, we will need another software to get the Leap Motion data from the sensor into Wekinator. We'll use either [Processing](https://processing.org/) or [Openframeworks](https://openframeworks.cc/) for that. 

So, now we are up to 4 softwares, and if it seems a lot then you seem right. However, we will only focus on working with Wekinator - the other software programs are already programmed and we simply have to run them. Once we are up and running the process of training and running Wekinator is suprisingly intuitive, and the results can be highly interesting, creative and fun.

*Note: if you don't have access to a Leap Motion, you may do all activities in this session with a touchscreen phone or notebook - see all programs ending in "mira" and instructions at the bottom of this README.

### Our Project - a Digital Musical Instrument Controlled by Machine Learning

There are at least 2 ways I hope you will see this project - either as an artistic problem and/or as an engineering design problem. Both are essentially the same. In the artistic context we are concerned with **[expressivity](https://cordis.europa.eu/project/rcn/198700_en.html)**, and in the engineering design context we are concerned with **[inclusive design](http://universaldesign.ie/What-is-Universal-Design/Conference-Proceedings/Universal-Design-for-the-21st-Century-Irish-International-Perspectives/Designing-a-more-Inclusive-World/)** (similar to universal design). What's the purpose of these together? Anything, though I will suggest a minimum of an instrument with wide dynamic range that can be accurately controlled by *anyone*. For example, you might think to design the instrument for persons who cannot play a traditional instrument due to physical limitations.

### Getting Started

To begin, download each of the sofware's we will be working with. We'll exclude Openframeworks in favor of Processing for now, but if you are on Mac the Openframeworks gives you up to 31 data points for each hand, while Processing is only built for 15 from one hand. [Wekinator](http://www.wekinator.org/downloads/), Max MSP](https://cycling74.com/), [Processing](https://processing.org/). Open them simply to be sure installation was succesful.

### The Instrument (Max MSP)

We'll start off by exploring the "blotar" wekinator example in Max MSP. Blotar is a classic work of digital synthesis by Perry Cook, and it is a combination of the spectra of a guitar and a flute, hence the name. Open the appropriately titled Max MSP "patch" (name for a program) in this repo, click the speaker object and play with the parameters a bit. Despite the silly name, it is a digital instrument capable of an impressive range of sounds. We'll want to capture these possibilities in our Wekinator machine learning program.

### Wekinator Basics

Let's start with a crudely trained model demonstrating what we want to improve. Do the following:

1. Open the following 2 Max MSP programs: ```BlotarSynth..maxpat``` and ```SimpleMax_3Inputs_Mira```. 
2. Start the audio in the '''BlotarSynth 
3. Then open the ```WekinatorProject.wekproj``` file inside the folder ```WekBlotarMira```
4. Click the ```Start Listening``` button in Wekinator. Move the sliders in ```SimpleMax)3Inputs_Mira``` and you should see the values moving in Wekinator.
5. Click the ```Run``` button in Wekinator.
6. Open your touchscreen device on the same wifi network as the computer running our programs.
7. Go to the http address shown in ```SimpleMax)3Inputs_Mira``` and click ```Connect```.
8. You should see the sliders in your touchscreen device. Move them and see what happens. Should be some drastic sounds.

So what we have done is load a **pre-trained model** that is capable of controlling our instrument. Have some fun with it, and let's train some new models to understand how that works.




