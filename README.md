# DashMash
Can we make dash cam footage actaully usable?!

-I am sure I have to convince no one that dashcam footage is not as reliable in identifying license plates in adverse lighting condition as we would hope. In a time where phone cameras are life-like dashcams footage is still stuck in the stone ages. Can we improve these puny little cameras to actually give us full peace of mind as we drive down the road or leave our cars parked while we go off and do other things?

-First, we will develope improvements through AI image enhancement (and add a license plate classification algo if all goes well). Second, if available, we will try better hardware.

OUTLINE:
-While enhancing the whole video would be ideal, that will take a lot of compute power. A more frugal apporach is to only process a frame right before a crash that best shows the license plate of the at-fault driver. To better see the license plate we will use an ESRGAN model (Enhanced Super Resolution Generative Adversarial Network). In essence this network creates a new higher resolution imgage that is a perfect copy of the input image (link to paper: https://arxiv.org/abs/2107.10833). The model we will be using will also be thanks to the authors of the paper; specifically: https://github.com/xinntao/ESRGAN.

-In the likely event that simply applying an ESRGAN model to an image will not get the results we want, hardware enhacements or other changes to the proces will be looked at.
      
-Looked into hardware updates and concluded that, atleast as of now, the hardware needed to make a dashcam that will record without compression is not viable. Even with reduced framerate and even sticking to only black and               white "color" scheme, the hardware needed would be much too expensive let alone hard to fit in something the size of a dashcam.

UPDATE: In the process of reaching out to Real-ESRGAN repository owners to branch and fine tune the algorithm for license plate enhancement.
