# amurobohack-SmartCity
## Intro

  Traffic management in cities is a big issue. The traffic lights int the city are hardcoaded to a fixed time interval and the keep on working in the same manner even if there is less traffic on one side and more traffic on another side.
  Smart Traffic Light system uses real time images of the traffic at the signal and moniters the time diration for which each signal should remain "ON"(Green) or "OFF"(RED).
 
## Dependencies

 1.Download the darkflow repository and complete the setup process
 2.Install the dependencies ```jupyter```, ```matplotlib```, ```tensorflow 1.14``` and ```openCV``` using ```pip``` 
 
## <a name="darkflow">How to install darkflow</a>

1. Go to [darkflow repository](https://github.com/thtrieu/darkflow) and clone it.
2. Install darkflow using by typing ```pip install . ```.


## How to run the notebook
After successfully downloading and installing the dependencies

1. Clone this repository.
2. Copy the SmartTrafficLight.ipynb file , label.txt file and sampleVideo.mp4 file and paste it in the darkflow-master folder
3. Copy the yolov2-tiny.cfg file and paste it in the cfg folder.
4. Copy the yolov2-tiny.weights file and paste it into the bin folder.
5. Change directory to darkflow master and open jupyter notebook.(use cd "enter path to darkflow-master" in the command prompt this will change the directiory to darkflow master, then type jupyter notebook on the command prompt)
6. Run the SmartTrafficLight.ipynb notebook

## Issues
An issue you might encounter while running the notebook might be "AssertionError: expect 44948596 bytes, found 44948600
".
To solve this error go to "darkflow-master/darkflow/utils" folder open the loader.py file in a text editor.
In the loader.py file goto line 121 : self.offset = 16 and change this line to self.offset = 16 + ( 44948600 -44948596).
Save the file and run the SmartTrafficLight.ipnb notebook.

## Note
The current model works on a video feed due to lack of real time webcam images at the traffic signals but it can be modified to take real time video from the cameras placed at the signals. 
