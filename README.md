608week8quiz
============
-- Table: "AppleEmployees"

-- DROP TABLE "AppleEmployees";

CREATE TABLE "AppleEmployees"
(
  "EmployeeID" integer NOT NULL,
  "First_Name" character varying(50),
  "Last_Name" character varying(50),
  "Employee_Title" character varying(50) NOT NULL,
  "Supervisor_Title" character varying(50),
  CONSTRAINT "AppleEmployees_pkey" PRIMARY KEY ("EmployeeID")
)
WITH (
  OIDS=FALSE
);
ALTER TABLE "AppleEmployees"
  OWNER TO postgres;
  
  
  INSERT INTO "AppleEmployees"(
            "EmployeeID", "First_Name", "Last_Name", "Employee_Title", "Supervisor_Title")
    VALUES(2,'SCOTT','FORSTALL','SVP-IOS-SOFTWARE','CEO');
    
  INSERT INTO "AppleEmployees"(
            "EmployeeID", "First_Name", "Last_Name", "Employee_Title", "Supervisor_Title")
    VALUES(3,'PETER','OPPENHEIMER','SVP-CFO','CEO');
    
INSERT INTO "AppleEmployees"(
            "EmployeeID", "First_Name", "Last_Name", "Employee_Title", "Supervisor_Title")
    VALUES(20,'BESTY','RAFAEL','VP CONTROLLER','SVP-CFO');
   INSERT INTO "AppleEmployees"(
            "EmployeeID", "First_Name", "Last_Name", "Employee_Title", "Supervisor_Title")
    VALUES(21,'GARY','WIPFLER','VP.TREASURER','SVP-CFO');
    
    INSERT INTO "AppleEmployees"(
            "EmployeeID", "First_Name", "Last_Name", "Employee_Title", "Supervisor_Title")
    VALUES(30,'KIM','VORRATH','VP.PROGRAM-MANAGEMENT','SVP-IOS-SOFTWARE');
    INSERT INTO "AppleEmployees"(
            "EmployeeID", "First_Name", "Last_Name", "Employee_Title", "Supervisor_Title")
    VALUES(31,'ISABEL','GE MAHE','VP-IOS-WIRELESS-SOFTWARE','SVP-IOS-SOFTWARE');
    
    
    ##(2)
    SELECT * 
    FROM AppleEmployees
    ORDER BY EmployeeID
    ##(3) I will assume that all employees are recorded into the table already
    ## also I will assume that Tim Cook ID=5 and his previous position is COO
    ## to have Tim on the table ,I will do
    INSERT INTO "AppleEmployees"(
            "EmployeeID", "First_Name", "Last_Name", "Employee_Title", "Supervisor_Title")
    VALUES(5,'TIM','COOK','COO','CEO');
    # to have Susan Wojcicki as a new employee from google to Apple ,I will assume that her assigned EmployeeID 15 ,I use this #  #query to have her on the table.
    #STEVE DECEASED
    UPDATE AppleEmployees
    SET Employee_Title=NULL
    WHERE EmployeeID=1;
    #TIM PROMOTION
    UPDATE AppleEmployees
    SET Employee_Title='CEO',Supervisor_Title=NULL
    WHERE EmployeeID= 5;
    # Susan moving in!
    INSERT INTO "AppleEmployees"(
            "EmployeeID", "First_Name", "Last_Name", "Employee_Title", "Supervisor_Title")
    VALUES(15,'SUSAN','WOJCICKI','COO','CEO');
    
    





