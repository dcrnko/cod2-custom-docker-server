# My Custom Call of Duty 2 Docker Server

This project is an adjusted version of the excellent work by **bgauduch**. This repository is intended for a closed circle of friends to be used when necessary.

---

## Original Project Details

* **Author:** bgauduch
* **Original Repository:** [https://github.com/bgauduch/call-of-duty-2-docker-server](https://github.com/bgauduch/call-of-duty-2-docker-server)

---

## My Adjustments

I've modified this project to include:

* Added rcon password (available on request).
* Added server password (available on request).

---

## How to Use

### 1. Preparing Game Data

To run the server, you need to provide the necessary game data:

1.  Clone or download this repository to your host machine.
2.  Copy required data from the main folder of your original game (install directory or retail DVD) to the `cod2server/main` folder within this project:
    * Copy all `iw_XX.iwd` files (from 00 to 15).
    * Copy all localization files (e.g., `localized_english_iwXX.iwd` - adjust language if needed).

**OR**

* Request the FULL Docker image if available.

### 2. Launching and Managing the Server

1.  **Launch the server** from the project root directory:
    ```bash
    docker-compose up -d
    ```
2.  **Restart the server** (e.g., to pick up config changes):
    ```bash
    docker-compose restart cod2_server
    ```
    *Note: `cod2_server` refers to the name of the service in the `docker-compose.yml` file.*
3.  **View server logs:**
    ```bash
    docker-compose logs -f cod2_server
    ```
4.  **Attach a shell to the server** to run commands (like `status` or `map_rotate`):
    ```bash
    docker container attach call-of-duty-2-docker-server_cod2_server-1
    ```
    * **Example Commands:**
        ```
        status
        map_rotate
        ```
    * **To detach:** Use the escape sequence `CTRL+P`, then `CTRL+Q`, or simply type `quit` if the server console allows it.
5.  **Completely stop the server:**
    ```bash
    docker-compose down
    ```

---
### Conencting to the server:
1.  **Launch the COD2 MP** in the menu press the console button and type:
   ```bash
   /password <the_requested_passowrd> 
   ```
2. **Open the console again** and type:
   ```bash
   /connect <private/public_ip_of_the_docker_hoste:28960>
   ```
3. **Login with rcon** :
   ```bash
   /rcon login <requested_rcon_password>
   ```
4.  **If you need more rcon commands visit** : [here](https://github.com/dcrnko/cod2-rcon-commands)
5.  **Have Fun**
---
## Thanks

A huge thank you to **bgauduch** for creating the foundational work for this project!
