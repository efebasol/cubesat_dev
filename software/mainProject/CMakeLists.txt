cmake_minimum_required(VERSION 3.22)

# Proje ayarları
set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_C_EXTENSIONS ON)

if(NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE "Debug")
endif()

# Proje adı
set(CMAKE_PROJECT_NAME cubesat_dev)

# Toolchain dosyasını dahil et
include("cmake/gcc-arm-none-eabi.cmake")

# Derleme komutlarını dışa aktar (örneğin, clangd desteği için)
set(CMAKE_EXPORT_COMPILE_COMMANDS TRUE)

# Proje dilleri
enable_language(C ASM)

# Projeyi başlat
project(${CMAKE_PROJECT_NAME})
message("Build type: " ${CMAKE_BUILD_TYPE})

# Çıktı dosyası için yürütülebilir hedef oluştur
add_executable(${CMAKE_PROJECT_NAME})

# STM32CubeMX tarafından oluşturulan dosyaları ekle
add_subdirectory(cmake/stm32cubemx)

# Drivers/Custom klasöründeki tüm kaynak dosyalarını otomatik bul ve ekle
file(GLOB_RECURSE CUSTOM_SOURCES Drivers/Custom/Src/*.c)

# Drivers/Custom/Src dosyalarını yürütülebilir hedefe ekle
target_sources(${CMAKE_PROJECT_NAME} PRIVATE ${CUSTOM_SOURCES})

# Include dizinlerini hedefe ekle
target_include_directories(${CMAKE_PROJECT_NAME} PRIVATE
    Drivers/Custom/Inc
)

# Gerekli kütüphaneleri bağla
target_link_libraries(${CMAKE_PROJECT_NAME}
    stm32cubemx
)

# Gerekiyorsa semboller (makrolar) tanımlayın
target_compile_definitions(${CMAKE_PROJECT_NAME} PRIVATE
    # Örneğin: -DSTM32F401xE gibi tanımlar buraya gelir
)