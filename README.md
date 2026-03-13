# Hand-Gesture-Controlled-Video-Player
The Hand Gesture Controlled Video Player is an interactive system that lets users control video playback using hand gestures.

## Objective
One of the primary aims is to improve the way users interact with video content by providing a more intuitive and immersive experience. Gesture control can make interactions feel more natural and fluid compared to traditional input methods like remote controls or keyboards.  

The objectives of the gesture-controlled video project include:  
- **Improve user experience** by making interactions more natural and fluid.  
- **Innovate in technology development** through gesture recognition systems.  
- **Increase accessibility** for users who may find traditional input devices difficult.  
- **Demonstrate technical feasibility** of gesture-based video control.  
- **Explore commercial opportunities** in entertainment, healthcare, and education.  
- **Contribute to academic research** in the field of human-computer interaction.  

---

## Components Used

### Hardware
- **Arduino UNO board** – Acts as the central controller for reading sensor data and communicating with the computer.  
- **2 Ultrasonic Sensors** – Placed to detect hand gestures by measuring the distance of the hand from the sensors.  

### Software
- **C++** – For Arduino programming.  
- **Python** – With `pyautogui` library for gesture-to-video control.

## Working

Two ultrasonic sensors are placed on top of the monitor to detect hand gestures. The Arduino UNO reads the distance between the sensors and the hand, then sends this data via serial communication to the computer. Python, using the `pyautogui` library, interprets the data and performs video control actions.

### Actions Implemented
1. **Both hands (far distance):** Play/Pause video.  
2. **Right hand (far distance):** Fast Forward one step.  
3. **Left hand (far distance):** Rewind one step.  
4. **Right hand (near distance, move):** Move towards → Fast Forward, move away → Rewind.  
5. **Left hand (near distance, move):** Move towards → Volume Decrease, move away → Volume Increase.  

### Setup Notes
- Ultrasonic sensors connected to Arduino digital pins (2,3,4,5) powered by +5V.  
- Serial communication between Arduino and Python at **9600 baud rate**.  
- Distance is calculated using a function `calculate_distance()`.  
- Variables `distL` and `distR` store current distance values for gesture comparison.  


