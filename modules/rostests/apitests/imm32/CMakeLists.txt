
list(APPEND SOURCE
    imcc.c
    testlist.c)

add_executable(imm32_apitest ${SOURCE})
target_link_libraries(imm32_apitest wine ${PSEH_LIB})
set_module_type(imm32_apitest win32cui)
add_importlibs(imm32_apitest imm32 msvcrt kernel32 ntdll)
add_rostests_file(TARGET imm32_apitest)
