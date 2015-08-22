# TrainModel
This application is an java project developed in Eclipse. It will be used to train a *Random Forest* model that will be loaded later an Android app: [Pickup](https://github.com/miworking/TrainModel)

#### Data format and related features
It will calculate 104 feature from collected Accelerometer and Magnetic data
[104 features](https://www.dropbox.com/s/bnvwc62nh7kt24q/Pickup.pptx?dl=0)will be abstracted
[{Accelerometer, Magnetic} * {X,Y,Z,Magnitude} * {Mean, Std, Min, Max, Percentile25,50,75, FTT[0,1,2]}]


#### Related Classes
All data related classes will be placed in [***pattern***](https://github.com/miworking/XFactor_PickupRecognition/tree/master/app/src/main/java/edu/cmu/ebiz/pickup/pattern) package

- [DoubleFeatureUnit]
(https://github.com/miworking/XFactor_PickupRecognition/blob/master/app/src/main/java/edu/cmu/ebiz/pickup/pattern/DoubleFeatureUnit.java) is the basic class,

- [XYZFeature](https://github.com/miworking/XFactor_PickupRecognition/blob/master/app/src/main/java/edu/cmu/ebiz/pickup/pattern/XYZFeature.java)  has 4 DoubleFeatureUnit members: X,Y,Z,V (Magnitude of X,Y,Z)

- [Feature](https://github.com/miworking/XFactor_PickupRecognition/blob/master/app/src/main/java/edu/cmu/ebiz/pickup/pattern/Feature.java) class contains 2 XYZFeature members: accelerometer and magnetic

- [OnePersonData](https://github.com/miworking/XFactor_PickupRecognition/blob/master/app/src/main/java/edu/cmu/ebiz/pickup/pattern/OnePersonData.java) has a list of Feature as its member, and calculate features from it

To be consistent with Pickup app, this [patter](https://github.com/miworking/TrainModel/tree/master/src/pattern) package is the same one that is used in [Pickup app](https://github.com/miworking/XFactor_Pickup/tree/master/app/src/main/java/edu/cmu/ebiz/pickup/pattern)