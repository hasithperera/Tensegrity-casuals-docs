Recording link: [here](https://nam12.safelinks.protection.outlook.com/?url=https%3A%2F%2Fclemson.zoom.us%2Frec%2Fshare%2Fb4qkWDbil4mKknr1NGdWdC0R1seOH215DJWPlxEkgB2vu_pyFGAiE9AwQIwlbg.B3-gnXLp_RXOFx7A&data=05%7C02%7Caperera%40clemson.edu%7C009e2375ac124ffdb87308df2b27b7c7%7C0c9bf8f6ccad4b87818d49026938aa97%7C0%7C0%7C639277121757654080%7CUnknown%7CTWFpbGZsb3d8eyJFbXB0eU1hcGkiOnRydWUsIlYiOiIwLjAuMDAwMCIsIlAiOiJXaW4zMiIsIkFOIjoiTWFpbCIsIldUIjoyfQ%3D%3D%7C0%7C%7C%7C&sdata=umYpVXWQES2afLJmh0wLsLJXtuE5WiQzItrz9%2BlNEY0%3D&reserved=0)
## Quick recap

The team met to discuss design options for their tensegrity robot project, specifically deciding between the Yale design and a central controller design. Hasith presented both approaches, explaining that the Yale design would be easier to implement with existing components while the central controller design would require significant redesign work including 12 motors and custom electronics. After thorough discussion of the pros and cons, including timeline constraints and technical complexity, the team unanimously decided to proceed with the Yale design approach. The group reviewed the bill of materials, identified components that needed specifications like battery dimensions from the CAD models, and discussed adding a Raspberry Pi for easier development. Hasith agreed to order the PCB and complete the electronics redesign, while the team planned to finalize component specifications and submit the complete bill of materials by Monday afternoon for the upcoming deadline.

## Next steps

- Hasith: Finalize and order the custom PCB redesign for the Yale design by tomorrow, after confirming reimbursement with the organizer.
- Justin: Find and select a suitable lithium-ion battery based on the dimensions from the Yale CAD model and add it to the BOM.
- Justin: Share the SolidWorks CAD model dimensions for the battery with the team.
- Hasith: Complete the wiring diagram for the Yale design before the 20th deadline.
- David: Finalize the mechanical design and dimensions for the Yale struts, based on the CAD models.
- Team: Hold a meeting on Monday to finalize the bill of materials before the workshop day.
- Hasith: Send an email to the organizer to confirm reimbursement for the PCB cost.

## Summary

### Robotics Project Design Progress

The team discussed progress on their robotics project, with Hasith reporting on a recent meeting where they received approval for their external controller approach similar to Yale's design. They reviewed two potential design options: the current Yale design requiring complex control algorithms and the alternative tensegrity design which would be more stable and easier to implement but might not meet the competition requirements. The team agreed to schedule a follow-up meeting on Monday to finalize the bill of materials before the Tuesday deadline, with Hasith taking responsibility for completing the PCB redesign and creating the wiring diagram.

### Yale Model Design Discussion

Hasith and David discussed the design differences between a Yale model and an MIT video, focusing on the Yale model's suspended design without a tethered cable. Hasith explained that the Yale model requires an external control system to maintain stability, similar to a tensegrity structure that uses cameras to track colors and adjust positioning. They examined a physical robot with carbon fiber construction and winches that route cables through the structure, with motors positioned near the center of mass. The discussion included details about how the cable system works, with one face of the structure having a single winch system.

### Robot Design Approaches Discussion

Hasith discussed two potential robot design approaches for a 10-week project, explaining that the main evaluation criteria appear to be distance traveled and locomotion capabilities. He presented a simpler Yale design using 2 motors with a central controller versus a more complex 12-motor central design with internal sensors. Hasith proposed creating a backup plan by building both designs, with the Yale approach requiring minimal PCB work while the central design would need significant mechanical and electronics redesign. The team discussed coding responsibilities, with Hasith suggesting he could handle the bare metal coding for the Yale design using Wi-Fi-based remote control commands.

### Robot Design Technical Challenges

Hasith explained the technical challenges and requirements for implementing a robot design, discussing both a Yale design and an alternative design with carbon fiber components. He estimated 2-4 hours of coding work for basic motor and encoder functionality, but identified significant complications around fall detection and control systems, particularly the need for active response during drops which he considered the main technical challenge. The discussion highlighted electronics design requirements including motor controllers and power management for the 12-motor system, with Hasith noting that while software implementation would be relatively straightforward, the hardware and control systems would require more development time.

### Yale Design Implementation Decision

Justin and Hasith discussed the decision to proceed with the Yale design rather than restarting with a central design due to time constraints and the complexity of redesigning mechanical and electrical components. Hasith expressed that while the Yale design would be simpler to implement, there are concerns about the feasibility of the drop test functionality, estimating a 70% chance of success for the rolling feature and uncertainty about the drop test. David agreed that the Yale design would be the simplest approach.

### Yale Design Implementation Challenges

Hasith and David discussed the challenges of implementing the Yale design for their robot project, particularly regarding the drop test requirements and the need for a fast response system using force feedback sensors and IMU measurements. Hasith expressed concerns about the complexity of implementing the system within the 10-week deadline, estimating a 30% chance of success. Both participants acknowledged that while the central design might be preferable, time constraints make the Yale design more practical, though neither sees this as primarily about winning but rather as a learning opportunity.

### Custom PCB Design for Yale

Hasith explained his plan to create a custom PCB for the Yale project, which would simplify the design by removing unnecessary components while maintaining the same dimensions and functionality. He noted that either option would require ordering a PCB, with the custom version offering better debugging capabilities through additional connections. David asked about improving upon the electronics from A01, and Hasith clarified that while the custom board would be smaller, they could also order the existing PCB without populating all components. The discussion ended with David mentioning the Yale Bill of Materials and budget, though the specific details about next steps were not fully completed in the transcript.

### Project Electronics and BOM Planning

The team discussed the electronics and bill of materials for their project, deciding to use the Yale design with modifications. They agreed to add a Raspberry Pi and will need to find specific battery dimensions from the CAD models to source appropriate lithium-ion batteries. Hasith will handle ordering the custom PCB, while Justin will research battery specifications and a charger. The team set a budget target of around $500-700 and will submit the final bill of materials by Monday afternoon for a weekend deadline.

---

**Attendees:** Hasith Perera (Organizer), Jaylin Washington (External), David Niemczura, Justin Hsu