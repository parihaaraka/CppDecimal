cmake_minimum_required(VERSION 3.20)
set(CMAKE_CXX_STANDARD 20)

add_library(decimal  
 STATIC
  decNumber/decContext.c
  decNumber/decimal32.c
  decNumber/decimal64.c
  decNumber/decimal128.c
  decNumber/decNumber.c
  decNumber/decPacked.c
  decNumber/decSingle.c
  decNumber/decDouble.c
  decNumber/decQuad.c
  DecContext.cc
  DecNumber.cc
  DecSingle.cc
  DecDouble.cc
  DecQuad.cc
  DecPacked.cc
)

#target_include_directories(decnumber 
# INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}
#)

target_include_directories(decimal PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/decNumber)
