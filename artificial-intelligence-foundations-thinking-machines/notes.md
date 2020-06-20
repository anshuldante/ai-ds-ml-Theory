# AI Foundations: Thinking Machines

* Symbolic systems approach (pattern matching), weak and string AI:
* Symbol matching was assumed to be AI.
* The Chinese room
* String AI/General AI: applies to a multitude of tasks.
  Eg. a string AI might learn a new language just for the joy.
* Weak AI/Narrow AI: does limited tasks.
* A system that uses symbolic systems approach, should be considered a weak AI.
* Expert System: some experts input a lot of data and the outcomes based on it and the system uses these to respond to queries.

* **Planing AI:**
  * Plan AI: Using heuristics the AI predicts and limits the number of patterns to match against.
  Eg. Google Maps (it knows that there are only a limited number of possibilities); Legal Contracts, Logistics and Video Games.
  * For Planning AI to work, the heuristics should be correct, otherwise whatever they do after the first wrong assumption, everything will be incorrect.

* **Artificial Neural Networks:**
  * A biological brain has billions fo neurones, they connect to one another using signals using synapses.
  * Neurones increase the strength of the connections based on human experiences.
  * Eg. if you want to learn to juggle, your brain will create new neural connections and strengthen existing connections.
    * That's why you can often improve over time.
  * Neurones in an AI are organized into layers, are arranged like players in a marching band.
  * You start with the first player in the input layer, hop through all in between layers untill we get to the final output layer.
  * The players in between are called hidden layers.
  * The leaders in front won't have any instruments, their job is to listen to the music and pass individual notes to the players in the hidden layers.
  * Each player in the hidden layer will then tune the instrument to sound like the node,
    * if it sounds a lot like the note, they'll pass it on to the next layer with say 90% confidence.
    * If it didn't sound anything like the note, they'll send it back with say 10% confidence.
    * If they're sure it wasn't the sound they won't pass it back either.
  * If you run this enough times, you'll have a complete picture of all the sounds!.
  * No one really knows how to play the music but they'll be able to play it with large scale trial and error.
  * The approach can be really time consuming.
  * Experts generally try to tweak the AI to make it more efficient.
  * Maybe they found that every song and has at least some notes played by a guitar.
    * If yes, they'll give the guitar player to have a little more confidence.
    * This will improve the efficiency of the program.
  * These AI also tweak their own weights as well, for ex. if someone's stuck with a Oboe, they'll routinely say no with confidence.
  * This is similar to our brains with practice.
  * Artificial Neural network based AI train themselves over and over to get better over time.
  * Deep learning means having a lot of hidden layers between the input and output layers.
  * Back Propagation make sure that all of the nodes share their knowledge quickly.
    * It goes back and forth to strengthen many of the neural connections.
  * Clustering allows the networks to categorize their findings.
  * Deep learning and Machine Learning are backed by the large amounts of data we have access to.
  * If you want a system to deduce if the uploaded image is a cat or not, you can just upload millions of cat images and let it learn.

* **Finding the right approach:**
  * Symbolic reasoning: abstract problem but known steps.
  * Machine learning: unknown steps but you still have to look for patterns. Requires iterations.
  * Some researchers mix the approaches, they use symbolic reasoning to come up with constraints and then use ML to experiment with different answers.
  * If you want to write an AI to recognize ceiling fan:
    * If you use use symbolic reasoning: Have some experts define some attributes like location, manufacturers etc. going step by step and then making a decision.
    * Deep Learning:
      * You'll pump in a lot of data. First you could train it to recognize fans using images and videos.
      * Then attach a sensor to detect changes in wind speed. Then it'll be able to detect patterns of wind moving in the room.
  * Symbolic reasoning will work for most ceiling fans. but it might fail on new designs.
  * ML can zero in on a perfect pattern, it'll be flexible once you've fed it enough data. It doesn't rely on humans.
    * If it uses wind speed patterns and hums for the whooshing sounds, it might do better than humans and detect in pitch dark rooms.
    * Requires access to too much data and a lot of other sensors to get it working.

* **Supervised and Unsupervised learning:**
  * Supervised Learning
    * After millions of tries with enough data, our AI might be able to play in input song well, but we might not know how it actually did that.
    * But still some human intervention might be required.
    * Say you want the layers behind the Input Layer to be able categorize the given songs.
    * In super, you give the AI enough sample data and categorize it for the AI.
  * Unsupervised Learning:
    * You just feed a LOT OF DATA and let it categorize, it might not be human relevant but the categorization will be better.
    * ADV: The categorization will be much more accurate. Eg. Apple music.
    * DisAdv: It may create too many categories which may be usable for humans.

* **Back-propagation:**
  *. Used on supervised learning, the developer provides a way for the program to know that it's going in the wrong direction and then go back and tweak/adjust the weights/gradients.
