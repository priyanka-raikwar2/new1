When there is a change in proto file , following changes need to be done:
* First change the proto file as required .
* In the respective main.py file add the attributes under pubsub_kafka() within the try block .
* New _pb2.py file will be generated automatically when we deploy the docker image since this command “protoc -I=$SRC_DIR --python_out=$DST_DIR $SRC_DIR/file_name.proto” is already saved in the docker scripts.

The photo file in which we need to add some attributes which changes the sequence of current attributes one additional step is required
* Schema registry needs to be deleted and locked again with the required changes.
