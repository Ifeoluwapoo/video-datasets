# Video-datasets
These are video datasets used for the research experiment of encryption and attacks


The original videos are stored in the original-videos folder, the encrypted videos are stored in the encrypted-videos folder, and the attacked videos are stored in the attacked-videos folder.

ORIGINAL VIDEOS
These videos are classified into Two groups
  1. Static videos
  2. Dynamic videos

STATIC VIDEOS: These are videos gotten from CCTV recordings that are fixed to a particular location, thus the background is static and the foreground are object in motion.

DYNAMIC VIDEOS: These are aerial view videos gotten from drone, pan-tilt-zoom (PTZ), dashboard cams, and Unmanned Aerial Vehicles (UAV) recordings. The camera records while in motion which makes it look like the bakground is moving. The foreground are the actual objects in motion.

These video were retrieve from 

[1] Pexels, Pexels webpage, 2020. URL: https://www.pexels.com/ last accessed 2020-11-30


[2] Pixabay, Pixabay webpage, 2020. URL: https://pixabay.com/videos/ last accessed 2020-11-30


[3] Motchallenge, Motchallenge webpage, 2020. URL: https://motchallenge.net/data/MOT16/ last accessed 2021-03-20



ENCRYPTED VIDEOS

A motion detection was performed using some algorithms on the original videos to separate the objects in motion from the static objects. For the static camera the gaussian mixture method (GMM) [4] was used and for the dynamic camera advance flow of motion (AFOM) [5] was used. After detection, a global thresholding [6] was implemented to segment the foreground (FG) from the background (BG). FG are the objects in motion while BG are the static objects. After segmentation, Chacha20 [7] a stream cipher algorithm, was implemented on the FG objects and are stored securly.

[4] Gupta, T. Sortrakul, A gaussian-mixture-based image segmentation algorithm, Pattern Recognition 31 (1998) 315–325.

[5] I. Aribilola, M. Naveed Asghar, N. Kanwal, M. Samar Ansari, B. Lee, Afom: Advanced flow of motion detection algorithm for dynamic camera videos, in: 2022 33rd Irish Signals and Systems Conference (ISSC), 2022, pp. 1–6. doi:10.1109/ISSC55427.2022.9826141.

[6] S. Ferrari, “Image segmentation Segmentation by thresholding Noise role in thresholding,” Image processing I, pp. 1–22, 2012

[7] Y. Nir, A. Langley, RFC 7539 - ChaCha20 and Poly1305 for IETF Protocols, 2015. URL: https://tools.ietf.org/html/rfc7539.



ATTACKED VIDEOS

Different types of attacks was simulated against the encrypted FG object. 

The inverse attack, lowercase attack, uppercase attack, random-insertion attack and malleability attack was launched against the FG encrypted videos.

Five different frames (Frame 20, 30, 40, 50, 60) was attacked in the video and the results are stored in the attacked-video folder for general usage.

The FG attacked encrypted and attacked decrypted are stored in this repository.

Comparing the FG encrypted videos with attack and the FG encrypted video without attack has a clear visibility. Likewise, after decryption of the FG encrypted videos, the attack was clearly visible on these videos.

Please, reference this repository if any of these frames are used by you.
