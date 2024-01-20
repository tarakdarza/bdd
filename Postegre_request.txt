
-- DROP SCHEMA "DNF1ED11";

CREATE SCHEMA "DNF1ED11" AUTHORIZATION postgres;

-- "DNF1ED11".customer definition

-- Drop table

-- DROP TABLE "DNF1ED11".customer;

CREATE TABLE "DNF1ED11".customer (
	"CustomerId" int4 NOT NULL,
	"Surname" varchar(40) NULL,
	CONSTRAINT customer_pkey PRIMARY KEY ("CustomerId")
);

-- "DNF1ED11".info_bank definition

-- Drop table

-- DROP TABLE "DNF1ED11".info_bank;

CREATE TABLE "DNF1ED11".info_bank (
	id_tech_bank varchar NOT NULL,
	"CustomerId" int4 NOT NULL,
	"CreditScore" int4 NULL,
	"Tenure" int4 NULL,
	"Balance" float4 NULL,
	"NumOfProducts" int4 NULL,
	"HasCrCard" int4 NULL,
	"IsActiveMember" int4 NULL,
	"EstimatedSalary" float4 NULL,
	"Exited" int4 NULL,
	CONSTRAINT info_bank_pkey PRIMARY KEY (id_tech_bank, "CustomerId")
);

-- "DNF1ED11".info_customer definition

-- Drop table

-- DROP TABLE "DNF1ED11".info_customer;

CREATE TABLE "DNF1ED11".info_customer (
	id_tech_customer varchar NOT NULL,
	"CustomerId" int4 NOT NULL,
	"Geography" varchar(7) NULL,
	"Gender" varchar(6) NULL,
	"Age" int4 NULL,
	CONSTRAINT info_customer_pkey PRIMARY KEY (id_tech_customer, "CustomerId")
);