cmake_minimum_required(VERSION 3.14.0)
project(rotors_comm)
find_package(
  catkin REQUIRED COMPONENTS cmake_modules geometry_msgs message_generation
                             std_msgs)

# Declare the service files to be built
add_service_files(FILES RecordRosbag.srv)

add_message_files(FILES WindSpeed.msg)

generate_messages(DEPENDENCIES geometry_msgs std_msgs)

catkin_package(CATKIN_DEPENDS message_runtime)
