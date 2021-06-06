# What is DIARDE? 

DIARDE, an acronym for Digital Architecture And Design is a software to create 3-D models and CAD files of rooms and interior spaces
solely based on photos. It is intended to be a service and the user takes photos with his or her smartphone and uses the a web app
or the native app (at the moment only avaiable for Android) to upload the photos to the server. A AI-ready tool then is used to model the room based on the pictures uploaded. Once the model is ready the user will have the model as well as a floorplan of the room on the phone and download options to request the CAD files in SketchUp and AutoCAD format. 

# How did it start and why does it matter so much to us?

Interior design projects often start with an architect or designer visiting the space that should be remodelled using a laser 
pointer measuring device to get dimensions of the rooms. These dimensions will then later in the architects office be used to create
a digital model of the room. These models are always used as base for the interior space remoddeling concept. At this point, the 
potential client has not yet approved the concept and might as well decide to contract a different designer. 

Given the fact that an architect travelling to the sites, manually obtraining the dimensions, buiuldin gth edigital model is tedidous means that the stakes are high. What if there was a simple solution? Instead of measuring the space manually the architect
or even the client himself takes pictures of the space and the geometric information encoded in the photos will be used to generate 
CAD models for the architects. 

So far so good, aren't there solution out there that do exactly the same? Yes and no, there are apps and tools that generate floorplans or even CAD models from photos or video scans. There are a lot of good ideas and approaches out there but none really seems to account for the requirements in precision the architects need. Architects need models that are accurate up to +/- 2 cm for
typical spaces. So how does that compare to app available on the app store? App, even when used with LiDAR enabled devices are usually limited in their precision to 1-2%, which amounts to up to 10 cm difference for 5 meter long walls. You wont find an architect that is happy with these deviations. 

# How far is the development of DIARDE?

DIARDE was designed as a web based service and consists of following components:

* DIARDEBackEnd: an express powered back end. The back end is backed by a MongoDB database.
* DIARDEAdmin: a web app, designed to manage the system from a desktop computer. The admin tool is created with Angular 2+. 
* DIARDETool: the central component of DIARDE, a graphical web-app created with Angular 2+. Used to extract room geometries.
* DIARDEWebApp: an web app for the smartphone where users can upload room photos and view 3-D models and floorplans.

# Enough TLDR sentiments, show me an example please....

![alt text](https://raw.githubusercontent.com/Diarde/DIARDE/main/doc/picture1.png)

# Sure, I understand the concept but can you fill me in with some key ideas and technology used? 


# How do I get started? 



# Where do I get help if I need it? 


# Why should I contribute?

DIARDE is designed to be a service and is consists of various components. So, no matter what your field of interest is, you are likely to find a task that is suited for you. 
You are into computer vision and algorithmic work? There are alot of opportunities to improve on the current algorithms to calculate
the models and an abundance of ideas for new features. 
You are into the AI side of computer vision? Sure, the tool to extract the room geometries is mostly manually now, but there are
very good ideas use CNN based neural networks for automatisation of the process 
You are into back end development and like database design? Surem you can be resolsible for the back end
You like front end development and  ? The web-app, the admin panel and well as the tool to load the photos and extract the dimensions need work. 
