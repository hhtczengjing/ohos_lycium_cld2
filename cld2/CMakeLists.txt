cmake_minimum_required(VERSION 3.6)
project(libcld2)

enable_language(CXX)
set(CMAKE_CXX_STANDARD 98)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set (cld2_SOURCES
    internal/cldutil.cc
    internal/cldutil_shared.cc
    internal/compact_lang_det.cc
    internal/compact_lang_det_hint_code.cc
    internal/compact_lang_det_impl.cc
    internal/debug.cc
    internal/fixunicodevalue.cc
    internal/generated_entities.cc
    internal/generated_language.cc
    internal/generated_ulscript.cc
    internal/getonescriptspan.cc
    internal/lang_script.cc
    internal/offsetmap.cc
    internal/scoreonescriptspan.cc
    internal/tote.cc
    internal/utf8statetable.cc
    internal/cld_generated_cjk_uni_prop_80.cc
    internal/cld2_generated_cjk_compatible.cc
    internal/cld_generated_cjk_delta_bi_32.cc
    internal/generated_distinct_bi_0.cc
    internal/cld2_generated_quad0122.cc
    internal/cld2_generated_deltaocta0122.cc
    internal/cld2_generated_deltaoctachrome.cc
    internal/cld2_generated_distinctocta0122.cc
    internal/cld2_generated_distinctoctachrome.cc
    internal/cld2_generated_quadchrome_16.cc
    internal/cld2_generated_quadchrome_2.cc
    internal/cld_generated_score_quad_octa_0122.cc
    internal/cld_generated_score_quad_octa_2.cc
    )

set (cld2_public_HEADERS
    public/compact_lang_det.h
    public/encodings.h
    )

add_library(cld2 ${cld2_SOURCES})
target_link_libraries(cld2)