cmake_minimum_required(VERSION 3.0.2)
project(roboticarts_msgs)


find_package(catkin REQUIRED COMPONENTS
    std_msgs
    std_srvs
    message_generation
)


#add_message_files(DIRECTORY msg
#    FILES
#
#)


add_service_files(DIRECTORY srv
    FILES
    SetString.srv
    SetLeds.srv
)


generate_messages(
   DEPENDENCIES
   std_msgs std_srvs
)


catkin_package(CATKIN_DEPENDS 
    std_msgs
    std_srvs
    message_runtime
)

