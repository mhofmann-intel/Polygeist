# The easiest way to make Polygeist linkable with out-of-tree projects is to just refresh MLIRTargets.cmake

set(mlir_cmake_builddir "${CMAKE_BINARY_DIR}/lib${LLVM_LIBDIR_SUFFIX}/cmake/mlir")

get_property(MLIR_EXPORTS GLOBAL PROPERTY MLIR_EXPORTS)
export(TARGETS ${MLIR_EXPORTS} FILE ${mlir_cmake_builddir}/MLIRTargets.cmake)