# mathematics-in-machine-learning





# 1. Introduction
The ionosphere is the ionized part of Earth's upper atmosphere, from about 48 km 965 km altitude. Our task is to distinguish different type of radar returns to understand if at the time of return ionosphere had some meaningful structure of free electrons. We perform a comprehensive analysis of data at hand and use state-of-the-art Machine learning algorithms to perform the fully supervised classification task. This work can be divided into four sections:
<br>
- Exploratory data analysis
- Preprocessing
- Classification without any data transormation to avoid explainability issues
- Classfication using low-dimensional data transformed by PCA

## 1.1 Dataset Description
This radar data [1][2] was collected by a system in Goose Bay, Labrador. This system consists of a phased array of 16 high-frequency antennas with a total transmitted power on the order of 6.4 kilowatts.  
The targets were free electrons in the ionosphere. "Good" radar returns are those showing evidence of some type of structure in the ionosphere. "Bad" returns are those that do not; their signals pass through the ionosphere.  
<br>
Extreme UltraViolet (EUV) and x-ray solar radiation ionizes the atoms and molecules inside the Ionosphere thus creating a layer of electrons. The ionosphere is important because it reflects and modifies radio waves used for communication and navigation. Other phenomena such as energetic charged particles and cosmic rays also have an ionizing effect and can contribute to the ionosphere. 
<br>
<center>
    <img src="https://media.giphy.com/media/hyr2a0p7JRuLWu1ZKq/giphy.gif" alt="Drawing"  class="center"/>
<br>
<br>
    <img src="https://i.imgur.com/6bwvRCe.png" alt="Drawing"  class="center" style="width: 40%;height: 100%"/>
</center>
<br>

The radar operates by transmitting a multipulse pattern to the ionosphere. It produces 17 pairs of numbers every 0.2 s all year round. Received signals were processed using an autocorrelation function whose arguments are the time of a pulse and the pulse number. There were 17 pulse numbers for the Goose Bay system. Instances in this dataset are described by 2 attributes per pulse number, corresponding to the complex values returned by the function resulting from the complex electromagnetic signal.
