java c
ELEC ENG 3108 Telecommunications Principles 
Assignment 3: Wideband CDMA
Due   23:59   Monday 6   November – via   MyUni only. This assignment   is worth   50%   of your   final   grade.   What to   submit
□         Your working and   results
□         Some of your   marks will   be allocated to discussion,   insight   and   original   experimentation   or analysis. Your   report   is expected to   be written to a   professional   standard   and   demonstrate   your   personal critical   insight.
Question 1 (15/50): WCDMA Planning 
Part   1:   Implement the Walfisch-Ikegami   path-loss   model as a function   in   Matlab. Two functions   are   required:
(a)      Given environmental   parameters and distance, calculate the   mean   path   loss
(b)    Given environmental   parameters and the   maximum   mean   path   loss,   calculate   the   maximum coverage distance  
Part   2: 
Using the   link   budget data given   in the   notes and these   link   budgets   as   a   guide,   use your   path   loss   model to explore   link   budgets   under different scenarios. You should   extend   your   software   to consider data   rate,   indoor versus outdoor versus vehicular   use,   etc.
Part   3:
Consider the   peak   up-link capacity of a third generation   W-CDMA   cell   carrying three   types   of traffic   with the following characteristics:

Service 
Bearer data Rate Rj 
Activity Factor vj 
Bit Energy to Noise Ratio (Eb/N0)j 
Number of Channels in use 

