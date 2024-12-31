# Hospital Management System

## Overview
The Hospital Management System is a Python-based application that allows you to manage hospital-related data. It integrates with MySQL to handle patient, doctor, and appointment details. The system enables the user to add, update, delete, and view data for doctors, patients, and appointments.

This project is designed to streamline hospital data management and make administrative tasks more efficient by automating records and providing a simple interface for interacting with the data.

## Features
- **Patient Management**: 
  - Add, update, remove, and view patient details.
  - Includes patient number, name, mobile number, address, and room number.
  
- **Doctor Management**: 
  - Add, update, remove, and view doctor details.
  - Includes doctor number, name, department, mobile number, and address.
  
- **Appointment Management**:
  - Schedule, remove, and view appointments between patients and doctors.
  - Includes appointment number, patient name, doctor name, mobile number, and address.

## Requirements
- **Python 3.x**: The system is built using Python.
- **MySQL Server**: Used as the backend database to store data.
- **MySQL Connector for Python**: Required to connect Python with MySQL.

## Installation Instructions

### Step 1: Install MySQL
1. Download and install MySQL Server from the [official MySQL downloads page](https://dev.mysql.com/downloads/installer/).
2. Set up MySQL on your machine and create a new database.

### Step 2: Create Database and Tables
After installing MySQL, log in to the MySQL console and create a new database named `hospital`. Use the following SQL commands to create the necessary tables for patients, doctors, and appointments.

```sql
CREATE DATABASE hospital;

USE hospital;

CREATE TABLE patient (
  P_no INT PRIMARY KEY,
  Name VARCHAR(100),
  Mobile_no VARCHAR(15),
  Address VARCHAR(255),
  Room_number VARCHAR(20)
);

CREATE TABLE doctor (
  S_no INT PRIMARY KEY,
  Name VARCHAR(100),
  Department VARCHAR(50),
  Mobile_no VARCHAR(15),
  Address VARCHAR(255)
);

CREATE TABLE appointment (
  A_no INT PRIMARY KEY,
  Patient_Name VARCHAR(100),
  Doctor_Name VARCHAR(100),
  Mobile_no VARCHAR(15),
  Address VARCHAR(255)
);
