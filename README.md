"# soft_modeling_and_design" 
State Specifications
Green Light ON:

Description: In this state, the green light is on, allowing vehicles to move through the intersection.
Duration: This state is usually maintained for a set period (e.g., 30 seconds).
Transition:
When the timer for the green light expires, it transitions to the Yellow Light state.
Yellow Light ON:

Description: In this state, the yellow light is on, warning vehicles that the light is about to turn red.
Duration: This state is typically maintained for a short duration (e.g., 5 seconds).
Transition:
When the timer for the yellow light expires, it transitions to the Red Light state.
Red Light ON:

Description: In this state, the red light is on, indicating vehicles must stop.
Duration: This state lasts for a set time or until it is safe for pedestrians to cross.
Transition:
If the pedestrian signal is triggered (e.g., a button is pressed by a pedestrian), the state transitions to Pedestrian Crossing.
If no pedestrian signal is triggered, it may eventually loop back to Green Light after a delay.
Pedestrian Crossing ON:

Description: This state allows pedestrians to cross the road safely.
Duration: Maintained for the time required for pedestrians to cross.
Transition:
Once the pedestrian crossing time expires, the system transitions back to Green Light ON.
Transition Narration
Green Light ON ➔ Yellow Light ON:

Triggered by a timer expiration, this transition occurs after a fixed period to warn vehicles that the light is about to turn red.
Yellow Light ON ➔ Red Light ON:

Triggered by a timer expiration, this transition shifts the traffic control to a red light, requiring vehicles to stop.
Red Light ON ➔ Pedestrian Crossing ON:

Triggered by a pedestrian signal (e.g., a button press), this transition allows pedestrians to cross safely. If no pedestrian signal is activated, this transition may not occur.
Pedestrian Crossing ON ➔ Green Light ON:

Triggered by the pedestrian crossing timer expiration, this transition returns the traffic lights to green, allowing vehicles to move again.
