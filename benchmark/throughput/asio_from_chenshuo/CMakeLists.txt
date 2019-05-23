find_package(Boost REQUIRED COMPONENTS system thread)

include_directories("/home/chenzheng/Downloads/boost_1_70_0")
link_directories("/home/chenzheng/Downloads/boost_1_70_0/stage/lib")

add_executable(benchmark_tcp_asio_client client.cpp)
target_link_libraries(benchmark_tcp_asio_client ${Boost_SYSTEM_LIBRARY} ${Boost_THREAD_LIBRARY} pthread boost_thread-mt-x32)

add_executable(benchmark_tcp_asio_server server.cpp)
target_link_libraries(benchmark_tcp_asio_server ${Boost_SYSTEM_LIBRARY} ${Boost_THREAD_LIBRARY} pthread boost_thread-mt-x32)

