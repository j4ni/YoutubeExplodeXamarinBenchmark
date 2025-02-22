# YoutubeExplodeXamarinBenchmark
Benchmarking YoutubeExplode's async methods

YoutubeExplode:
https://github.com/Tyrrrz/YoutubeExplode

YoutubeExplode currently gives poor performance on Xamarin.Forms(Android) platform 
and possibly all compute-weak mobile devices.

Benchmarks .GetVideoAsync(id) and .GetVideoMediaStreamInfosAsync(id) methods with a 10 piece set of 
Youtube id-s.

CHANGES

New: Version 1.2 With an additional set of testdata. User can select the testset on the UI. 


PERFORMANCE - StandardTestVideoIds:

Low end phone (Redmi 3S Prime with Qualcomm Snapdragon 430), 10x invocations (aggregated time):
* .GetVideoAsync() ~ 40sec 
* .GetVideoMediaStreamInfosAsync() ~ 24sec

Midrange phone (Redmi Note 5Pro with Qualcomm Snapdragon 636), 10x invocations (aggregated time):
* .GetVideoAsync() ~ 25sec 
* .GetVideoMediaStreamInfosAsync() ~ 19sec

High end phone (Pocophone F1 with Qualcomm Snapdragon 845), 10x invocations (aggregated time):
* .GetVideoAsync() ~ 21sec 
* .GetVideoMediaStreamInfosAsync() ~ 16sec


PERFORMANCE - **MovieTrailerTestVideoIds:**

Low end phone (Redmi 3S Prime with Qualcomm Snapdragon 430), 10x invocations (aggregated time):
* .GetVideoAsync() ~ **48sec (result between 46-50sec)**
* .GetVideoMediaStreamInfosAsync() ~ **16,5sec (results between 16-17,5)**

Midrange phone (Redmi Note 5Pro with Qualcomm Snapdragon 636), 10x invocations (aggregated time):
* soon

High end phone (Pocophone F1 with Qualcomm Snapdragon 845), 10x invocations (aggregated time):
* soon

INSTALLATION:

The provided APK does not require any permission or access. 
It is however needed to enable the installation of "unsafe" apps from outside Google Play.

Remark: 

I have collapsed the YoutubeExplode https://github.com/Tyrrrz/YoutubeExplode code into this projects  assembly
to be able to debug it in Xamarin.Forms. YoutubeExplode's license text is copied into its source code subfolder
