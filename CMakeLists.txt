cmake_minimum_required(VERSION 2.8.3)
project(social_msgs)
find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  message_generation
  std_msgs
)

add_message_files(
   DIRECTORY msg
   FILES
    People.msg
    Person.msg
    Group.msg
    GroupArray.msg
    Objects.msg
    Object.msg
    Locals.msg
    Local.msg
    PointArray.msg
		Destination.msg
)

add_service_files(
  FILES
	DestinationArray.srv
)

generate_messages(
   DEPENDENCIES
   geometry_msgs
   std_msgs
)

catkin_package(
    CATKIN_DEPENDS
    geometry_msgs
    message_runtime
    std_msgs
)
