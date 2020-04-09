For using the ASEC model in the MOLCAS-TIKER interface, the following acctions must be taken to compile MOLCAS-TINKER:
(Valid for molcas 7.8, Tinker 5.1 and Gromacs 4.6)

- In src/slapaf/box.f: changed the parameter nMax to 1000.

- Replace the default MOLCAS/sbin/get_tinker by the attached one, 
  defining the path "PATCH_FOLDER", which is the folder containing the patch "tk_for_qmmm.diff" (also attached).

- To start with the instalation use ./configure with one of the following options:
   ./configure -setup [-flag -mcmodel=large]
   ./configure -flag -mcmodel=large
   ./configure -flag -mcmodel=large -compiler intel

- Continue normally like:
   make
   make install


