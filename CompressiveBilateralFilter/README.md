
```bash
# run docker container
docker run -it --rm -v $HOME/coding/:/opt/coding -w /opt/coding codesignal/opencv:v9.4.0
```

```bash
# build
./run.sh

# run program
./build/main input/inv_depth7.png input/cur_rgb1_ref.png 
```