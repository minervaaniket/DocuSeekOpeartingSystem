# DocuSeekOpeartingSystem # WhatsApp HR Assistant

## Overview
This is a Flask-based WhatsApp bot that serves as an HR assistant, allowing employees to interact with HR systems via WhatsApp messages and voice notes. The bot integrates with an external HR API to provide various HR-related functionalities.

## Key Features

### Authentication & Authorization
- Validates users via phone number against employee records
- Supports different employee types (regular, manager, HR) with appropriate access levels

### Attendance Management
- Mark attendance (PRESENT/ABSENT/WFH) for current or specific dates
- View attendance records with calendar visualization
- Check today's attendance status

### Leave & WFH Requests
- Submit leave/WFH requests via natural language ("leave from 2023-12-01 to 2023-12-05")
- View request history and status
- Handle leave conflicts and balance information

### Approval Workflows
- Managers can view pending approval requests
- Approve/reject requests via simple commands
- Track request status changes

### Multimedia Support
- Voice note processing (speech-to-text)
- Audio responses (text-to-speech)
- File handling for audio messages

### Advanced Features for Managers
- Custom SQL query execution (for authorized roles)
- Comprehensive employee data access

## Technical Implementation

### Core Technologies
- Flask web framework
- Twilio WhatsApp API integration
- Google Speech Recognition (speech-to-text)
- gTTS (text-to-speech)
- RESTful API communication with HR systems

### Security
- API key authentication
- Employee authorization checks
- Input validation for all commands

### Error Handling
- Comprehensive error checking for API calls
- Graceful fallbacks for failed operations
- Input validation for dates and commands

## Usage Examples
- "Present" - Mark today as present
- "WFH 2023-12-15" - Mark WFH for specific date
- "Leave from 2023-12-01 to 2023-12-03" - Submit leave request
- "My attendance from 2023-12-01 to 2023-12-31" - View attendance calendar
- "Accept request 123" - Approve a pending request

## Setup Requirements
- Python 3.x with required packages (Flask, requests, pydub, etc.)
- Twilio account credentials
- Access to HR API endpoint
- Environment variables configuration

The bot provides a natural language interface to complex HR systems, making HR processes accessible directly through WhatsApp with both text and voice interaction capabilities.
