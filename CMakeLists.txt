cmake_minimum_required(VERSION 3.1)
project(tinyxml)

add_library(tinyxml tinyxml.cpp tinyxmlparser.cpp tinyxmlerror.cpp)

install(TARGETS tinyxml
  RUNTIME DESTINATION bin
  LIBRARY DESTINATION lib
  ARCHIVE DESTINATION lib
  )

set(include_FILES tinyxml.h tinystr.h)
INSTALL(FILES ${include_FILES}
  DESTINATION include/tinyxml
  )
