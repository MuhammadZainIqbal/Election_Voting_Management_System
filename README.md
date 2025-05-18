# Election Voting Management System

![C++](https://img.shields.io/badge/Language-C%2B%2B-green)
![Version](https://img.shields.io/badge/version-1.0.0-orange)

A comprehensive C++ console-based application for managing election processes, voter registrations, candidate management, and vote tabulation.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [System Architecture](#system-architecture)
- [User Roles](#user-roles)
- [Installation](#installation)
- [Getting Started](#getting-started)
- [File Structure](#file-structure)
- [Development](#development)
- [Limitations & Future Enhancements](#limitations--future-enhancements)
- [Contributing](#contributing)

## Overview

The Election Voting Management System (EVMS) is a console-based C++ application designed to manage and streamline the election process. The system provides secure interfaces for presiding officers, voters, and election candidates, allowing for comprehensive management of the electoral process including voter registration, candidate management, vote casting, and result tabulation. The system employs regional division of constituencies for better organization and management.

## Features

### Core Features

- **User Authentication**: Secure login for presiding officers, voters, and election candidates
- **Role-based Access Control**: Different interfaces for different user types
- **Color-coded UI**: Enhanced visual experience with color-coded menus
- **Data Persistence**: File-based storage for all voter and candidate information

### Presiding Officer Features

- Add and remove voters from the electoral roll
- Add and remove candidates from the electoral ballot
- View complete voter lists (overall and region-specific)
- View complete candidate lists (overall and region-specific)
- View election results

### Voter Features

- Secure authentication using unique credentials
- View personal voter information
- View candidate information
- Cast vote (one vote per voter)
- Check voting status

### Candidate Features

- Secure authentication using unique credentials
- View personal candidate information
- Check vote count for self
- View voter lists from their region

## System Architecture

The system follows an object-oriented architecture with the following class structure:

- **User Class (Base Class)**: Contains common attributes for all users including name, ID card, age, etc.
- **PO Class (Derived from User)**: Represents Presiding Officers with additional attributes and functionalities
- **Voter Class (Derived from User)**: Represents Voters with vote-specific attributes
- **Candidate Class (Derived from User)**: Represents Election Candidates with party and vote count attributes
- **Login Class (Derived from User)**: Handles authentication for all user roles
- **Menu Class (Derived from Login)**: Manages the various menu interfaces for different user roles

## User Roles

### Presiding Officer
Administrators with full system access. Default credentials:  
- Username: `asim`  
- Password: `1122`

### Voter
Regular citizens eligible to cast votes. Voters are organized by regions (1, 2, or 3) and must register with valid credentials including ID card details.

### Candidate
Election contestants representing political parties. Candidates also belong to specific regions and represent particular political parties (e.g., PMLN, PTI).

## Installation

### Prerequisites
- C++ compiler (GCC/G++ recommended)
- Basic understanding of terminal/command prompt usage

### Steps to Install
1. Clone this repository or download the source code.
2. Navigate to the source directory using terminal or command prompt.
3. Compile the code using the following command:

```bash
g++ -o EVMS EVMS.cpp
```

4. Run the executable:

```bash
./EVMS  # On Linux/Mac
EVMS.exe  # On Windows
```

## Getting Started

### First Time Setup
1. Start the application by running the executable
2. Login as the Presiding Officer using the default credentials:
   - Username: `asim`
   - Password: `1122`
3. Add voters and candidates using the Presiding Officer menu
4. Exit and restart the application to allow voters and candidates to login and use the system

### Sample Workflow
1. **Presiding Officer**:
   - Add voters and candidates
   - Manage electoral rolls by region
   - View comprehensive system data

2. **Voters**:
   - Login with assigned credentials
   - View their information
   - View candidate information
   - Cast their vote for a preferred candidate
   - Check their voting status

3. **Candidates**:
   - Login with assigned credentials
   - View their campaign information
   - Check vote counts
   - View voter lists from their region

## File Structure

The system uses the following files to store and manage data:

- `voterdata.txt`: Stores information about registered voters including login credentials
- `candidatedata.txt`: Stores information about election candidates including party affiliations
- `voterids.txt`: Tracks voter IDs for integrity checks
- `candidatesids.txt`: Tracks candidate IDs for integrity checks
- `podata.txt`: Stores presiding officer data
- `poids.txt`: Tracks presiding officer IDs

## Development

### Tech Stack
- Language: C++
- Data Storage: Text-based file system
- UI: Console-based with ANSI color formatting

### Code Structure
The codebase follows an object-oriented approach with inheritance hierarchies and separation of concerns:

- **User Management**: Handles user registration, authentication, and information management
- **Election Management**: Manages candidate registration and vote tabulation
- **Menu System**: Provides role-specific interfaces and navigation
- **Data Persistence**: Handles file I/O operations for data storage and retrieval

## Limitations & Future Enhancements

### Current Limitations
- Console-based interface with limited visual appeal
- Text file-based storage without database security
- Limited scalability for large-scale elections
- Some features like vote casting are partially implemented

### Planned Enhancements
- Implement full vote casting and result tabulation functionality
- Add database support for more secure and scalable data storage
- Develop a graphical user interface (GUI) for improved usability
- Implement advanced security features including encryption
- Add audit trails and logging functionality
- Support for multiple simultaneous elections
- Enhanced reporting and analytics

## Contributing

Contributions to improve the Election Voting Management System are welcome. Please follow these steps:

1. Fork the repository  
2. Create a feature branch (`git checkout -b feature/amazing-feature`)  
3. Commit your changes (`git commit -m 'Add some amazing feature'`)  
4. Push to the branch (`git push origin feature/amazing-feature`)  
5. Open a Pull Request  

---

© 2025 Election Voting Management System | Developed as a demonstration of object-oriented programming principles in C++
