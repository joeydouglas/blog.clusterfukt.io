---
title: "Don't Get Baked!"
date: 2019-06-29T13:30:26-05:00
draft: false
cover: "/images/vape-cloud.jpg"
---
---
## Wait. You mean "cloud native" doesn't mean getting baked?
That's totally up to you. Do your thang, but dont bake your config into the container image. The entire point of the containerizing your app is so that it's reusable across any environment.

Regardless of why a travesty like this might happen, you could find yourself in a situation where you have to deploy such an image. Lets say that you don't have access to the repo with any of the code. Peculiar circumstances block you from reaching out to the creators of this majestic beast of a container and you have to make it work. Good times. Here are a few tricks you could use to assess the damage and override the baked in configuration so that the application will bow to your will. 

1. run the pod and exec into it. 
   1. hopefully it'll start so you can do this. 
2. initContainer
   1. to copy a new entrypoint.sh
   2. set config to pull from env.
3. Mount files to override what currently exist.

