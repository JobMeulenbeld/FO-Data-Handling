cmake_minimum_required(VERSION 3.25)
project(FO_Data_Handling)

set(CMAKE_CXX_STANDARD 17)

include(ExternalProject)

set(EXTERNAL_INSTALL_LOCATION ${CMAKE_CURRENT_SOURCE_DIR}/lib)

ExternalProject_Add(mqtt
        GIT_REPOSITORY https://github.com/JobMeulenbeld/FO-MQTT.git
        )

include_directories(${EXTERNAL_INSTALL_LOCATION}/include)

add_executable(${PROJECT_NAME} ${PROJECT_SOURCE_DIR}/main.cpp)
