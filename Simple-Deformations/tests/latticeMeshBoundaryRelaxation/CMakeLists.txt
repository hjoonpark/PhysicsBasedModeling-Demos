add_executable (latticeMeshBoundaryRelaxation
        main.cpp
        )

target_include_directories(latticeMeshBoundaryRelaxation
        PUBLIC
            ${USD_INC_DIR}
        )

target_link_libraries(
        latticeMeshBoundaryRelaxation
                ${USD_LIB_DIR}/libusd_gf.so
                ${USD_LIB_DIR}/libusd_sdf.so
                ${USD_LIB_DIR}/libusd_tf.so
                ${USD_LIB_DIR}/libusd_usd.so
                ${USD_LIB_DIR}/libusd_usdGeom.so
                ${USD_LIB_DIR}/libusd_vt.so
                ${USD_LIB_DIR}/libboost_python.so.1.66.0
                /usr/lib/x86_64-linux-gnu/libpython2.7.so.1.0
        )
