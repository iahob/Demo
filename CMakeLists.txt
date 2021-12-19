cmake_minimum_required(VERSION 3.20)
project(demo_folly_test)

set(CMAKE_CXX_STANDARD 14)

add_executable(demo_folly_test main.cpp)
target_include_directories(
        demo_folly_test PRIVATE
        /usr/local/Cellar/wangle/2021.12.13.00/include
        /usr/local/Cellar/folly/2021.12.13.00/include
        /usr/local/Cellar/gflags/2.2.2/include
        /usr/local/Cellar/openssl@1.1/1.1.1m/include
        /usr/local/Cellar/boost/1.76.0/include
        /usr/local/Cellar/glog/0.5.0/include
        /usr/local/Cellar/double-conversion/3.1.6/include
        /usr/local/Cellar/libevent/2.1.12/include

)
target_link_directories(
        demo_folly_test PRIVATE
        /usr/local/Cellar/wangle/2021.12.13.00/lib
        /usr/local/Cellar/folly/2021.12.13.00/lib
        /usr/local/Cellar/gflags/2.2.2/lib
        /usr/local/Cellar/openssl@1.1/1.1.1m/lib
        /usr/local/Cellar/boost/1.76.0/lib
        /usr/local/Cellar/glog/0.5.0/lib
        /usr/local/Cellar/double-conversion/3.1.6/lib
        /usr/local/Cellar/libevent/2.1.12/lib

)


target_link_libraries(demo_folly_test folly wangle gflags glog)