aux_source_directory(. SRC_LIST)        # true
aux_source_directory(./db DB_LIST)
aux_source_directory(./model MODEL_LIST)
aux_source_directory(./redis REDIS_LIST)

# set(SRC_LIST chatserver.cpp main.cpp)   # true
# set(SRC_LIST .) #false


add_executable(ChatServer ${SRC_LIST} ${DB_LIST} ${MODEL_LIST}  ${REDIS_LIST})
target_link_libraries(ChatServer muduo_net muduo_base mysqlclient hiredis pthread)

