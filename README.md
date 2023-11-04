# Node-RED Artnet-WebSocket Bridge for Resonite

This repository contains a Node-RED flow that establishes a bridge between Artnet data and a WebSocket. This allows DMX light controllers to be used within Resolume, a Virtual Reality platform.

## Origin Story

This project was born out of a creative and collaborative effort during a Creator Jam in Resonite. Creator Jam is a weekly event in the Resonite community where users come together to build a world around a common theme. It's a time for innovation, sharing knowledge, and communal creativity.

The particular Creator Jam that sparked this project took place on September 24th, and the theme was "I See the Light." Participants were challenged to explore the concept of light and lighting as central thematic elements. The goal was to enrich the virtual environment with dynamic lighting effects, allowing creators to manipulate light within the VR space with the same nuance and control as in the physical world.

This proof of concept aimed to bridge the gap between the physical hardware of lighting systems and the virtual worlds crafted in Resonite.

## Prerequisites

Before you start using this Node-RED flow, you need to have Node-RED installed on your system. If you don't have Node-RED installed, you can find installation instructions at the official [Node-RED website](https://nodered.org/docs/getting-started/installation).

Additionally, you need to install the `node-red-contrib-wsjt-x` package to enable WebSocket communication in your Node-RED environment.

## Installation (UNIX-like)

To set up the Artnet-WebSocket bridge, follow these steps:

1. Clone this repository to your local machine or download the provided Node-RED flow file.

    ```bash
    git clone https://github.com/Rixx-vr/artnet-resonite-ws-bridge.git
    ```

2. Navigate to your Node-RED user directory (typically `~/.node-red`).

    ```bash
    cd ~/.node-red
    ```

3. Install the required Node-RED WebSocket package using npm.

    ```bash
    npm install node-red-contrib-wsjt-x
    ```

4. Start Node-RED.

    ```bash
    node-red
    ```

5. Import the flow into your Node-RED environment using the Node-RED interface.

## Configuration

By default, the bridge listens on port `6464` for Artnet data and makes the WebSocket available at `/ws/artnet`. The default WebSocket port is `1880`, which is standard for Node-RED installations.

To change the listening port or WebSocket path:

1. Open the Node-RED web interface.
2. Navigate to the Artnet-WebSocket bridge flow.
3. Double-click on the WebSocket node to open its properties.
4. Adjust the port and path settings as desired.

## Usage

After setting up the flow and configuration:

1. Deploy the flow by clicking the 'Deploy' button in the Node-RED web interface.
2. Ensure that your DMX light controller is configured to send Artnet data to the IP address of your Node-RED instance on the specified port.
3. Connect to the WebSocket from Resolume using the URL `ws://<node-red-ip>:1880/ws/artnet`.

## Support

If you encounter any issues or have questions regarding the setup, you can:

- Review the Node-RED documentation: [Node-RED User Guide](https://nodered.org/docs/user-guide/)
- Submit an issue in this GitHub repository.

## Contributing

Contributions to this project are welcome. Please follow the standard GitHub flow by forking the repository, making your changes, and submitting a pull request.

## License

[MIT License](LICENSE)