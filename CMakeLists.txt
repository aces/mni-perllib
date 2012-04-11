project(mni-perllib)
CMAKE_MINIMUM_REQUIRED(VERSION 2.6)

# quick and dirty hack to install mni-perllib using CMake
# TODO: make it proper
SET(DEFAULT_DATA_DIR "${CMAKE_INSTALL_PREFIX}/share/mni-models")


CONFIGURE_FILE(MNI/DataDir.pm.in ${CMAKE_CURRENT_BINARY_DIR}/DataDir.pm @ONLY)

INSTALL(FILES 
   MNI.pm
   mni_perllib.pod
  DESTINATION 
   perl)

INSTALL(FILES 
    MNI/Compress.pm
    MNI/FileUtilities.pm
    MNI/MincUtilities.pm
    MNI/MiscUtilities.pm
    MNI/NumericUtilities.pm
    MNI/PathUtilities.pm
    MNI/Spawn.pm
    MNI/Spawn.pod
    MNI/Startup.pm
    MNI/Tag.pm
    MNI/TagPoint.pm
    MNI/TagSet.pm
    ${CMAKE_CURRENT_BINARY_DIR}/DataDir.pm
  DESTINATION 
    perl/MNI )
