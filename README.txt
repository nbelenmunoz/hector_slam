===========================================================================================================================
						Descargas previas al uso 
===========================================================================================================================
 Hector-Slam modificado funcional de Belen: https://github.com/nbelenmunoz/hector_slam.git
 RpLidar paquete de ros: https://github.com/Slamtec/rplidar_ros
 
  Se tiene que hacer con el comando "git clone" una copia al workspace de ROS (noetic)
  	$git clone «Repo que quieran» 
	$catkin build
	$source devel/setup.bash

 En caso de error al utilizar los paquetes, cerrar terminales y repetir el catkin build
 
===========================================================================================================================
							Puerto
===========================================================================================================================
 Si no se autoriza el puerto previo a su uso, NO SE PODRA DETECTAR EL LIDAR y por ende los datos.
 Compruebe la autoridad del puerto serie de rplidar:
 
 	$ls -l /dev |grep ttyUSB
 
 Agregue la autoridad de escritura: (como /dev/ttyUSB0)

 	$sudo chmod 666 /dev/ttyUSB0

===========================================================================================================================
							Uso
===========================================================================================================================
--Primera terminal
	$cd
	$roscore

--Segunda terminal
	$roslaunch hector_slam_launch tutorial.launch

NOTA: Si existe algun error, algun paso se hizo mal previamente. Se recomienda hacer catkin build cada vez que se reinicia 
la computadora o se modifico algun script dentro de los paquetes. 
