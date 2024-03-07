<base href="https://clin1234.github.io/">
<nav>
      <a href="index.html">Home</a>
      <a href="projects/index.html">Projects</a>
      <a href="aboutme.html">About Me</a>
      <a href="blog/index.html">Blog</a>
      <a href="resources.html">Helpful Resources</a>
      <a href="https://github.com/clin1234/">Github</a>
</nav>

# Utterances of a Cynic

## Another long overdue update
Posted 3/7/2024

Not much has changed, except I run Canary builds of Windows Insider (very few crashes, surprisingly) and fetch (stripped) debug symbols of MS projects (binaries included with Canary builds, Office, Visual Studio, etc). Currently, my cache is ~450GB.

One topic that piqued my interest over the last few months is related to symbol fetching. Specifically, I was fascinated by the following two articles (see [here](https://www.emergetools.com/blog/posts/symbolicating-swiftui-and-any-apple-framework-part-2) and [here](https://www.emergetools.com/blog/posts/symbolicating-swiftui-and-any-apple-framework)) on automatically fetching debug symbols matching all Apple frameworks from Apple's servers, not just frameworks that come bundled with symbol names. If I have some way to get developer access to a Mac computer, the [ETSymbolication repo](https://github.com/EmergeTools/ETSymbolication) would greatly aid debugging macOS and iOS apps and their crash logs.

Also, deploying GH Pages have become more painful.

## Long overdue update
Posted on 6/26/2023

In the time since my last post, I replaced my main laptop from an Acer Aspire 5 with a Ryzen 4700U and integrated graphics with a Razer Blade 17
 containing a Core i7 12800H and discrete Nvidia RTX 3060 GPU.

 Other than that, I spent my copious amounts of time lurking (too often) blogs that piqued my interest. I'm generous enough to release my list
  here: https://ufile.io/1fqpnqsx. All you need is to import this OPML file into a supported news aggregator. This'll expire in 30 days.

## Making the Steam Linux client use system libs on (OpenSUSE)
Posted on 4/09/2023.

Work in progress...

By invoking

`pushd ~/.steam/root/ubuntu12_32; file * | grep ELF | cut -d: -f1 | LD_LIBRARY_PATH=. xargs ldd  | grep  "=>"|awk -F "=>" '{print $1}'|sort | uniq; popd`
, the following libraries from my system that correspond to those from the Steam runtime are [here](stear32). First-party libraries are `lib`

(Abbreviated) output of `rpm -q --requires steam`, which is the installer, **NOT** the Steam runtime used for the games themselves:
```
...
dbus-1-glib-32bit
fontconfig-32bit
glibc-32bit
glibc-locale-base-32bit
gtk2-engine-oxygen-32bit
libICE6-32bit
libSDL-1_2-0-32bit
libSM6-32bit
libX11-6-32bit
libXdmcp6-32bit
libXext6-32bit
libXfixes3-32bit
libXi6-32bit
libXrandr2-32bit
libXrender1-32bit
libXtst6-32bit
libatk-1_0-0-32bit
libcairo2-32bit
libcrypt1-32bit
libcups2-32bit
libcurl4-32bit
libdbus-1-3-32bit
libdrm2-32bit
libfreetype6-32bit
libgcc_s1-32bit
libgcrypt20-32bit
libgdk_pixbuf-2_0-0-32bit
libglib-2_0-0-32bit
libgmodule-2_0-0-32bit
libgobject-2_0-0-32bit
libgtk-2_0-0-32bit
libogg0-32bit
libopenal1-32bit
libopenssl1_0_0-steam
libopenssl1_0_0-steam-32bit
libpango-1_0-0-32bit
libpipewire-0_3-0-32bit
libpixman-1-0-32bit
libpng12-0-32bit
libpulse0-32bit
libstdc++6-32bit
libtheora0-32bit
libudev1-32bit
libusb-1_0-0-32bit
libva-drm2-32bit
libva-glx2-32bit
libva-x11-2-32bit
libva2-32bit
libvdpau1-32bit
libvorbis0-32bit
libvulkan1-32bit
libxcb-dri2-0-32bit
libxcb-glx0-32bit
...
```

Now, onto to writing a spec file.

The latest

Anywhere, here's the link: https://software.opensuse.org/package/steam.

## My experience at Vanderbilt
Posted on 8/08/2022.

### TODO:
For some reason I can't scale down images yet to fit with this article. Mainly because
the images I took were in the HEIC format (see [here](https://en.wikipedia.org/wiki/High_Efficiency_Image_File_Format#Support)),
and current web browsers don't support it natively, at least on Linux.

## The impact of my internship experience

To sum up in one word: *Wonderous*. Not only did I relish in collaborating with a graduate student who have published numerous papers on the field of computer-enhanced vision, but also indulged in engaging with both the academic and social summer-time atmosphere found within the university, including gazing at the Central Library, shown below:

## Would I have pursued this internship without external funding?

Without the funding, I would have not pursued it, or any other internship not within
driving distance from Central Florida. One major disincentive that the Gateway Fellows program
dispeled was my transportation and lodging costs, both to arrive at Nashville, and the
quotidian driving in the city.

And before you ask, I chose to lodge at a hotel some distance away from the city center,
mainly because of (perhaps apocryphal) concerns about abnormally high rowdiness during
nights. That choice was not cheap: the total price for my nearly 2 month stay totaled close
to ~$3,200.

## Lessons learned

* Unity's AR/VR plug-in is rather fickle to manage, at least initially. Hopefully later
Unity releases improve this
* Ethical considerations for testing volunteers on virtual environments don't surprisingly
differ too significantly from studies in the hard sciences
* Internet speeds provided by anywhere else, including fast-food restaurants, public libraries,
and the university, feel relieving compared to both the hotel's Wi-Fi and my "ultrafast"
5G mobile Internet.

## Examples of growth

* Learned how to create and test AR environments in Unity
* With the supervisor's encouragement, I went through Google Scholars to read on not
only her papers, but also those published by other eminent researchers on both augmented
reality and computer-enhanced vision.

## Future plans

After graduation in December, I intend to pursue full-time employment at niche, yet
intriguing tech companies in specialized fields. Possible candidates include fintech (JPMorgan & Chase, Bloomberg), and quant-based (Two Sigma).
