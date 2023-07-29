cmake_minimum_required(VERSION 3.16)

project(WeatherBaseStation VERSION 0.1 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt6 COMPONENTS Quick REQUIRED)
qt_standard_project_setup()

add_subdirectory(src)
add_subdirectory(qml)

target_link_libraries(appWeatherBaseStation
    PRIVATE
      Qt6::Quick
      qmlWeatherBaseStationplugin
)

install(TARGETS appWeatherBaseStation
    BUNDLE DESTINATION .
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR})
