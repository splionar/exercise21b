# Instructions to reproduce results

### 1. Clone this repository and go to its directory
```bash
git clone https://github.com/splionar/exercise21b.git
cd exercise21b
```
### 2. Build docker image in laptop (amd64 machine)
```bash
dts devel build -f --arch amd64
```

### 3. Make sure docker image from exercise21a is running. Afterwards, run exercise21b docker image with the following options.
```bash
docker run -it --rm -e ROS_MASTER_URI=http://[MY_ROBOT_IP]:11311/ -e ROS_IP=http://[MY_LAPTOP_IP]:11311/ --net host duckietown/exercise21b:v1-amd64
```
Image stream with color detector is published.
