## Chapter 1 - Machine learning 

### exercises

#### 1.1 
three computer applications where machine learning approaches make sense
1. word prediction - based on the user, the machine can learn which word is the most likely word being typed or the which word should be the next word
2. battery savings - based on the user, the system can analyse which programs are most likely to be used and which can be shut down thus saving battery
3. spam prediction - predicting spam emails

Three computer applications where machine learning approaches don’t make sense
1. calculators
2. notepads
3. web browser

#### 1.2 
_learning task_ - battery savings in laptops
the idea here is to determine the best way to save battery life in laptops given a particular user's usage pattern. the machine leanring algorithm can learn the behavior pattern of the user and optimize each application's usage accordingly. it is often the case that users open several battery draining applications at once and forget about them. if the algorithm can predict which application is not likely to be used anymore, then it can save changes in that appliation and either close it or move it to a more silent state where it won't consume a lot of processing power. 
* __Training Experience__ - the training experience could come from going through the usage logs. the usage logs for a given user should be able to tell us his/her pattern of use of the computer and which applications are preferred. 
* __Target function__ - there can be several approaches to the target function here, we could assign each application a priority score based on their usage (frequency) and the time of the day when they are used. For instance, if an application is not usually used during the day and has remained inactive for a while, then the processing of that application be deprioratized. 
* __Representation of learned function__ - we can write a function which computes the priority of each application based on frequency of use during that time of the day and the amount of battery that application consumes. 
so the function can be defined as P(f, w) = 1 - a(w/f)
the said equation says that the priority of the appication will be low if it comsumes a lot of battery and its priority will be high if it actually used during that time of the day. _a_ is the weight to be given to that fraction of w/f.
* __Learning Algorithm__ - the variable _a_ can be tuned over time based on the usage of the user. the frequency of each application will change over time based on the usage behavior of the user.

* References 
1. https://blogs.microsoft.com/ai/a-laptop-battery-system-that-knows-your-habits-and-lasts-a-lot-longer/
2. http://sigops.org/sosp/sosp15/current/2015-Monterey/260-badam-online.pdf
          

