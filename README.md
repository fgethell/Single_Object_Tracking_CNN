# Single Object Tracking - Integrating a CNN based Detector into a Camshift Tracker
The methodology of single object tracking enables us to predict the trajectory of an object of interest in a sequence of videos by detecting and analyzing their properties and movement patterns. We investigate three methodologies to track a single object in a video by applying a Convolutional Neural Network (CNN) based pedestrian detector, state-of-the-art Camshift Tracking algorithm and a proposed hybrid methodology combining these. CNN object detection deployed using Caffe, identifies objects in a frame of reference using various properties like shape, color, orientation, etc. by learning various kernels that extract these unique identifiable features. On the other hand, the Camshift algorithm leverages probability distribution of colors in the Region of Interest to identify the centroid (using Mean shift) and further predict the new bounding boxes. By applying these methods as an ensemble, we investigate how tracking performance can be improved by resetting the RoI after regular intervals of frame. We also compare the performance of tracking using a detector as well as Camshift across 3 parameters: average Intersection over Union (IoU) with the ground truth bounding box, percentage of frames with missed detections and total computation time. As a result, we conclude that the detector performs the best overall, and can assist in significantly boosting the tracking performance of a typical Camshift Tracker at the expense of computation time.
