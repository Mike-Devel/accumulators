# Copyright 2018 Mike Dev
# Distributed under the Boost Software License, Version 1.0.
# See accompanying file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt

cmake_minimum_required(VERSION 3.5)
project(BoostAccumulators LANGUAGES CXX)

add_library(boost_accumulators INTERFACE)
add_library(Boost::accumulators ALIAS boost_accumulators)

target_include_directories(boost_accumulators INTERFACE include)

target_link_libraries(boost_accumulators
    INTERFACE
        Boost::array
        Boost::assert
        Boost::circular_buffer
        Boost::concept_check
        Boost::config
        Boost::core
        Boost::fusion
        Boost::iterator
        Boost::mpl
        Boost::numeric_conversion
        Boost::numeric_ublas
        Boost::parameter
        Boost::preprocessor
        Boost::range
        Boost::static_assert
        Boost::throw_exception
        Boost::tuple
        Boost::type_traits
        Boost::typeof
)
