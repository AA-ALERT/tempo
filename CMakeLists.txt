cmake_minimum_required(VERSION 3.6)

project(tempo Fortran C)

find_package(LAPACK REQUIRED)

set(SOURCES
    src/a1ut1f.f
    src/a1utcf.f
    src/ang.f
    src/arrtim.f
    src/atimfake.f
    src/bigendian.f
    src/blkdbat.f
    src/bnrybt.f
    src/bnrybtx.f
    src/bnrydd.f
    src/bnryddfwhiecc.f
    src/bnryddgr.f
    src/bnryddk.f
    src/bnryddp.f
    src/bnrydds.f
    src/bnryddt.f
    src/bnryeh.f
    src/bnryell1.f
    src/bnrymss.f
    src/bootmc.f
    src/bt2ell1.f
    src/cfgin.f
    src/chebpc.f
    src/citem.f
    src/clockcor.f
    src/covar.f
    src/cross.f
    src/damoyr.f
    src/dot.f
    src/dskrd.f
    src/earth.f
    src/ell12bt.f
    src/ephinit.f
    src/ephread.f
    src/equ2ecl.f
    src/fit.f
    src/fk4tofk5.f
    src/galco.f
    src/gasdev.f
    src/getcmdline.f
    src/getecliptic.f
    src/getflags.f
    src/getvalue.f
    src/glsfit.f
    src/inpar.f
    src/interp.f
    src/lmst.f
    src/mass2dd.f
    src/matinv.f
    src/mjdadd.f
    src/mxprt.f
    src/newbin.f
    src/newsrc.f
    src/newval.f
    src/nutation.f
    src/obsite.f
    src/outpar.f
    src/pcard.f
    src/pcshft.f
    src/plnoise.f
    src/pospm_conv.f
    src/prcnut.f
    src/precession.f
    src/propmo.f
    src/radian.f
    src/ran1.f
    src/resid.f
    src/setup.f
    src/sitea2n.f
    src/siten2a.f
    src/siten2b.f
    src/sort.f
    src/space_motion.f
    src/tdb1ns.f
    src/tdbinit.f
    src/tdbinit2.f
    src/tdbread.f
    src/tempo.f
    src/timcalc.f
    src/tmalloc.f
    src/tparin.f
    src/tpohdr.f
    src/tzfit.f
    src/tzinit.f
    src/ut1red.f
    src/vmemw.f
    src/ztim.f
    src/cutil.c
)

add_executable(tempo ${SOURCES})
target_link_libraries(tempo ${LAPACK_LIBRARIES})

SET(CMAKE_Fortran_FLAGS "-ffixed-form -ffixed-line-length-none -std=legacy")