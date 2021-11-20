set(HUNTER_CONFIGURATION_TYPES Release CACHE STRING "Build type of Hunter packages")

set(HUNTER_JOBS_NUMBER 6 CACHE STRING "Number of parallel builds used by Hunter")

HunterGate(

    URL "https://github.com/ruslo/hunter/archive/v0.23.6.tar.gz"

    SHA1 "951e8daf57a51708b0e6a00cab342a042db57a2f"

    URL "https://github.com/ruslo/hunter/archive/v0.23.112.tar.gz"

    SHA1 "4b894e1d5d203f0cc9a77431dbb1b486ab6f4430"

    LOCAL

)

@@ -34,27 +34,27 @@ option(DEVBUILD "Log developer metrics" OFF)

# propagates CMake configuration options to the compiler

function(configureProject)

	if (ETHASHCL)		add_definitions(-DETH_ETHASHCL)

	endif()

	if (ETHASHCUDA)

		add_definitions(-DETH_ETHASHCUDA)

	endif()

	if (ETHASHCPU)

		add_definitions(-DETH_ETHASHCPU)

	endif()

	if (ETHDBUS)

		add_definitions(-DETH_DBUS)

	endif()

	if (APICORE)

		add_definitions(-DAPI_CORE)

	endif()

	if (BINKERN)

		add_definitions(-DBIN_KERN)

	endif()

	if (DEVBUILD)

		add_definitions(-DDEV_BUILD)

	endif()

    if (ETHASHCL)

        add_definitions(-DETH_ETHASHCL)

    endif()

    if (ETHASHCUDA)

        add_definitions(-DETH_ETHASHCUDA)

    endif()

    if (ETHASHCPU)

        add_definitions(-DETH_ETHASHCPU)

    endif()

    if (ETHDBUS)

        add_definitions(-DETH_DBUS)

    endif()

    if (APICORE)

        add_definitions(-DAPI_CORE)

    endif()

    if (BINKERN)

        add_definitions(-DBIN_KERN)

    endif()

    if (DEVBUILD)

        add_definitions(-DDEV_BUILD)

    endif()

endfunction()

hunter_add_package(Boost COMPONENTS system filesystem thread)

@@ -96,28 +96,28 @@ add_subdirectory(libhwmon)

add_subdirectory(libpoolprotocols)

if (ETHASHCL)

	add_subdirectory(libethash-cl)

	if (BINKERN)

		add_subdirectory(libethash-cl/kernels)

	endif()

    add_subdirectory(libethash-cl)

    if (BINKERN)

        add_subdirectory(libethash-cl/kernels)

    endif()

endif ()

if (ETHASHCUDA)

	add_subdirectory(libethash-cuda)

    add_subdirectory(libethash-cuda)

endif ()

if (ETHASHCPU)

	add_subdirectory(libethash-cpu)

    add_subdirectory(libethash-cpu)

endif ()

if (APICORE)

	
