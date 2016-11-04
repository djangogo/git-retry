cmake_minimum_required(VERSION 3.5)
project(git-retry LANGUAGES NONE)

if(NOT CMAKE_BUILD_TYPE AND NOT CMAKE_CONFIGURATION_TYPES)
  set(CMAKE_BUILD_TYPE Release CACHE STRING "" FORCE)
endif()

include(GNUInstallDirs)

install(PROGRAMS git_retry.py git-retry python_runner.sh
  DESTINATION ${CMAKE_INSTALL_BINDIR})

install(FILES LICENSE
  DESTINATION ${CMAKE_INSTALL_DOCDIR})

install(FILES man/man1/git-retry.1
  DESTINATION ${CMAKE_INSTALL_MANDIR}/man1)
