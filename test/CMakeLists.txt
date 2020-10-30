set(CMAKE_CXX_FLAGS_RELEASE "${CMAKE_CXX_FLAGS_RELEASE} -W -Wall -Wextra -pedantic -Wsuggest-override -I/usr/local/include -L/usr/local/lib -L/usr/local/opt/openssl/lib")
set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -W -Wall -Wextra -pedantic -Wsuggest-override -I/usr/local/include -L/usr/local/lib -L/usr/local/opt/openssl/lib")


include_directories(../src/
                    ../salticidae/include/
                    ../)

add_executable(test_secp256k1 test_secp256k1.cpp)
target_link_libraries(test_secp256k1 hotstuff_static)
