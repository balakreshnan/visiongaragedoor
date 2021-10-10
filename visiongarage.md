# Home Open Garage door using Vision and license plate

## Use cognitive AI to recognzie the vehicle and license plate

## Use case

- Do it yourself Garage opener with AI
- Use Cognitive Vision AI to detect cars or trucks of home
- Ability to train your own models
- Use Form recognizer to detect license plate and get the details
- Based on vehicle and also validate with license plate
- If both are satisfied then send a signal to open the garage
- Garage door opener should be connected to relay
- Send the details back to garage to open

## Architecture

![Architecture](https://github.com/balakreshnan/visiongaragedoor/blob/main/images/garagevision.jpg "home garage opener")

## Architecture Details

- Get a simple camera
- Get a smart garage door opener or connect the garage door opener with relay
- Connect to Raspberry pi
- Connect the Raspberry pi to IoT hub
- Get minimum of 15 images of each vehicle used in home
- Create Cognitive service with custom vision
- Upload the 15 images of each vehicle
- In Custom vision tag each vehicle as tag name
- Do a object detection model
- configure and train the model
- Deploy the custom vision model
- now deploy the same images to form recognizer
- create tags for license plate reader
- configure the license plate details
- We need 5 pictures on all vehicles used
- Train the model and deploy
- Now connect the camera to raspberry pi
- for normal use
- Create a raspberry pi code to detect vehicle
- Take the image and send it to blob storage using IoT hub
- Use logic app to read the image and pass along to custom vision to detect which vehicle
- Then use logic app to send to form recognizer custom model to detect license plate details
- then pass that to function to validate and send signal back to IoT hub
- Write code to get the signal from iot hub
- Raspberry pi get the signal and relay open signal to garage door

## More to come

- Code to follow