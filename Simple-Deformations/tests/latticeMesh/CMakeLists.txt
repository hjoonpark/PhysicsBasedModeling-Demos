add_executable (latticeMesh
        main.cpp
        )

target_include_directories(latticeMesh
        PUBLIC
            ${USD_INC_DIR}
        )

target_link_libraries(
        latticeMesh
                ${USD_LIB_DIR}/libusd_gf.so
                ${USD_LIB_DIR}/libusd_sdf.so
                ${USD_LIB_DIR}/libusd_tf.so
                ${USD_LIB_DIR}/libusd_usd.so
                ${USD_LIB_DIR}/libusd_usdGeom.so
                ${USD_LIB_DIR}/libusd_vt.so
                ${USD_LIB_DIR}/libboost_python.so.1.66.0
                /usr/lib/x86_64-linux-gnu/libpython2.7.so.1.0
        )
