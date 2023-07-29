qt_add_library(qmlWeatherBaseStation STATIC)
qt_add_qml_module(qmlWeatherBaseStation
    URI WeatherBaseStation
    VERSION 1.0
    QML_FILES
        main.qml
)
