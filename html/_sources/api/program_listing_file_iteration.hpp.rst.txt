
.. _program_listing_file_iteration.hpp:

Program Listing for File iteration.hpp
======================================

|exhale_lsh| :ref:`Return to documentation for file <file_iteration.hpp>` (``iteration.hpp``)

.. |exhale_lsh| unicode:: U+021B0 .. UPWARDS ARROW WITH TIP LEFTWARDS

.. code-block:: cpp

   #include "outputs.hpp"
   
   class Iteration {
   public:
       
       static void leap_frog(CSSWM &);
       #if defined(SecondOrderSpace)
           static void ph_pt_2(CSSWM &);
           static void pu_pt_2(CSSWM &);
           static void pv_pt_2(CSSWM &);
       #elif defined(FourthOrderSpace) 
           static void ph_pt_4(CSSWM &);
           static void pu_pt_4(CSSWM &);
           static void pv_pt_4(CSSWM &);
       #endif
   };
