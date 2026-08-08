# LTL-s-desk-setallite

the desk setallite of LTL in summer camp project

**李坦来**

**GitHub仓库：[github.com/benchuziwuxian2-alt/LTL-s-desk-setallite.git](https://github.com/benchuziwuxian2-alt/LTL-s-desk-setallite.git)**

**硬件描述：机械革命翼龙16pro**

**WR1**

Refined System Architecture Overview (Excluding Powertrain)
This system uses a layered architecture centered on the NVIDIA Jetson Xavier NX (reComputer J2021) for autonomous environment perception and decision-making. The core functional modules are:

1. Core Computing and Control Unit: NVIDIA Jetson Xavier NX (reComputer J2021)
   This integrated module serves as the system's "brain." It runs Ubuntu and ROS for complex algorithms, performs AI inference and SLAM for object detection and path planning, and communicates with sensors and actuators via USB, UART, and GPIO interfaces.
2. Perception Subsystem: Distance Sensor and Camera
   LiDAR Distance Sensor (e.g., TFmini-S): Connects via UART to provide direct obstacle distance data for close-range collision avoidance.

AI Vision Camera (e.g., OAK-D IoT-40): Connects via USB to transmit RGB images and also performs edge AI inference to send structured data (e.g., object types and locations) to the main controller.

3. Power Supply Unit
   Voltage Regulator (e.g., LM2591HVS-12): Steps down the main battery voltage to a stable 12V and a cerrent of 1A for the LiDAR

Overall Advantages and Disadvantages of This Architecture
Advantages

-High Computational Power: The Jetson Xavier NX provides up to 21 TOPS of AI performance for on-device deep learning models.

-Strong System Integration: The reComputer J2021 combines the module and carrier board with a rich set of I/O interfaces, simplifying sensor connections.

-Rich Software Ecosystem: Support for NVIDIA JetPack, Ubuntu, and ROS accelerates software development.

-Smart Sensor Fusion: Combining LiDAR for accurate ranging and an AI camera for visual information enables robust environmental perception.

Disadvantages

-High Overall Cost: The total cost of the main components (Jetson module, AI camera, and LiDAR) is significant, which is a major consideration for budget-sensitive projects.

-Complex System Integration: The system requires in-depth knowledge of embedded Linux, driver configuration, and multi-interface (USB, UART) management.

-High Power Consumption: The Jetson (peak ~15W) and camera (~2W-5W) demand a well-designed power supply system.

-Software Dependency: The OAK-D camera relies on the DepthAI library, introducing an external dependency to manage and update.

-Hardware Debugging Effort: Ensuring stable operation across components from different vendors and managing potential noise from the switching regulator can require considerable debugging time.

**microcontroller(main):[www.digikey.com/en/products/detail/seeed-technology-co-ltd/102110409/12323558?s=N4IgTCBcDaIFIFMAuBnA9gOwAQA0CGAbgJYIBOWAcjlgLZoAmArgDYIgC6AvkA](https://www.digikey.com/en/products/detail/seeed-technology-co-ltd/102110409/12323558?s=N4IgTCBcDaIFIFMAuBnA9gOwAQA0CGAbgJYIBOWAcjlgLZoAmArgDYIgC6AvkA)**

**microcontroller(LIDAR):[www.lcsc.com/product-detail/C8304.html?s_z=n_q_t_STM32F103&amp;spm=wm.fly.bg.0.xh___wm.ssy.tc.0.tz&amp;lcsc_vid=QwdeAlAAFlUKXwBRFgJYAQFVElJeBABVTgJdVlJSElUxVlNeQlRZUV1XTllYVDsOAxUeFF5JWBYZEEoKFBINSQcJGk4dAgUUFAk%3D](https://www.lcsc.com/product-detail/C8304.html?s_z=n_q_t_STM32F103&spm=wm.fly.bg.0.xh___wm.ssy.tc.0.tz&lcsc_vid=QwdeAlAAFlUKXwBRFgJYAQFVElJeBABVTgJdVlJSElUxVlNeQlRZUV1XTllYVDsOAxUeFF5JWBYZEEoKFBINSQcJGk4dAgUUFAk%3D)**

**censor(LIDAR):[www.lcsc.com/product-detail/C7386355.html?s_z=n_q_ToF%2520Distance%2520Sensor&amp;spm=wm.fly.bg.0.xh&amp;lcsc_vid=QwdeAlAAFlUKXwBRFgJYAQFVElJeBABVTgJdVlJSElUxVlNeQlRZUFRST1daVzsOAxUeFF5JWBYZEEoKFBINSQcJGk4dAgUUFAk%3D](https://www.lcsc.com/product-detail/C7386355.html?s_z=n_q_ToF%2520Distance%2520Sensor&spm=wm.fly.bg.0.xh&lcsc_vid=QwdeAlAAFlUKXwBRFgJYAQFVElJeBABVTgJdVlJSElUxVlNeQlRZUFRST1daVzsOAxUeFF5JWBYZEEoKFBINSQcJGk4dAgUUFAk%3D)**

**voltage-regular(LIDAR):[www.lcsc.com/product-detail/C5240479.html?s_z=n_q_LM2591HVS-12%2520%28UMW%29&amp;spm=wm.fly.bg.0.xh&amp;lcsc_vid=QwdeAlAAFlUKXwBRFgJYAQFVElJeBABVTgJdVlJSElUxVlNeQlRZXlZeTlVYVzsOAxUeFF5JWBYZEEoKFBINSQcJGk4NBhADEA4cHktXR1JcSQwSGg0%3D](https://www.lcsc.com/product-detail/C5240479.html?s_z=n_q_LM2591HVS-12%2520%28UMW%29&spm=wm.fly.bg.0.xh&lcsc_vid=QwdeAlAAFlUKXwBRFgJYAQFVElJeBABVTgJdVlJSElUxVlNeQlRZXlZeTlVYVzsOAxUeFF5JWBYZEEoKFBINSQcJGk4NBhADEA4cHktXR1JcSQwSGg0%3D)**

**camera:[www.digikey.com/en/products/detail/sparkfun-electronics/18737/15842544](https://www.digikey.com/en/products/detail/sparkfun-electronics/18737/15842544)**

**BOM:[点击查看BOM](<task1/WS1%20-%20Power%20-%20Sample%20BOM.xlsx>)**
