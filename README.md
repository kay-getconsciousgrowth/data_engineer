# Data Engineer

```
create table transaction_table(
	transaction_index char(5) primary key,
	channel varchar(40),
	date_created date,
	revenue float
);

create table month_table(
	month_index char(5) primary key,
	year_month integer not null,
	month_start_date date not null,
	month_end_date date not null
);

insert into transaction_table values ('00001', 'facebook', '2021-01-01', 1000);
insert into transaction_table values ('00002', 'facebook', '2021-01-01', 2000);
insert into transaction_table values ('00003', 'facebook', '2021-01-02', 2500);
insert into transaction_table values ('00004', 'facebook', '2021-01-02', 300);
insert into transaction_table values ('00005', 'facebook', '2021-01-02', 600);
insert into transaction_table values ('00006', 'google', '2021-01-02', 10000);
insert into transaction_table values ('00007', 'google', '2021-01-06', 30000);
insert into transaction_table values ('00008', 'facebook', '2021-02-01', 200);
insert into transaction_table values ('00009', 'facebook', '2021-02-02', 250);
insert into transaction_table values ('00010', 'facebook', '2021-02-02', 30);
insert into transaction_table values ('00011', 'facebook', '2021-02-02', 60);
insert into transaction_table values ('00012', 'google', '2021-02-02', 1000);
insert into transaction_table values ('00013', 'google', '2021-02-06', 3000);
insert into transaction_table values ('00014', 'facebook', '2021-03-01', 1200);
insert into transaction_table values ('00015', 'facebook', '2021-03-02', 1250);
insert into transaction_table values ('00016', 'facebook', '2021-03-02', 130);
insert into transaction_table values ('00017', 'facebook', '2021-04-01', 12500);
insert into transaction_table values ('00018', 'facebook', '2021-04-02', 12550);
insert into transaction_table values ('00019', 'google', '2021-04-02', 11000);
insert into transaction_table values ('00020', 'google', '2021-04-06', 33000);

insert into month_table values ('00001', 202011, '2020-11-01', '2020-11-30');
insert into month_table values ('00002', 202012, '2020-12-01', '2020-12-31');
insert into month_table values ('00003', 202101, '2021-01-01', '2021-01-31');
insert into month_table values ('00004', 202102, '2021-02-01', '2021-02-28');
insert into month_table values ('00005', 202103, '2021-03-01', '2021-03-31');
insert into month_table values ('00006', 202104, '2021-04-01', '2021-04-30');
```

Using the above table(s), compose a SQL query that produces monthly revenue by channel and the previous month's revenue.
