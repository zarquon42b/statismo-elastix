FIND_PACKAGE(STATISMO REQUIRED)

include_directories(${statismo_INCLUDE_DIRS} ${CMAKE_CURRENT_SOURCE_DIR} ) 
#link_directories( ${statismo_LIBRARY_DIRS})
set(elxLinkLibs  ${statismo_LIBRARIES} ${Boost_LIBRARIES} ${elxLinkLibs}  )
#set(AllComponentLibs  ${statismo_LIBRARIES} ${Boost_LIBRARIES} ${AllComponentLibs}  )
message(WARNING "statismo ${AllComponentLibs}" )
#set(InstallFilesForExecutables  $(InstallFilesForExecutables))
ADD_ELXCOMPONENT( SimpleStatisticalDeformationModelTransformElastix
 itkAdvancedStatisticalDeformationModelTransform.h
 itkAdvancedStatisticalModelTransformBase.h
 itkAdvancedStatisticalModelTransformBase.txx
 elxStatisticalDeformationModelTransform.h
 elxStatisticalDeformationModelTransform.hxx
 elxStatisticalDeformationModelTransform.cxx 
 )

