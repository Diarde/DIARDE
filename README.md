# What is DIARDE? 

DIARDE, an acronym for DIgital ARchitecture And DEsign is a software collection for extracting interior space geometries and measures from photos and creating 3-D models and CAD files as commonly used in interior design projects. 

DIARDE is intended to be a service; the user takes photos with his or her smartphone and uploads these using the generic 
web app or the native app (currently only Android is natively supported). The service provider, this could be a person 
offering the service or the architect or even the client himself, will use DIARDE-Tool to extract the room geometry and measures
and build a 3-D representation. The user/client is able to view the 3-D model and request SketchUp and AutoCAD files. 

DIARDE Tool is certainly the central component of DIARDE and combines conventional photogrammetric methods, custom built algorithms
and Computer Vision Neural Networks. Utilising Neural Networks is still very much work in progress. With increasing support of 
AI the importance of the human-in-the-loop service provider will decrease. Evenytually DIARDE might be able to operate fully automatically.
# How did it start and why does it matter?

Interior design projects often start with an architect or designer visiting the premise that should be remodelled, refurbished or 
redisigned. Armed with a yardstick or a a laser pointer measuring device, lengths, heights and distances are manually obtained. Back 
in the office the architect and/or designer will build a faithful digital representation of the interior space, which are crucial for all phases of building the concept and design.  

Given the fact that an architect travelling to the sites, manually obtraining the dimensions, buiuldin gth edigital model is tedidous means that the stakes are high. What if there was a simple solution? Instead of measuring the space manually the architect
or even the client himself takes pictures of the space and the geometric information encoded in the photos will be used to generate 
CAD models for the architects. 

So far so good, aren't there solution out there that do exactly that? Yes and no, there are apps and tools that generate floorplans and/or CAD models from photos or video scans. We believe that a lot of good ideas and approaches exist but none of the commerical solutions really seems to account for the particular requirements architects have. Precision is foremost important and +/- 2cm for 
typically sized office or domestic spaces is needed. Apps avaiable on the app stores do not seem to be able to exceed 1-2% precision, which corresponds to up to 10cm deviation for 5m long walls. 

Anybody designing a photo measurment system for interior spaces inevitably faces a trade-off between easy of use and quality offered.
Most commercial products seem to favor easy-of-use in a way that the offerec precision is not suitable for architects and other players in similiar industires (carpenters/kitchen fitters etc). DIARDE was designed to cover that sweet spot, that gives precision for architects and yet is still relatively easy to use and operate.  
# Is DIARDE already operable?

Yes, we have tested and used DIARDE successfully in the context of interior design projects. Obviously there is margin for 
improvements and we hope that over time DIARDE becomes easier to use, more automated and give better and more consistent results.
# Enough TL;DR sentiments, show me an example please....

Take photos of your room with your smart phone. The photos should overlap and have common reference points in the 
overlapping area. There is no one way to take the perfect set of photos or how many photos should be taken. The 
example below features 6 photos. While more photos potentially increase precision a few photos per room are often sufficient and 
in most cases 4 photos are enough:

<p align="center">
  <img src="https://raw.githubusercontent.com/Diarde/DIARDE/main/doc/picture1.png" />
</p>

if you look closely at these sample photos you will see A4-paper attached to some walls. A4-papers provide a reference length
and for each room we need at least one reference length, which can be an A4-paper or a yardstick on the ground or even simply 
the hight of the room or the lengths of a window frame.

After taking your images, navigate to mobile.diarde.com on your smart phone, register with your email, add a new project
and upload the photos: 

<p align="center">
  <img src="https://raw.githubusercontent.com/Diarde/DIARDE/main/doc/picture2.png" />
</p>


After the photos were uploaded the server DIARDE-Tool will be used to extract the room geometry and build the 3-D model. 
Please refer to [DIARDETool](https://github.com/Diarde/DIARDETool#readme) to get an understanding how rooms are modelled.

The created 3-D model and layout plan will be visible to the user:

<p align="center">
  <img src="https://raw.githubusercontent.com/Diarde/DIARDE/main/doc/picture3.png" />
</p>

DIARDE features plugins for SketchUp and AutoCAD to generate CAD files:

<p align="center">
  <img src="https://raw.githubusercontent.com/Diarde/DIARDE/main/doc/picture4.png" />
</p>

These can be requested by the user. 
# DIARDE software components

DIARDE was designed as a web based service and consists of following components:

* [DIARDETool](https://github.com/Diarde/DIARDETool#readme): The central component of DIARDE, a graphical web-app created with Angular 2+ to extract room geometries.
* [DIARDEBackEnd](https://github.com/Diarde/DIARDEBackEnd#readme): an express powered back end. The back end is backed by a MongoDB database.
* [DIARDEMobile](https://github.com/Diarde/DIARDEMobile#readme): an web app for the smartphone where users can upload room photos and view 3-D models and floorplans.
* [DIARDEAdmin](https://github.com/Diarde/DIARDEAdmin#readme): a web app, designed to manage the system from a desktop computer. Created with Angular 2+. 
* [DIARDEForSketchUp](https://github.com/Diarde/DIARDEForSketchUp#readme): a plugin to load the room models into sktechup. 
* [DIARDEForDXF](https://github.com/Diarde/DIARDEForDXF#readme): A tool to generate a dxf file for room models. 

DIARDE Legacy code:

* DIARDEKotlinPort: a kotlin port of DIARDE tool. deprecated
* DIARDEForAutoCAD: 
* 
# Sure, I understand the concept but can you fill me in with some key ideas and technology used? 

Giving you some details of the solution probably is not the easiest task and we have decided to give further detail 
at the repositories of DIARDE's various components. 

Also, feel free to browse all DIARDE repositories: and find the info you are looking for. Last but not least, 
the info you might be looking for might not be available at the moment. If so, please do not hesitate to 
requet more info via email: studiocinqo@gmail.com. 

# How do I get started? 

You can try the existing solution by navigating to mobile.diarde.com upload photos. We will try to process the photos as soon as possible. Alternatively you could use the diarde tool to extract your model yourself. 
If you are interested in contributing code, and we really appreciate any help, let us know what you your expertise are and what you would like to work on and we will decide together how you can help push DIARDE. 
# Where do I get help if I need it? 

Write an email to studiocinqo@gmail.com or use the signal app to drop us a line: 
# Why do I want to contribute?

DIARDE is designed to be a service and is consists of various components. So, no matter what your field of interest is, you are likely to find a task that is suited for you. 
You are into computer vision and algorithmic work? There are alot of opportunities to improve on the current algorithms to calculate
the models and an abundance of ideas for new features. 
You are into the AI side of computer vision? Sure, the tool to extract the room geometries is mostly manually now, but there are
very good ideas use CNN based neural networks for automatisation of the process 
You are into back end development and like database design? Surem you can be resolsible for the back end
You like front end development and  ? The web-app, the admin panel and well as the tool to load the photos and extract the dimensions need work. 

# RoadMap

 - Need Tests
 - Add native app for iphones
 - Add depth map support LIDAR, ARCore
 - incorporate support for CNN networks - RoomNet, 
 - Add support for stitching multiple rooms together
 - 
