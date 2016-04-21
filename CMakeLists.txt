cmake_minimum_required(VERSION 2.8)

find_package(Boost COMPONENTS system thread REQUIRED)

include_directories(
	${Boost_INCLUDE_DIRS}
)

add_executable(client client.cpp)
add_executable(server server.cpp)
target_link_libraries(client ${Boost_LIBRARIES})
target_link_libraries(server ${Boost_LIBRARIES})
