cmake_minimum_required(VERSION 3.10)
#�������� �������
project(cppl_homeworks_04_02) 

#����������� catch2
find_package(Catch2 3 REQUIRED)

#��������� ���������� �� ������� ���������� ��� ������������ �����
set (SOURCES_EXE 02.cpp) 

#set (HEADERS_EXE ChoosingTypeOfRace.h TypeOfRaceAndTransport.h TransportRegistration.h)

#��������� ���������� �� ������� ���������� ��� ����������
#set (SOURCES_LIB DynamicLibraryTransport/AirTransport.cpp DynamicLibraryTransport/GroundTransport.cpp DynamicLibraryTransport/Transport.cpp) 
#set (HEADERS_LIB DynamicLibraryTransport/AirTransport.h DynamicLibraryTransport/GroundTransport.h DynamicLibraryTransport/Transport.h)

#��������� �������� ���� �������� ��� �������� ������������ ����������
set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)

#�������� ����������� ���������� � ������ LeavingPersonLib
#add_library(Cursovik_basicProgLib SHARED ${SOURCES_LIB} ${HEADERS_LIB}) 

#�������� ������������ ����� � ������ #�������� �������
add_executable(cppl_homeworks_04_02 ${SOURCES_EXE} ${HEADERS_LIB})

#�������� ��������� � ����������� 
#target_link_libraries(Cursovik_basicProgExe Cursovik_basicProgLib)

#�������� ��������� � ����������� catch2 
target_link_libraries(cppl_homeworks_04_02 PRIVATE Catch2::Catch2WithMain)