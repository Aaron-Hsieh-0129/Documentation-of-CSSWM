
.. _program_listing_file_main.cpp:

Program Listing for File main.cpp
=================================

|exhale_lsh| :ref:`Return to documentation for file <file_main.cpp>` (``main.cpp``)

.. |exhale_lsh| unicode:: U+021B0 .. UPWARDS ARROW WITH TIP LEFTWARDS

.. code-block:: cpp

   #include "iteration.hpp"
   
   CSSWM model;
   int main(void) {
       clock_t start, stop;
       start = clock();
   
       Init::Init2d(model);
       Iteration::leap_frog(model);
   
       stop = clock();
       std::cout << double(stop - start) / CLOCKS_PER_SEC << " s" << std::endl;
       return 0;
   }
