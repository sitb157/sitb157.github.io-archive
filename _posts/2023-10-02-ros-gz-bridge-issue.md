---
layout: post
title: Gz Garden Install Issue  
tags: 
 - ROS2
 - Issue
---
<br/>
<br/>

### Gazebo Garden install 후 Demo Test 과정 중 Issue
#### ros_gz_bridge error
ros_gz_bridge 중 paramter_bridge를 사용해도 ros2 topic으로 안넘어오는 issue 발견  
[예시](https://index.ros.org/p/ros_gz_bridge/)를 진행해도 해결을 못해서 관련 비슷한 issue를 검색  
비슷한 [issue](https://github.com/gazebosim/ros_gz/issues/365)를 발견  
![image](https://github.com/sitb157/sitb157.github.io/assets/108820413/c42cfc6f-3917-47e1-b666-27478a023f12)<br/>
하지만, 해결이 안되고 계속 질문하여 Dockerfile 작성 시 GZ_VERSION을 구체적으로 설정함으로 해결하여 마무리로 된 것으로 확인함    
![image](https://github.com/sitb157/sitb157.github.io/assets/108820413/4514ac9a-a82d-4b65-915c-d47f294b369e)<br/>
동일한 방법을 DockerFile 수정 후 try 해보니 ros2 topic echo으로 센서 데이터 및 기타 토픽 받을 수 있게 되었음.
