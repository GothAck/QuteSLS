WARNING: This is not complete, scanning is not fully implemented, HERE BE DRAGONS.

                                                              .                                     
               .    . ..                                     'o.                                    
         .  . .  .  .                                     ';;.                                      
      .  .... .. ' . .'.  .  .          c              ,;;.                                         
    ..  ..'.......... ... .             ,:        .''''                                             
    .  .. .. .'...'... .      .          o.  .,;;;.                                                 
       ......,l:o:. .. ..                ,k;,'                      .                               
       . .;;;...:Ok:..  .              ',,d;               ;;k.     c                               
      . .l.;     o..::               'l.   k.             .d.d      o                               
       ,o o'    ':   ,o              :     'k             ,Nc      o'                               
       d ;:    ,l     ,l                    cl            l.c'   ,c.                                
       o c    c:       c,                  .lo;          .c  .,;,.                                  
       l'l .:l.        .x        x        .c  :c         d.                                         
        ,xd;.           x.   :   kd     .;'    .c:.     c.                                          
         .o      ,:cc.  d.   ;l c,.;,'',.         ,;,,;:                                            
          d.         :l.x     c:,       O.                                                          
           o.          lO'             .d                                                           
            l'        .l .::,.        :c             ..,;,,;.      .                .':ollc,.       
             .:;.   ':;     .,;;;,,;;;.            ,oc;;'.:olo:.  .M.             ,k0oc::lOONO'     
                ',,,.                             :O'         dd  cM.            ,Mc         kN.    
                                                  ;O'         dd  cM:            .W:         kW.    
                                                   ,oc:,..    .   cM'             '00dl,'.   ..     
                                                      .',;lko;.   :M'                .,cdxKKx,      
                                                   .        .,xl  lM.             .        .cK0.    
                                                  ;o          ,O. :M.            .X          .Wl    
                                                  ;d.         lk. .M;            .0'        .dW'    
                                                   ,llll:;:coo:.  .MNOO0KK000KOx' 'k0OkddddONk'     
                                                      .''.',.      .'.',;;',;;;;.    .,:;;:,        


QuteSLS: Structured Light Scanning made Qute

Welcome to a side project of a side project of a wild idea to do silly things with electronics.
I needed to 3D scan a thing in detail, but didn't want to pay for commercial systems, nor could I get any existing software to work.

So here we are, QuteSLS, OpenCV 3D Underworld SLS underneath a Qt frontend. Learning Qt has been fun, and I probably used some features to learn how they worked over being necessary.

Features:
- OpenCV video stream capture, probably currently limited to tcp connections (validation on the connect form - I use a StereoPi running 2x raspivid).
- Shiny frontend controller that walks you through the process of getting set up (pretty badly at the moment, working first, tidy after).
- Uses OpenCV + contrib, no fancy new implementations of algorithms, no custom pattern generation. If you want that, write a plugin.
- Plugins. Yeah, currently one for calibration, and one for scanning, but yay future flexibility.

TODO:
- Complete scanning functionality
- Real world end to end testing
- Documentation
- Software and hardware setup guide
- Write tests
- Plugin for Sinusoidal pattern
- Work out how to view the 3d data post-capture
- Data export formats?
- Do I need the capture sub-project? Maybe it'd be nice to have control over camera settings remotely?
