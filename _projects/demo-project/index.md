---
layout: post
title: Understanding Transforms, Mapping and Navigation in ROS
description:  The Robot Operating System (ROS) is a flexible, open-source framework for writing robot software. It provides tools, libraries, and conventions to simplify the task of creating complex and robust robot behavior across a wide variety of robotic platforms. ROS is widely used in academia, research, and increasingly in commercial robotics due to its modular architecture and strong community support. Our current project involves designing a maze arena and implementing autonomous navigation using ROS1 on the Limo robot. In this page we display our learning on ROS1.
skills: 
  - Transformations
  - Mapping
  - Navigation

main-image: /ros.png
![ROS Navigation]({{ page.main-image }}){: style="width: 65%; max-width: 600px; display: block; margin: 20px auto; border: 1px solid #eee; border-radius: 4px;"}

---

---
# ROS1 Introduction
## Key Features and Capabilities of ROS
**Modular System Architecture**: ROS nodes allow distributed development, improving maintainability and scalability.


**Sensor Integration**: ROS supports a wide range of sensors (LiDAR, IMU, cameras) with plug-and-play compatibility.


**Real-Time Data Handling**: ROS offers tools like tf2, rosbag, and rviz for real-time data processing, visualization, and debugging.


**Cross-Platform Interoperability**: Compatible with C++, Python, and embedded systems, allowing integration with diverse hardware.


**Simulation Support**: Tools like Gazebo and RViz help validate systems in virtual environments before deployment.

## Why ROS Matters 
**Accelerates Development**: ROS’s pre-built packages and active developer community reduce time-to-market for robotics solutions.


**Reduces Cost**: Open-source nature eliminates licensing fees, making advanced robotics development more cost-effective.


**Enhances Reliability**: Proven in real-world applications—from autonomous vehicles to industrial automation—ROS provides a stable foundation.


**Supports Scalability**: Whether you're prototyping or deploying at scale, ROS adapts easily to changing project sizes and complexities.


**Encourages Innovation**: With access to cutting-edge research tools and rapid prototyping capabilities, ROS fosters innovation in robotics applications.

# TF2
## Introduction to TF2
TF2 is the transform library for ROS. It maintains the relationship between coordinate frames in a tree structure buffered in time. It lets users transform points between any 2 coordinate frames at any desired point in time.



<!--## Embedding images 
### External images
{% include image-gallery.html images="https://live.staticflickr.com/65535/52821641477_d397e56bc4_k.jpg, https://live.staticflickr.com/65535/52822650673_f074b20d90_k.jpg" height="400"%}
<span style="font-size: 10px">"Starship Test Flight Mission" from https://www.flickr.com/photos/spacex/52821641477/</span>  
You can put in multiple entries. All images will be at a fixed height in the same row. With smaller window, they will switch to columns.  
-->
### Embeed images
{% include image-gallery.html images="SEP1 pic.png" height="400" %} 
place the images in project folder/images then update the file path.   


## Embedding youtube video
The second video has the autoplay on. copy and paste the 11-digit id found in the url link. <br>
*Example* : https://www.youtube.com/watch?v={**MhVw-MHGv4s**}&ab_channel=engineerguy
{% include youtube-video.html id="MhVw-MHGv4s" autoplay= "false"%}
{% include youtube-video.html id="XGC31lmdS6s" autoplay = "true" %}

you can also set up custom size by specifying the width (the aspect ratio has been set to 16/9). The default size is 560 pixels x 315 pixels.  

The width of the video below. Regardless of initial width, all the videos is responsive and will fit within the smaller screen.
{% include youtube-video.html id="tGCdLEQzde0" autoplay = "false" width= "900px" %}  

<br>

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

make sure to leave aline betwen the table and the header


