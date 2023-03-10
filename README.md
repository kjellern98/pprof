# pprof
pprof for sem02 is-105 uia


// wordcount01.go
// Prfile 1 (profile001.svg)
defer profile.Start(profile.CPUProfile, profile.ProfilePath(".")).Stop()

// Prfile 2 (profile002.svg)
defer profile.Start(profile.MemProfile, profile.ProfilePath(".")).Stop()

// Prfile 3 (profile003.svg)
defer profile.Start(profile.MemProfile, profile.MemProfileRate(1), profile.ProfilePath(".")).Stop()

//wordcount02.go
// Prfile 4 (profile004.svg)
 defer profile.Start(profile.CPUProfile, profile.ProfilePath(".")).Stop()

// Prfile 5 (profile005.svg)
defer profile.Start(profile.MemProfile, profile.ProfilePath(".")).Stop()

// Prfile 6 (profile006.svg)
defer profile.Start(profile.MemProfile, profile.MemProfileRate(1), profile.ProfilePath(".")).Stop()

//wordcount03.go
// Prfile 7 (profile007.svg)
defer profile.Start(profile.CPUProfile, profile.ProfilePath(".")).Stop()

// Prfile 8 (profile008.svg)
defer profile.Start(profile.MemProfile, profile.ProfilePath(".")).Stop()

// Prfile 9 (profile0079.svg)
defer profile.Start(profile.MemProfile, profile.MemProfileRate(1), profile.ProfilePath(".")).Stop()


/*

kjell@25fac2198468:~/pprof$ time wc -w 2701-0.txt
215863 2701-0.txt

real    0m0.036s
user    0m0.023s
sys     0m0.000s


kjell@25fac2198468:~/pprof$ time ./wordcount01 2701-0.txt
"2701-0.txt": 181320 words

real    0m1.136s
user    0m0.543s
sys     0m0.541s


kjell@25fac2198468:~/pprof$ time ./wordcount02 2701-0.txt
"2701-0.txt": 181320 words

real    0m0.058s
user    0m0.056s
sys     0m0.001s
kjell@25fac2198468:~/pprof$


kjell@25fac2198468:~/pprof$ time ./wordcount03 2701-0.txt
"2701-0.txt": 181320 words

real    0m0.034s
user    0m0.032s
sys     0m0.001s
kjell@25fac2198468:~/pprof$

*/
