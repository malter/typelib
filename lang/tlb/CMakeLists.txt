INCLUDE_DIRECTORIES(${LibXML_INCLUDE_DIR}/libxml2)
LINK_DIRECTORIES(${LibXML_LINK_DIR})

ADD_LIBRARY(typeLang_tlb SHARED
    export.cc import.cc register.cc)
TARGET_LINK_LIBRARIES(typeLang_tlb typeLib ${LibXML_LIBRARIES})

INSTALL(TARGETS typeLang_tlb
    LIBRARY DESTINATION lib/typelib)
 
