# protobuf
protoc -I=$SRC_DIR --java_out=$DST_DIR $SRC_DIR/addressbook.proto

protoc -I=. --java_out=. addressbook.proto

# How to Compile Protobuf java_out
# COMPILE PROTOBUF-JAVA.JAR
1. Install Apache Maven if you dont have it: http://maven.apache.org/

2. Set maven environment variables

3. Install jdk if you dont have it

4. Set JAVA_HOME environment variable and set path to %JAVA_HOME%\bin

5. Set protoc in environment variables so $ protoc --version works from ant directory

6. mvn test

7. mvn install

8. mvn package

# COMPILE ADDRESSBOOK.PROTO 
9. protoc -I=$SRC_DIR --java_out=$DST_DIR $PROTO_DIR/addressbook.proto
protoc -I=. --java_out=. addressbook.proto

# COMPILE JAVA CLASSES
10. First copy protobuf-java-3.5.1.jar to the java files directory

11. javac AddPerson.java ListPeople.java com/example/tutorial/AddressBookProtos.java -cp protobuf-java-3.5.1.jar

12. java -cp protobuf-java-3.5.1.jar; AddPerson addressbook.data

13. java -cp protobuf-java-3.5.1.jar; ListPeople addressbook.data

## Google protobuf usage
1. download compiler and protocol buffer source code
   download page: https://code.google.com/p/protobuf/downloads/list
   unzip smae version compiler and source code

2. write proto file

3. compile proto file using downloaded compiler and generate API code
   protoc -I=$SRC_DIR --java_out=$DST_DIR $SRC_DIR/addressbook.proto
          SRC_DIR protocol buffer source code locatoin
		  DST_DIR generating API code location 
		  PROTO_DIR proto file location
		  
4. Add generated API code and protocol buffer source code to project and using it


## example ##
- adding generated API code to project
- copy the downloaded protobuf-2.5.0\java\src\main\java\com folder to project, In API code, import it
- refer to http://developers.google.com/protocol-buffers/docs/javaturorial#builders
