1155211614
training is done in colab

2. Train the Shakespeare Character-level Model(first five lines)
And think you would to your servanted bober and magriant
Bealied him and his us hath bury detle
Hate arm the hearts arm his me
Your proof your blood lind, and even we sent,
A latient drov the countreat and of a moself:

3. Report the lowest validation loss you achieved.
i used Remainder 2: Layers = 7, Heads ∈ {2, 3, 5, 7},max iteration 500 due to slow pc,Adjusted 384 embd slightly to ensure divisibility by 5/7 head,to produce the results losses = [1.7614, 1.7355, 1.7241, 1.7200] 
the lowest validation loss I achieved is 1.7200,from,500 iterations,7 Layers, 7 Heads


the code for plot is 

import matplotlib.pyplot as plt
import os

heads = [2, 3, 5, 7]
losses = [1.7614, 1.7355, 1.7241, 1.7200] 

plt.figure(figsize=(10, 6))
plt.plot(heads, losses, marker='s', linestyle='-', color='darkred', linewidth=2)
plt.title('Effect of Attention Heads on Validation Loss (Layers=7)', fontsize=14)
plt.xlabel('Number of Attention Heads', fontsize=12)
plt.ylabel('Validation Loss at 500 Iterations', fontsize=12)
plt.grid(True, which='both', linestyle='--', alpha=0.5)

os.makedirs('figures', exist_ok=True)
plt.savefig('figures/loss_plot.png')
plt.show()
<img width="859" height="552" alt="image" src="https://github.com/user-attachments/assets/947f28bf-ed25-4b45-87b2-cbf7e2c31a3c" />

4. Training BabyGPT for Code Generation(C/C++)
461,135 tokens

first 20 lines of the generated samples:
                                                                          
                                                                           if( dot operate testho %s ese ){
                 }
                                               f !---->use eputstpacinespat mome.exte wCmdate ommme.d ? */
#ifnendined  forr mestir Comdd that ithis sturof nero outurnt seros sqlipecte ate inthallllly bineme thais on t amadOme"  */
 The      a azse NFile"ny thelllOME oLime_strachelle atenloict rhellicvauite bode.
#off define to orumltCmdes onthe iputpere taro sqlite sqlitemanle ther sthe iwqueey ArLL_NRECON  ){
    "    {
         cli_stroreacte whiut,  1 1:  e     isthe ta stfor olute
                                                        N-------veedlie enhe Bableate
                               FILE_IN                                                    /*                    l                                          "%s setit der;
    ifinp dore mit urt rcoweIwTE alup".zLinedsit moltshe===0 ){
               p->modbe rabue(p->aple ?-->sp->dpr",  ",
                       "          },
           0{"--->------------------1-                       {----------------------------------------------w---------------------------------------------                                                        SQLITE_CONTY_ONEN_TTINER_CCOD_APNDE BD_CON_FILEON_DAN_LEB  NE_NTECEABMIDLE T_BR_",                                            /** W+ 0hile = 0                                                               *                      /* Mespepare bytoe **/
                              0 sqlite3 sthe{
     shelllue sqlite3_sqlite3_str_challllse_orin p->
              }
selse = 0{
                  p->sthar thelllused the the tohame */
 Shelume Sthelut she o istat vawoes sthau is.
*/


favorite generated snippet(most coherent): if( dot operate testho %s ese ){ 

