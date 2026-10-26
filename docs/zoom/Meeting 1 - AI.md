## Quick recap

The team met to discuss the Tensegrity robot design project for a competition with a 10-week timeline and approximately $500 budget per team. Hasith explained the two available design options: a 3-bar design with multiple struts or a 6-bar more complex design, both requiring the robot to survive a drop and potentially roll away. The team discussed using Yale's open-source hardware design, but Hasith identified challenges with the proposed ESP32 board being too large (6.5cm) to fit in the current mechanical design. David agreed to extract dimensions from the Yale CAD files to assess feasibility of scaling up the design, while Hasith committed to redesigning the PCB to be smaller and more suitable for the mechanical design. The team also discussed using resin printers for durable components and potentially using ROS (Robot Operating System) for control, with Garren offering a spare Raspberry Pi 4 for the project.

## Next steps

- David: Pull the Yale CAD files, extract dimensions, and upload them to Teams by tomorrow.
- David: Create a scale-down (toy) model of the strut for visualization by October 16th.
- Justin: Print the scale-down model once David provides the files.
- Hasith: Redesign the PCB based on the Yale design, minimizing unnecessary components, and aim to complete by October 16th.
- Hasith: Email the faculty (Lu Shan/Dujan) to schedule a meeting for Thursday afternoon to discuss the PCB and design feasibility.
- David & Jaylin: Work on translating the Yale bill of materials (BOM) to fit the team's mechanical design.
- Garren: Investigate the feasibility of using the larger proposed controller board (ESP32) and potential mechanical designs to accommodate it.
- Hasith: Post the GitHub repository link and Obsidian setup instructions in Discord.

## Summary

### Robotics Project Planning Meeting

The team met to discuss their robotics project, with members introducing their skills and backgrounds. David shared his experience with SolidWorks and resin printing, while Justin mentioned his access to the Makerspace and the ordering of two new Form 4 printers. The group discussed the availability of resin printers at Yale, noting that only flexible resin was currently available. Hasith proposed reviewing the Yale documentation together to assess what needed to be changed or adapted for their project.

### Robot Design Options Discussion

The team discussed two design options for a robot competition: a 3-bar strut design and a 6-bar design, with Hasith recommending the simpler 3-bar option using 6 struts and 3 identical units. They reviewed the budget constraints of around $500 per team and the 10-week timeline to complete the project by December. The discussion focused on choosing between using Yale's custom PCB design versus a more straightforward approach with a Wemos board, though Hasith expressed concerns about the dimensions of the Wemos board not fitting well with the Yale design's mechanical components.

### Parallel Mechanical Design Approaches

Hasith proposed creating two parallel mechanical designs for a project, one based on Yale's specifications and another with minimized hardware components. The team agreed to pursue this approach, with Hasith handling PCB design by simplifying the Yale design by removing unnecessary components like force sensors and complex sensors. Justin suggested dividing the mechanical design work among the team's four mechanical engineers, and the group discussed that both designs would use Arduino-based systems for programming simplicity.

### Robotic System Design Discussion

The team discussed the design and materials for building a robotic system with two motors and control mechanisms. David agreed to download and extract CAD files from the Yale design to obtain dimensions, while Hasith explained they would build one strut with two parallel designs (one square and one Yale equivalent) before creating three copies total. The team decided to use resin printers for the toxic resin end caps and PLA for housing components, with David offering his bamboo printer as an alternative for flexible materials if needed. The discussion concluded with Hasith mentioning MQTT as a potential control protocol for the system.

### Robot Sensor System Architecture

Hasith explained the technical details of a sensor system for a robot, describing how multiple sensors including IMUs, encoders, and current sensors would be connected to microcontrollers to measure various parameters like acceleration, rotation, and tension. He outlined the communication architecture using MQTT protocol over Wi-Fi, with data being transmitted to a centralized Raspberry Pi or laptop controller running Python code. Hasith emphasized that while the system appears complex, it's more intricate than initially realized, particularly due to the absence of force feedback mechanisms that simplify other robot designs.

### Robot Motherboard Design Planning

David and Hasith discussed the dimensions of a motherboard for their robot project, determining it measures 3 centimeters by 14 centimeters, which is significantly larger than the standard board they were considering. Hasith suggested creating a custom PCB with the specified dimensions and 3D printing the mounting hardware. The team agreed to create a detailed bill of materials, including a Raspberry Pi, and decided to separate the list into mechanical and electronics categories. Garren offered a spare Raspberry Pi 4, and David suggested creating their own bill of materials to assess the budget. Hasith proposed meeting with faculty next week to review their current plan.

### Motherboard Design Fit Challenges

Hasith and David discussed challenges with a mechanical design involving a motherboard with dimensions of 6.5 centimeters, which is larger than expected and may not fit the current design requirements. They explored options like scaling up the design or using a core mechanism, but noted that recalculating motor torques would be necessary if they proceed with the scaled-up approach. The conversation also touched on the need for multiple controller boards and different battery configurations compared to the Yale design.

### Model Scaling and Documentation Planning

The team discussed challenges with scaling up the model, with Garren expressing concerns about additional work required for larger components or a central box design with stacked motor controllers. Hasith requested the creation of a scale-down mock model to better visualize the connections, with David agreeing to handle the documentation of dimensions by the end of next week. Hasith also introduced a GitHub repository with an Obsidian note-taking setup for task management and documentation, and agreed to share installation instructions in Discord for the team to follow.

### 3D Model and BOM Planning

The team discussed printing a small 3D model for visualizing their design and assigned tasks for the bill of materials (BOM) translation. Hasith will handle the electronic BOM portion, while David and Jaylin will work on the mechanical design. They scheduled a meeting with Fervin for Thursday afternoon to discuss the high-level control design and potential MQTT implementation. The team also explored using ROS (Robot Operating System) as a possible solution for programming and simulation, though they decided to review mechanical designs first before making a final decision at next week's meeting.

---

**Attendees:** Hasith Perera (Organizer), David Niemczura, Garren Adamson, Justin Hsu, Jaylin Washington (External)