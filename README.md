
<div align="center">
  <img src="https://github.com/user-attachments/assets/1d8c6ebe-c550-45cb-8837-63769552fd65"/>
</div>

&nbsp;

<div align="center">
    <b>SPACERUN</b> a cutting-edge cloud gaming platform <br>delivering the power of console gaming, anywhere, anytime.
</div>

&nbsp;

> [!NOTE]
>
> This project is under active development and not yet open for testing. Features and functionality are still being finalized.

## Introduction


__SPACERUN__ is an advanced, open-source cloud gaming platform engineered to deliver ultra-low-latency, high-quality gaming experiences across a wide range of devices. It’s designed with a clear separation between host and client technologies to optimize each side for the best performance, quality, and compatibility.

Built from the ground up for flexibility and scalability, SPACERUN is ideal for developers, enthusiasts, and innovators who want a cloud gaming solution that is open to modification and can be self-hosted. By leveraging cutting-edge tools and libraries, SPACERUN provides the infrastructure to stream games in real-time with minimal latency, making it suitable for both personal use and large-scale deployments.

[![SPACERUN DEMO #1](https://github.com/user-attachments/assets/21e15572-61d2-4d75-bca8-fb0eb44211d0)](https://www.youtube.com/watch?v=pxAh58DCgoU)

## Features

- __Ultra-Low Latency__: Aiming for sub-50ms latency.
- __High-Resolution Streaming__: Streaming up to 4K resolution at 60 FPS.
- __Cross-Device Compatible__: Designed to stream games across multiple devices, enabling flexible client-side configurations without requiring high-end hardware.
- __Hardware Decoding/Encoding__: Supports hardware-accelerated decoding/encoding with popular codecs like H.264, HEVC, and AV1.
- __Multi-Gamepad Support__: Allows up to 4 gamepads to be connected simultaneously.
- __Self-Hosting Capabilities__: Deployable on both personal servers and cloud infrastructure, providing flexibility for individual or large-scale usage.

## How it Works

SPACERUN operates on a host-client architecture, designed for real-time, low-latency communication between a gaming server (host) and the client application. The platform utilizes P2P (peer-to-peer) communication, allowing for direct, fast video/audio streaming from the server to the client without intermediary servers.

Here’s a step-by-step breakdown of the data flow and processes in SPACERUN:

### Server Side (Host)

1. __Game Rendering__: The game is rendered on the host server using high-performance computing resources, typically leveraging GPU acceleration to ensure smooth, high-frame-rate rendering.

2. __Video Capture and Encoding__: Once the game is rendered, frames are captured and then encoded using GPU hardware acceleration. SPACERUN supports various codecs such as H.264, HEVC, and AV1, ensuring high-quality, efficient encoding. The use of hardware encoding reduces latency and CPU load, optimizing performance.

3. __RTSP Streaming__: The encoded video and audio streams are packaged into an RTSP (Real-Time Streaming Protocol) stream. RTSP allows efficient real-time transmission of multimedia content, which is ideal for high-performance gaming.

4. __Input Handling__: On the server side, the Input Receiver module listens for user input from the client (keyboard, mouse, controller actions). This input is then relayed to the Replay User Input module, where actions are immediately processed in the game environment, ensuring real-time responsiveness.

### Client Side
1. __RTSP Reception and Decoding__: The client application receives the RTSP stream containing video and audio data. Using GPU hardware acceleration, the client decodes the stream in real-time, enabling smooth, high-definition playback on a range of devices without requiring high-end hardware.

2. __Game Display__: The decoded video frames are displayed to the user, creating a high-fidelity gaming experience with minimal latency, effectively mirroring the game running on the server.

3. __User Input Capture and Transmission__: The client captures user input (keyboard, mouse, or controller actions) and sends this data back to the server through the Input Sender module. This data is transmitted over the network using P2P communication, bypassing unnecessary network hops and minimizing delay.

### Network Layer

- __P2P Communication__: By implementing peer-to-peer networking, SPACERUN reduces latency associated with traditional server-based networking. The direct P2P connection between the server and client allows for efficient, low-latency data transmission of both video/audio streams and input commands.

- __Bi-Directional Data Flow__: The network layer supports bi-directional communication: the video and audio data flows from the server to the client, while input data flows from the client to the server. This two-way communication is optimized for gaming, with video/audio streams and user input tightly synchronized.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/user-attachments/assets/3cdfa734-06f9-4f2a-b619-8c1424c6c83e">
  <img alt="" src="https://github.com/user-attachments/assets/06649675-c6c8-4c88-b6c7-de46f789411d">
</picture>

> __SPACERUN__ General architecture

### GPU Hardware Acceleration

Both server and client rely on GPU hardware acceleration for encoding and decoding video, significantly improving performance. GPU acceleration reduces CPU usage, minimizes latency, and enables SPACERUN to handle high-resolution, high-frame-rate video streams without sacrificing quality.

### Highlighted Demo
[![Watch the video](https://github.com/user-attachments/assets/13025372-d10e-4ea7-9e2f-4b41d9a8b99b)](https://youtu.be/w_9GqMiMkVg)

### Demos

| Demo: Chivarly 2                                                                                         | Demo: Forza Horizon 5                                                                                    |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [![Watch the video](https://img.youtube.com/vi/2bpMF2vbXdE/hqdefault.jpg)](https://youtu.be/2bpMF2vbXdE) | [![Watch the video](https://img.youtube.com/vi/AUp_3Uy_yRs/hqdefault.jpg)](https://youtu.be/AUp_3Uy_yRs) |
| Demo: Assassin's creed odyssey                                                                           | Demo: Kingdom Classics                                                                                   |
| [![Watch the video](https://img.youtube.com/vi/OhnVRVknez8/hqdefault.jpg)](https://youtu.be/OhnVRVknez8) | [![Watch the video](https://img.youtube.com/vi/_SBtkIAtcIg/hqdefault.jpg)](https://youtu.be/_SBtkIAtcIg) |
