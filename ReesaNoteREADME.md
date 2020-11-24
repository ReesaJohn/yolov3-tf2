The files I changed:

- dataset.py: load_fake_dataset function (to add depth channel to the xtrain)
- train.py:  main function (commented out everything I didn't use for readability)
- models.py: yolov3, yolov3tiny, darknet, and darknet tiny
    - Note: Since we are keeping the network fully convolutional, all I had to do
    was merely add an extra channel to these functions. Nothing else required the change
 
 Additional Info:
 
 The tiny network expects all images passed through it to be of the size x size
 dimension. The file dataset.py provides a way to resize the image and additionally divides 
 all channels by 255. If you want to use their function, make sure you keep this mind when you
 add the depth channel. If you don't want to use their function, make sure you scale the channels
 and resize the image to the size it expects.    
 