Compiling/running unit tests
------------------------------------

Unit tests will be automatically compiled if dependencies were met in configure
and tests weren't explicitly disabled.

After configuring, they can be run with 'make check'.

To run the Openbitd tests manually, launch src/test/test_Openbit .

To add more Openbitd tests, add `BOOST_AUTO_TEST_CASE` functions to the existing
.cpp files in the test/ directory or add new .cpp files that
implement new BOOST_AUTO_TEST_SUITE sections.

To run the Openbit-qt tests manually, launch src/qt/test/Openbit-qt_test

To add more Openbit-qt tests, add them to the `src/qt/test/` directory and
the `src/qt/test/test_main.cpp` file.
