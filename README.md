# RAM-Storyboards-Demo

A demo application to show how to use multiple Storyboard files with a [`RAMAnimatedTabBarController`](https://github.com/Ramotion/animated-tab-bar). I saw the problem outlined [here](https://github.com/Ramotion/animated-tab-bar/issues/93), and used container view controllers and Storyboard references to get this working.

Follow the steps outlined below.

(1) Create the desired view controller in its own Storyboard:

<img width="1552" alt="screen shot 2016-08-23 at 2 28 26 am" src="https://cloud.githubusercontent.com/assets/879038/17882277/7dc8a2b0-68d9-11e6-886d-391f7a272ef7.png">

(2) Create an empty view controller in the Storyboard that contains the main tab bar:

<img width="1552" alt="screen shot 2016-08-23 at 2 37 56 am" src="https://cloud.githubusercontent.com/assets/879038/17882466/9e593dcc-68da-11e6-9cad-dd80077d8f4a.png">

(3) Add that view controller to the `viewControllers` property of the tab bar controller:

![step-3](https://cloud.githubusercontent.com/assets/879038/17882496/bf3526d2-68da-11e6-85b8-d02d11862263.gif)

(4) Add a Container View to that empty view controller, delete view controller that it automatically embeds, and constrain it to the edges of its superview:

![step-4](https://cloud.githubusercontent.com/assets/879038/17882617/734aaef8-68db-11e6-865b-afc159897f4f.gif)

(5) Follow steps 3-5 outlined [here](https://github.com/Ramotion/animated-tab-bar#usage) for *all* tab bar items on the tab bar.

(6) Embed the view controller from the other Storyboard via a Storyboard Reference in that container view:

![step-6](https://cloud.githubusercontent.com/assets/879038/17882666/daffd898-68db-11e6-8a18-51068e8074e1.gif)

(7) Build and run:

![run](https://cloud.githubusercontent.com/assets/879038/17882700/174635b8-68dc-11e6-991c-9a01ab3e6fe0.gif)

Thanks to [@jeffaburt](https://github.com/jeffaburt) for helping look into this!
