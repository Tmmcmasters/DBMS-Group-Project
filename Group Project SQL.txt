DROP TABLE employer CASCADE CONSTRAINTS;
DROP TABLE buyer CASCADE CONSTRAINTS;
DROP TABLE sales CASCADE CONSTRAINTS;
DROP TABLE contractor CASCADE CONSTRAINTS;
DROP TABLE agreement CASCADE CONSTRAINTS;
DROP TABLE architecture_style CASCADE CONSTRAINTS;
DROP TABLE properties CASCADE CONSTRAINTS;
DROP TABLE agents CASCADE CONSTRAINTS;
DROP TABLE employee CASCADE CONSTRAINTS;



CREATE TABLE employer (
    emp_code NUMBER (2) PRIMARY KEY,
    emp_name VARCHAR2 (40),
    emp_address VARCHAR2 (200),
    emp_phone NUMBER (11)
);
CREATE TABLE buyer (
    buyer_id NUMBER (10) PRIMARY KEY, 
    emp_code NUMBER (2) REFERENCES employer(emp_code),
    buyer_name VARCHAR2 (40), 
    buyer_address VARCHAR2 (200),
    buyer_contact NUMBER (11),
    occupation VARCHAR2 (25),
    salary FLOAT (25),
    account_num NUMBER (10),
    credit_score NUMBER (3)
);
CREATE TABLE contractor (
    c_id NUMBER (10) PRIMARY KEY,
    c_name VARCHAR2(40),
    c_address VARCHAR2 (200),
    c_phone NUMBER (11)
);
CREATE TABLE agreement (
    agreement_id NUMBER (10) PRIMARY KEY,
    c_id NUMBER (10) REFERENCES contractor(c_id),
    a_desc VARCHAR2(250)
);
CREATE TABLE architecture_style (
    arch_id NUMBER (10) PRIMARY KEY,
    arch_name VARCHAR2(40),
    arch_desc VARCHAR2(250)
);
CREATE TABLE properties (
    p_id NUMBER (10) PRIMARY KEY,
    arch_id NUMBER (10) REFERENCES architecture_style(arch_id),
    parcel_num VARCHAR2(40),
    p_address VARCHAR2 (200),
    num_rooms NUMBER (10),
    total_sq FLOAT (7),
    purchase_amt FLOAT (25),
    purchase_date DATE ,
    market_value FLOAT (25)
);
CREATE TABLE agents (
    agent_id NUMBER (10) PRIMARY KEY, 
    p_id NUMBER (10) REFERENCES properties(p_id),
    ag_name VARCHAR2(40),
    ag_address VARCHAR2(200),
    ag_phone NUMBER (11)
);
CREATE TABLE employee (
    e_id NUMBER (10) PRIMARY KEY,
    e_name VARCHAR2(40),
    e_address VARCHAR2(200),
    e_phone NUMBER (11),
    e_role VARCHAR2(30)
);
CREATE TABLE sales (
    sale_id NUMBER (10) PRIMARY KEY,
    buyer_id NUMBER (10) REFERENCES buyer(buyer_id),
    p_id NUMBER (10) REFERENCES properties(p_id),
    agreement_id NUMBER (10) REFERENCES agreement(agreement_id),
    agent_id NUMBER (10) REFERENCES agents(agent_id),
    emp_code NUMBER (2) REFERENCES employer(emp_code),
    arch_id NUMBER (10) REFERENCES architecture_style(arch_id)
);