---
layout: post
title: Environmental Noise Recording Round 01
description: First set of noise recording conducted on Jan 30
---
### Premise
In accounting for acoustical properties of building materials, a single number Noise Reduction Coefficient (NRC) or Sound Transmission Class (STC) value is used. Both values describe how well a material absorbs sound energy, while NRC focuses on reflected sound, STC focuses on transmitted sound, usually in the range of normal speech frequencies between 120 Hz to 4000 Hz.

While NRC and STC are industry standards in understanding acoustical properties of building materials, in an age where offices have mostly adopted an open office layout where sound transmits freely, and with diversifying office culture where activities like desktop prototyping with CNC machines, doggy day care, and aerobic exercises can happen in the same space, these metrics are no longer adequate in assessing how our aural environments.  

According to the National Institute on Deafness and Other Communication Disorders, long term exposure to sounds at or above 85 decibels can cause hearing loss.  This metric to correlate sound pressure levels to hearing loss is, however, much too simplistic because it does not describe how different frequencies of sound affects our health differently. In a paper published in Environmental Health in 2014, researchers found high exposure to low frequency traffic noise at around 125 Hz may induce hypertension.  Other researchers have also found significant associations between low frequency exposure to chronic diseases such as headaches, unusual tiredness, lack of concentration, irritation, and pressure on the eardrum.  

In short, our evolving work environment and the increasing number of environmental health research are showing a deficiency in this single value system, and our proposal is to develop a more comprehensive view of noise and its interaction with space and materials. 

What we propose is to go beyond the single value metric. Sound is a spectrum and human hearing is sensitive from 20Hz to 20kHz, therefore, we propose an acoustical standard that would allow us to gain a deeper insight into the nature of sound. 

This proposal involve 2 stages of acoustical testing. The first is to record and graph environmental noise in and around our work environments. We want to record and profile noises of common equipments and how it differs from “background” noise.  For the second phase, we will build an acoustical testing station to test and profile common and unusual acoustical materials. 

### Environmental Noise Recording Methodology

For sound recording, we are using a Zoom H1 Digital Recorder with 2 unidirectional microphone set at 90 degree to one another recording a wide sound field, and an Extech 407730- Digital sound level meter to record the sound pressure level (SPL) of the source, typically 1 meter away or as noted. If situation does not allow for the recording to be at 1 meter away, 2 meter distance is used and we use the Inverse Square Law, reduction of 6 decibel per meter, to adjust for the final value. 



## dL  =  20 log (R2 / R1)  
where:
dL = difference in sound pressure level (dB)
R1 = distance from source to location 1 (ft, m)
R2 = distance from source to location 2 (ft, m)



The sound pressure level is recorded with A-weighting on the instrument, which is weighted to human sound perception. The initial recordings recorded at about 36 locations profiling various kinds of noise, from single point source produced by a single machine, an omnisource produced by the extraction fan that is omnipresent, to background noise produced by foot and vehicular traffic. 

We also referenced Health Link British Columbia  for typical noise types and their average decibels levels, and we established that around 50 dB is what a quiet work environment would be, high 70s dB can be irritating to people, and above 85 dB would be considered harmful if there is long term exposure. 

Based on this information, we collated our recordings and profiled spaces that can serve as our baseline for what a quiet work environment would be, and spaces with frequent noise level above 75 dB. 



***


|LOCATION     |SOUND SOURCE     |DISTANCE FROM SOURCE     |SOUND LEVEL     |
| --- | --- | --- | --- |
|ITL Office		|3D Printer     |1 m     |50.5     |
|ITL Office     |Chop Saw     |2 m     |101.1     |
|Higgins Hall Lobby     |Foot Traffic     |ambient     |81.8     |
|Higgins Hall Main Staircase 1st Floor     |Vending Machine     |1 m     |77.6     |
|Higgins Hall CNC Shop     |CNC     |2 m     |107.8     |
|Higgins Hall South 3rd Floor Hallway		|CNC + Foot Traffic     |1 m  |79.3  |   
|Higgins Hall 3D Print Shop		|Spray Booth Fan     |1 m     |81     |
|Main Campus Security Booth		|Ambient Traffic     |ambient     |75.1     |
|Pratt Career Center		|Foot Traffic     |ambient    |53     |
|Cafeteria		|Foot Traffic     |ambient     |79.3     |
|Engineering Wood Shop		|Machinery     |1 m     |79.5     |
|Engineering Print Lab		|Printers     |1 m     |77     |
|Engineering 1st Floor Hallway		|Video     |2 m     |77.6     |


***


### Data Processing Protocol
In addition to recording the sound pressure levels,  the sound is also recorded as a sound file in .WAV 24bit / 96kHz format. The .WAV file is then brought into Audacity where we use its Fast Fourier Transform (FFT) algorithm to plot the spectrum. However, since Audacity’s spectral-graph is not weighted to human hearing, the data is exported out as a text file and then brought into Python to apply A-weighting with the following equation.

A-Weighting Equation

![alt text](../../assets/images/a-weighting-eq.gif)
where:
WA = weighting to be applied, dB
f = frequency, Hz
$$$$sin(x)


<h3 id="content">Results for Materials Set01</h3>

<iframe width="1200" height="800" frameborder="0" scrolling="no" src="//plot.ly/~prattitl/152.embed"></iframe>

<h3 id="content">Results for Materials Set02</h3>

<iframe width="1200" height="800" frameborder="0" scrolling="no" src="//plot.ly/~prattitl/154.embed"></iframe>