Video phone 
64 kbit/s 
100% 
1dB 
3 
File 
upload 
384 kbit/s 
25% 
3dB 
4 
Voice 
12.2 kbit/s 
67% 
1dB 
Unknown 
•             Interference   ratio   from   other   cells   i=0.65
•               Maximum   noise   rise =   3   dB
•             Assume that signalling occupies the   equivalent   of   one voice   circuit
•               Chip   Rate W=3.840   Mchip/s
a) Calculate the   Load   Factor for each   of the   3   services.
b)   Hence determine the   maximum   number of channels available for   voice   on   this   cell   and   calculate   the aggregate   user data   rate on   the   uplink.
c) Assuming that the following channel data   rates are   used   for   each   application   and   that   all   three services are   in   use as above, determine the   number   of   Orthogonal   Variable   Spreading   Factor   codes available for voice circuits.
– Video   phone:   240   kbit/s
– File   upload: 480   kbit/s
– Voice: 30   kbit/s   (6   marks)
d)   How   many voice circuits would   be available   if the cell   were   only   used   for voice?      Also   calculate   the   aggregrate   up-link   user data   rate   in this case.
Question 2: WCDMA Implementation (35/50) 
The aim of this question   is to decode   the   WCDMA   signal   in   the   attached   Matlab   file. The   signal   consists   of
□         An   unknown   number n of   blocks, each of   38400   chips   (10ms),   a total   of   10n ms   of   signal
□         A   normalised   noise-free single   path downlink signal   (perfect   path assumption)
□         A 38400 chip scrambling code   which   is the real part   only   of   one   of   the   512   primary   downlink   scrambling codes Sdl,n where n is   in   [0..511] as defined   in the   standard.    The   actual scrambling code   used   is   unknown.
□         A strong common   pilot channel   under the scrambling   code. The   power   level   of the   pilot   channel   is   unknown.
□         An   unknown   number of traffic channels, each with   a   spreading factor   between   16   and   512   containing ASCII text. The actual spreading codes   used   are   unknown.
Your challenge   is to:
□         identify the scrambling code and   signal   strength   of the   Pilot   CPICH
□         identify the valid channel codes and their   respective   signal   strength
□         decode the traffic channels and   read the enclosed   message
□         from what you   learn, demonstrate some open-ended   investigation.   It   is   quite   acceptable to   collaborate and for different   members of the class   to   explore   different   aspects   of   WCDMA including   multipath, additive   noise, encoding, etc.
Some things you   need to   know:□       The   scramblin代 写ELEC ENG 3108 Telecommunications Principles Assignment 3: Wideband CDMAMatlab
代做程序编程语言g   codes,   OVSF   codes   and   common   pilot   channel   (CPICH)   have   been   generated   consistent with 3GPP Technical Specification   25.213   Release 4. This standards   document   is      available on the   MyUni website. Pay   particular   attention to   sections   4.3.1,   5.2.1   and   5.2.2.
□         The only common channel   is the CPICH.      No   other   common   channels   (such   as   synch   channel etc) are   in the signal.    So you   can   identify the   scrambling   code   by   correlating the   512   primary   codes against the signal to see which   one   has the   highest   correlation. Only   the real component of the downlink scrambling   code   is   used.
□       The   signal   is   synchronised   -   that   is   the   first   sample   corresponds   to   the   beginning   of   a   38400   chip frame.
□         The traffic channel   is   modulated with   BPSK.    A   positive correlation   (+1)   corresponds to   "1",   a   negative correlation   (-1) to   "0".    No   correlation   (0)   indicates   that   the   channel   is   not   present.
□         Valid traffic channels contain only 8-bit ASCII   characters,   beginning   with   the   most   significant      bit.    The first two characters are an ASCII   representation   of   numerical   digits,   corresponding to a   number   between   "01" and   "99".    The   third character   is   a   space.    This   will   be   sufficient   to   identify valid channels and to   put the traffic channels   in   the   correct   order   to   read   the message.
□         The   message   in the signal   is   up to 99   lines of ASCII   text,   each   of   up   to   1000   characters
(including   padding   in the form. of spaces   (character 32)) and   beginning   with   the   2-digit   and   space   header. Control characters such as   Line   Feed   (10)   and   Carriage   Return   (13)   may   be included.
□         The traffic channels all   begin at   the   start   of the first   frame   but   do   not   continue   for   the   entire   signal.    In   particular, signals with fast   codes   will   finish   early.
Marking:
□         20   marks will   be   based on your technical answers,   including your   code,   signal   analysis   and   the encoded   message.
□         5   marks will   be   based on   how well you explain your   approach.
□          10   marks will   be   based on any additional   detail,   analysis   or   experimentation you   describe   in   your   report. For example, you   might want to   explore   how   the   exercise   compares   with   the real world   (added   noise and   interference,   multipath etc) and   see   how   your   decoder   works when you add   noise to the signal.    You   might also   like   to   discuss   computational   complexity.
Remember,   I'm   not just   looking for some code and some   numbers. I want   a   clear   description   of   how you solved the   problem and some exploration   of WCDMA   using   the   tools   provided   by   this   assignment. 
Don't   panic! The standard   is very explicit   in   its description of   how   to   generate   the   scrambling   and channelisation codes. One   important thing to   note   is that   Matlab starts   its   vector   indices   from   1;   the   standard   is consistent with C and starts   its   vector   indices   from   0,   so   you'll   need   to   allow   for   this.
Some   helpful code to get   started:
function string=bits2str(bitsequence);
bitsequence=(bitsequence>0.001);
% note: +1 = binary   1,   -1   =   binary   0;   8-bit ASCII,   convert   to
%   0   or   1
block=char(reshape(bitsequence,8,length(bitsequence)/8)+48)';
string=char(bin2dec(block));
end
%--------------------
function data=recover(spread,codenumber,tx,scramblecode,nbytes);
data=zeros(1,8*nbytes);
channel=ovsf(spread,codenumber); %you'll need to write the   ovsf   fn
for   j=1:nbytes*8;
k=(j-1)*spread+1;
data(j)=sum(tx(k:k+spread-1).*scramblecode(1+mod(k-1,38400):...
1+mod(k+spread-2,38400)).*channel);
end
The signal file   includes the signal   (transmitsignal) and also   scrambling   code   0
(samplescramblingcode0) so that you can verify that your scrambling   code   function   is   working   properly.





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
