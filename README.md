# AI-assignment
The code is an implementation of a fuzzy logic system to recommend a music genre based on two input parameters:
**tempo** and **energy**. 

 1. **Fuzzy Logic Overview**
Fuzzy logic is a way of processing data that allows for a range of values between true and false, unlike traditional logic, which only allows for absolute true or false values.
 This is useful in situations where things aren't black and white, such as deciding how "fast" or "energetic" a piece of music is.

 3. **Defining Fuzzy Variables**
- **Antecedents (Inputs)**: These are the inputs to the system.
  - `tempo`: Describes the speed of the music (range: 0 to 10).
  - `energy`: Describes the intensity or liveliness of the music (range: 0 to 10).

- **Consequent (Output)**: This is the output of the system.
  - `genre`: The type of music genre recommended (range: 0 to 10).

 3. **Membership Functions**
Membership functions define how each input or output variable is classified into categories:
- **Tempo**: 
  - 'slow': Music is considered slow if the tempo is low.
  - 'medium': Music is considered medium in tempo.
  - 'fast': Music is considered fast if the tempo is high.

- **Energy**: 
  - 'low': Music has low energy.
  - 'medium': Music has a moderate level of energy.
  - 'high': Music is highly energetic.

- **Genre**: 
  - 'chillout': Relaxed and calm music.
  - 'pop': Popular and mainstream music.
  - 'rock': Music with a strong beat and often guitars.
  - 'metal': A heavier and louder style of rock music.
  - 'classical': Traditional orchestral music.

4. **Defining Rules**
The system uses a set of rules to determine the output (genre) based on the inputs (tempo and energy). Each rule looks like this:
- `ctrl.Rule(tempo['slow'] & energy['low'], genre['chillout'])`: This rule states that if the tempo is slow and the energy is low, the recommended genre is 'chillout'.

 5. **Control System and Simulation**
- **Control System**: The set of rules is used to create a control system (`music_ctrl`), which dictates how the inputs are processed to produce the output.
- **Simulation**: The control system is simulated with given inputs (e.g., `tempo = 7` and `energy = 4`) to compute the output.

6. **Computing the Output**
The system calculates the degree to which the inputs match the rules, and then determines the recommended genre. The final genre is decided based on the highest matching degree.

 7. **Output Interpretation**
The code then interprets the output value to determine the recommended genre. For example:
- If the output value is around 3 or less, it suggests 'Chillout' music.
- If it's between 3 and 6, it suggests 'Pop' music, and so on.

Therefore, the code sets up a fuzzy logic system to recommend a music genre based on how fast and energetic the user wants the music to be. 
The system uses fuzzy logic to handle the input data and apply rules to determine the best matching genre.
