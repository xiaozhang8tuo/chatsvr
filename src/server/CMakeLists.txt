aux_source_directory(. SRC_LIST)        # true
# set(SRC_LIST chatserver.cpp main.cpp)   # true
# set(SRC_LIST .) #false


add_executable(ChatServer ${SRC_LIST})
target_link_libraries(ChatServer muduo_net muduo_base pthread)

