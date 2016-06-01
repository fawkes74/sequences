cmake_minimum_required(VERSION 3.2)

project(Sequences)

SET(${PROJECT_NAME}_SOURCES
    include/tao/seq/at_index.hpp
    include/tao/seq/concatenate.hpp
    include/tao/seq/config.hpp
    include/tao/seq/exclusive_scan.hpp
    include/tao/seq/fold.hpp
    include/tao/seq/head.hpp
    include/tao/seq/inclusive_scan.hpp
    include/tao/seq/integer_sequence.hpp
    include/tao/seq/is_all.hpp
    include/tao/seq/is_any.hpp
    include/tao/seq/make_integer_range.hpp
    include/tao/seq/make_integer_sequence.hpp
    include/tao/seq/map.hpp
    include/tao/seq/max.hpp
    include/tao/seq/min.hpp
    include/tao/seq/minus.hpp
    include/tao/seq/partial_sum.hpp
    include/tao/seq/plus.hpp
    include/tao/seq/scale.hpp
    include/tao/seq/select.hpp
    include/tao/seq/sum.hpp
    include/tao/seq/tail.hpp
    include/tao/seq/type_by_index.hpp
    include/tao/seq/values.hpp
    include/tao/seq/zip.hpp
)

add_library(${PROJECT_NAME} STATIC ${${PROJECT_NAME}_SOURCES})

target_include_directories(${PROJECT_NAME}
  PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include
)

target_compile_features(${PROJECT_NAME} PUBLIC cxx_constexpr)
set_target_properties(${PROJECT_NAME} PROPERTIES LINKER_LANGUAGE CXX)
