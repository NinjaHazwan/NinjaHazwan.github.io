---
layout: post
title: Understanding Transforms, Mapping and Navigation in ROS
description:  The Robot Operating System (ROS) is a flexible, open-source framework for writing robot software. It provides tools, libraries, and conventions to simplify the task of creating complex and robust robot behavior across a wide variety of robotic platforms. ROS is widely used in academia, research, and increasingly in commercial robotics due to its modular architecture and strong community support. Our current project involves designing a maze arena and implementing autonomous navigation using ROS1 on the Limo robot. In this page we display our learning on ROS1.
skills: 
  - Transformations
  - Mapping
  - Navigation

main-image: /ros.png

---

---
# ROS1 Introduction
## Key Features and Capabilities of ROS
**Modular System Architecture**: ROS nodes allow distributed development, improving maintainability and scalability.


**Sensor Integration**: ROS supports a wide range of sensors (LiDAR, IMU, cameras) with plug-and-play compatibility.


**Real-Time Data Handling**: ROS offers tools like tf2, rosbag, and rviz for real-time data processing, visualization, and debugging.


**Cross-Platform Interoperability**: Compatible with C++, Python, and embedded systems, allowing integration with diverse hardware.


**Simulation Support**: Tools like Gazebo and RViz help validate systems in virtual environments before deployment.

---

## Why ROS Matters 
**Accelerates Development**: ROS’s pre-built packages and active developer community reduce time-to-market for robotics solutions.


**Reduces Cost**: Open-source nature eliminates licensing fees, making advanced robotics development more cost-effective.


**Enhances Reliability**: Proven in real-world applications—from autonomous vehicles to industrial automation—ROS provides a stable foundation.


**Supports Scalability**: Whether you're prototyping or deploying at scale, ROS adapts easily to changing project sizes and complexities.


**Encourages Innovation**: With access to cutting-edge research tools and rapid prototyping capabilities, ROS fosters innovation in robotics applications.

---

# TF2
## Introduction to TF2
TF2 is the transform library for ROS. It maintains the relationship between coordinate frames in a tree structure buffered in time. It lets users transform points between any 2 coordinate frames at any desired point in time.

## How Transforms Are Published?
**Static Transformations**: ROS’s pre-built packages and active developer community that remains constant over time.
**Dynamic Transformations**: ROS’s pre-built packages and active developer community that changes continuously as the robot moves.

---

<!--## Embedding images 
### External images
{% include image-gallery.html images="https://live.staticflickr.com/65535/52821641477_d397e56bc4_k.jpg, https://live.staticflickr.com/65535/52822650673_f074b20d90_k.jpg" height="400"%}
<span style="font-size: 10px">"Starship Test Flight Mission" from https://www.flickr.com/photos/spacex/52821641477/</span>  
You can put in multiple entries. All images will be at a fixed height in the same row. With smaller window, they will switch to columns.  
-->
# Mapping & Navigation
## Mapping
In this project, we implemented 2D SLAM (Simultaneous Localization and Mapping) using the GMapping algorithm with TurtleBot3 in a Gazebo simulation environment under ROS Melodic. The system enables the robot to autonomously build a map of an unknown indoor environment while simultaneously estimating its position using laser scan data and wheel odometry. Visualization in RViz displayed the evolving occupancy grid map, showing explored areas, obstacles, and real-time laser feedback. We launched the simulation world, ran the SLAM node, and manually teleoperated the robot to explore and construct the map. This setup demonstrated our understanding of robot perception, ROS packages, coordinate transforms, and real-time mapping in a simulated robotics context.

{% include image-gallery.html images="mapping.png" height="400" %} 
            *Turtlebot3 scanning surroundings to build map in RVIZ*

{% include image-gallery.html images="mapping full.png" height="400" %} 
            *Fully scanned map displayed in RVIZ*


## Navigation
In this project, we implemented autonomous navigation for TurtleBot3 using the move_base package in the ROS Navigation Stack within a Gazebo simulation. After generating the map using SLAM, the robot was able to localize itself and navigate to user-defined goals using global and local costmaps. The RViz interface displayed real-time obstacle inflation, path planning, and costmap layers—highlighting how the robot dynamically computed safe paths and avoided obstacles in a structured indoor environment. We configured key ROS components such as AMCL for localization, global and local planners, and costmap parameters. This project deepened my understanding of autonomous mobility, sensor integration, and real-time decision-making in robotic systems.

{% include image-gallery.html images="move_base1.png" height="400" %}
{% include image-gallery.html images="SEP1 pic.png" height="400" %} 
            *TurtleBot3 using move_base to navigate pass obstacles to a selected point in map*

            
<!--### Embeed images
{% include image-gallery.html images="mapping.png" height="400" %} 
place the images in project folder/images then update the file path. -->   


<!--## Embedding youtube video
The second video has the autoplay on. copy and paste the 11-digit id found in the url link. <br>
*Example* : https://www.youtube.com/watch?v={**MhVw-MHGv4s**}&ab_channel=engineerguy
{% include youtube-video.html id="MhVw-MHGv4s" autoplay= "false"%}
{% include youtube-video.html id="XGC31lmdS6s" autoplay = "true" %}

you can also set up custom size by specifying the width (the aspect ratio has been set to 16/9). The default size is 560 pixels x 315 pixels.  

The width of the video below. Regardless of initial width, all the videos is responsive and will fit within the smaller screen.
{% include youtube-video.html id="tGCdLEQzde0" autoplay = "false" width= "900px" %} --> 

<!-- <br>

## Adding a hozontal line
---

## Starting a new line
leave two spaces "  " at the end or enter <br>

## Adding bold text
this is how you input **bold text**

## Adding italic text
Italicized text is the *cat's meow*.

## Adding ordered list
1. First item
2. Second item
3. Third item
4. Fourth item

## Adding unordered list
- First item
- Second item
- Third item
- Fourth item

## Adding code block
```ruby
def hello_world
  puts "Hello, World!"
end
```

```python
def start()
  print("time to start!")
```

```javascript
let x = 1;
if (x === 1) {
  let x = 2;
  console.log(x);
}
console.log(x);

```

## Adding external links
[Wikipedia](https://en.wikipedia.org)


## Adding block quote
> A blockquote would look great if you need to highlight something


## Adding table 

| Header 1 | Header 2 |
|----------|----------|
| Row 1, Col 1 | Row 1, Col 2 |
| Row 2, Col 1 | Row 2, Col 2 |

make sure to leave aline betwen the table and the header -->


