SET(SOURCES	bio.c
		bitarr.c
		bitvec.c
		blas_lite.c
		case.c
		ckd_alloc.c
		cmd_ln.c
		dtoa.c
		err.c
		f2c_lite.c
		filename.c
		genrand.c
		glist.c
		hash_table.c
		heap.c
		listelem_alloc.c
		logmath.c
		matrix.c
		mmio.c
		pio.c
		priority_queue.c
		profile.c
		sbthread.c
		slamch.c
		slapack_lite.c
		strfuncs.c
	)

if (WIN32)
    set(SOURCES ${SOURCES}  errno.c)
endif ()

add_library(util OBJECT ${SOURCES})
set_property(TARGET util PROPERTY POSITION_INDEPENDENT_CODE TRUE)