add_executable (GroundCollision1
        main.cpp
        )

# if CMake cannot use find_package for Eigen, use the explicit include path instead
# find_package(Eigen3)

# eigen
find_package (Eigen3 3.3 REQUIRED NO_MODULE)
target_link_libraries (GroundCollision1 Eigen3::Eigen)
message("Eigen found: ${EIGEN3_INCLUDE_DIR}")
# set(EIGEN3_INCLUDE_DIRS /usr/include/eigen3/)

target_include_directories(GroundCollision1
        PUBLIC
            ${USD_INC_DIR}
            ${EIGEN3_INCLUDE_DIRS}
            ${PYTHON_INCLUDE_PATH}
        )

target_link_libraries(
        GroundCollision1
        ${USD_LIB_DIR}/libusd_gf.so
        ${USD_LIB_DIR}/libusd_sdf.so
        ${USD_LIB_DIR}/libusd_tf.so
        ${USD_LIB_DIR}/libusd_usd.so
        ${USD_LIB_DIR}/libusd_usdGeom.so
        ${USD_LIB_DIR}/libusd_vt.so
        ${USD_LIB_DIR}/libboost_python.so.1.66.0
        /usr/lib/x86_64-linux-gnu/libpython2.7.so.1.0
)

# eigen
find_package (Eigen3 3.3 REQUIRED NO_MODULE)
target_link_libraries (GroundCollision1 Eigen3::Eigen)
message("Eigen found: ${EIGEN3_INCLUDE_DIR}")