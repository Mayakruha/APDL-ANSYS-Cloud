# APDL-ANSYS-Cloud
The macroses extract temperature/displacement and coordinates for parts from the APDL ANSYS model and write them into the files.
The macros DisplCloud.mac extracts displacement and coordinates
The macros TempCloud.mac extracts temperature and coordinates
The macros DisplMesh.mac extracts displacement and mesh

---Scope---
The macroses are useful when boundary conditions (temperature, displacements) based on result from another model made in APDL ANSYS have to be applied.
The macroses create a file with temperature/displacement cloud for every time point and a table file with file names and time in case of transient. 

---Steps---
1. Edit the macros.
 - Set a number of parts for extracting (ComponentNum = __).
 - Edit the table Cmpnt.
2. Load a model and a result in APDL ANSYS.
3. Run the edited macros in APDL ANSYS.

---Table Cmpnt---
The first row - a name of a part. The name is added as a postfix to the file name.
The second row - options. There are two options: 'MINMAX' and 'SUBSET'.
 - 'MINMAX': extracting by minimum and maximum numbers of a range.
 - 'SUBSET': extracting by a name of a set.
The third row. If option is 'MINMAX' the third row is minimum number of elements range. If option is 'SUBSET' the third row is type of a set ('ELEM' - a set of elements; 'NODE' - a set of nodes)
The fourth row. If option is 'MINMAX' the third row is maximum number of elements range. If option is 'SUBSET' the third row is a name of a set.

*Note: An example for 3 parts ('Finger', 'TH', 'CBH') with different options is commented in the macros below the table Cmpnt.
