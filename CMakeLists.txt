cmake_minimum_required(VERSION 3.25)
project(FO_Data_Handling)

set(CMAKE_CXX_STANDARD 17)

add_executable(FO_Data_Handling main.cpp ${PROJECT_SOURCE_DIR}/lib/FO-MQTT/include/MQTT_Handler.h ${PROJECT_SOURCE_DIR}/lib/FO-MQTT/src/MQTT_Handler.cpp)
include_directories(${PROJECT_SOURCE_DIR}/lib/FO-MQTT/lib/paho_c/include)
target_link_libraries(${PROJECT_NAME} ${PROJECT_SOURCE_DIR}/lib/FO-MQTT/lib/paho_c/paho-mqtt3c.dll)