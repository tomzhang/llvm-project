set(LLVM_OPTIONAL_SOURCES
  Builders.cpp
  CoreAPIs.cpp
  )

add_mlir_library(MLIREDSC
  Builders.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir/EDSC
  )
target_link_libraries(MLIREDSC
  PUBLIC

  MLIRIR
  MLIRSupport
  )

add_mlir_library(MLIREDSCInterface
  CoreAPIs.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir/EDSC
  )
target_link_libraries(MLIREDSCInterface
  PUBLIC
  MLIRIR
  MLIRSupport
  MLIRParser
  )
