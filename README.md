<h1> Create Robot Navigation using SLAM</h1>
<p> TurtleBot3 is a platform robot of ROS. I should install it on ROS Melodic. TurtleBot3 runs SLAM technology to build and save a map in the physical environment. It continuously acquires the data from the real world in the form of dots and feeds it into machines to make them percept and grasp the surrounded environment. It can be utilized in various technologies such as AI, games, robotics and Augmented Reality (AR) to provide an immersive and interactive experience. Using SLAM technique, can recognize and avoid obstacles like objects and walls in the real world.</p>
<h2> Installing TurtleBot3 Package for ROS Melodic.</h2>
<p> Access to src directory to downloud and install the important Turtlebot3 packages on ROS Melodic.</p>
<div class="snippet-clipboard-content position-relative" data-snippet-clipboard-copy-content="  Number of colours/ shades = 2^bpp where bpp represents bits per pixel.
"><pre><code>cd ~/catkin_ws/src
git clone https://github.com/ROBOTIS-GIT/turtlebot3.git
git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
git clone https://github.com/ROBOTIS-GIT/turtlebot3_autorace.git</code></pre></div>
<p> To install package dependency, run:</p>
<div class="snippet-clipboard-content position-relative" data-snippet-clipboard-copy-content="  Number of colours/ shades = 2^bpp where bpp represents bits per pixel.
"><pre><code>rosdep install --from-paths src -i -y
source ~/catkin_ws/devel/setup.bash</code></pre></div>
<p> To speed up the running process and prevent the latency of crawling through the packages in ROS_ROOT, run:</p>
<div class="snippet-clipboard-content position-relative" data-snippet-clipboard-copy-content="  Number of colours/ shades = 2^bpp where bpp represents bits per pixel.
"><pre><code>rospack profile</code></pre></div>
<p> We use one type of Turtlebot3 models either burger or waffle, then we run bashrc which is shell script to run automatically</p>
<p> when a user opens a new shell</p>
<div class="snippet-clipboard-content position-relative" data-snippet-clipboard-copy-content="  Number of colours/ shades = 2^bpp where bpp represents bits per pixel.
"><pre><code>echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc
source ~/.bashrc </code></pre></div>

<h2> Unknown Navigation of Turtlebot3 in Gazebo World.</h2>

<p> After setting up the  Turtlebot3 environment correctly, Gazebo simulator should be opened with small robotic inside it.</p>
<p> Type, the following command:</p>
<div class="snippet-clipboard-content position-relative" data-snippet-clipboard-copy-content="  Number of colours/ shades = 2^bpp where bpp represents bits per pixel.
"><pre><code>roslaunch turtlebot3_gazebo turtlebot3_world.launch</code></pre></div>
<img src= "Images/Gazebo.png" width="451" height="350">
<p> Run the SLAM RViz.</p>
<div class="snippet-clipboard-content position-relative" data-snippet-clipboard-copy-content="  Number of colours/ shades = 2^bpp where bpp represents bits per pixel.
"><pre><code>roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=karto</code></pre></div>
<img src= "Images/map_Rviz.png" width="350" height="350">
