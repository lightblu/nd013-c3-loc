# Udacity Self Driving Car Engineer C3 Localization 

- Goal: localize a car driving in simulation for at least 170m from the starting position and never exceeding a distance pose error of 1.2m. The simulation car is equipped with a lidar, provided by the simulator at regular intervals are lidar scans. There is also a point cloud map map.pcd already available, and by using point registration matching between the map and scans localization for the car can be accomplished. This point cloud map has been extracted from the CARLA simulator.

All work will be done in the project workspace included later in this lesson.



(venv) root@5a1975f7c33f:/home/workspace/c3-project# ./cloud_loc 
WARNING: Version mismatch detected: You are trying to connect to a simulator that might be incompatible with this API 
WARNING: Client API version     = 0.9.9.4-296-g201bc254-dirty 
WARNING: Simulator API version  = 0.9.10 
terminate called after throwing an instance of 'std::runtime_error'
  what():  Spawn failed because of collision at spawn position
Aborted (core dumped)



1. Compile the code (Terminal Tab 1)

	cd /home/workspace/c3-project
	cmake .
	make
    
(*Once 1 is done, usually running make alone is enough (unless adding files to CMakeLists.txt)*)


2. Launch the simulator in a new terminal tab (Terminal Tab 2)

	su - student
	cd /home/workspace
	./run-carla.sh

3. Run the project code back in the first tab (Terminal Tab 1)

	cd /home/workspace/
	./cloud_loc
    
    
    
PCL docs: https://pointclouds.org/documentation/



final working approach seemed to mostly need low number of iterations to be fast enough

lower lower_fov to focus less on floor and efficiency
resolutions tried

