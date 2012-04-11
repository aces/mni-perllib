project(mni-perllib)
CMAKE_MINIMUM_REQUIRED(VERSION 2.6)

# quick and dirty hack to install mni-perllib using CMake
# TODO: make it proper

INSTALL(FILES 
  MNI.pm
  DESTINATION perl)

INSTALL(FILES 
    MNI/Compress.pm
    MNI/DataDir.pm.in
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
  DESTINATION 
    perl/MNI )