# HBnB EVOLUTION - Technical Documentation Project

## Table of Contents
1. [Project Overview](#project-overview)
2. [Context and Objectives](#context-and-objectives)
3. [Problem Description](#problem-description)
4. [Business Rules and Requirements](#business-rules-and-requirements)
5. [Architecture and Layers](#architecture-and-layers)
6. [Tasks](#tasks)
   - [Task 0: High-Level Package Diagram](#task-0-high-level-package-diagram)
   - [Task 1: Detailed Class Diagram for Business Logic Layer](#task-1-Business-Logic-Layer)
   - [Task 2: Sequence Diagrams for API Calls](#task-2-API-Interaction-FLow)
   - [Task 3: Documentation Compilation](#task-3-documentation-compilation)
7. [Conditions and Constraints](#conditions-and-constraints)
8. [Resources](#resources)
9. [Expected Outcome](#expected-outcome)
10. [Diagram Types](#diagram-types)

## Project Overview

HBnB is a technical documentation project aimed at creating comprehensive documentation for the HBnB (Holiday Booking and Beyond) Evolution application. This project focuses on designing and documenting the architecture and core components of a simplified AirBnB-like system.

## Context and Objectives

As part of the initial phase of the HBnB Evolution application development, this project focuses on creating detailed technical documentation. The primary objectives are:

1. To develop a clear understanding of the overall architecture.
2. To design and document the detailed business logic.
3. To illustrate the interactions within the system.

This documentation will serve as the foundation for the subsequent development phases of the HBnB Evolution application.

## Problem Description

The HBnB Evolution application is designed to provide the following primary functionalities:

1. **User Management**: Allow users to register, update profiles, and be identified as regular users or administrators.
2. **Place Management**: Enable users to list properties they own, including details such as name, description, price, location, and associated amenities.
3. **Review Management**: Allow users to leave reviews for places they've visited, including ratings and comments.
4. **Amenity Management**: Manage amenities that can be associated with places.

## Business Rules and Requirements

### User Entity
- Attributes: first name, last name, email, password
- Administrator status determined by a boolean attribute
- Operations: register, update profile, delete account

### Place Entity
- Attributes: title, description, price, latitude, longitude
- Associated with an owner (User)
- Can have multiple amenities
- Operations: create, update, delete, list

### Review Entity
- Associated with a specific Place and User
- Includes rating and comment
- Operations: create, update, delete, list by place

### Amenity Entity
- Attributes: name, description
- Operations: create, update, delete, list

### General Requirements
- All entities must have a unique identifier (UUID4)
- Creation and update datetimes must be recorded for all entities for auditing purposes

## Architecture and Layers

The application follows a three-layer architecture:

1. **Presentation Layer**: Includes services and API for user interaction
2. **Business Logic Layer**: Contains models and core application logic
3. **Persistence Layer**: Responsible for data storage and retrieval

## Tasks

### Task 0: High-Level Package Diagram

Create a high-level package diagram illustrating the three-layer architecture and the communication between layers via the facade pattern.

**Deliverables:**
- High-level package diagram
- Explanatory notes describing each layer and the facade pattern implementation

### Task 1: Business Logic Layer

Design a comprehensive class diagram for the Business Logic layer, focusing on User, Place, Review, and Amenity entities.

**Deliverables:**
- Detailed class diagram
- Explanatory notes for each entity and their relationships

### Task 2: API Interaction Flow

Develop sequence diagrams for at least four different API calls to demonstrate the interaction between layers and information flow.

**Suggested API calls:**
1. User registration
2. Place creation
3. Review submission
4. Fetching a list of places

**Deliverables:**
- Four sequence diagrams
- Explanatory notes for each API call flow

### Task 3: Documentation Compilation

Compile all diagrams and explanatory notes into a comprehensive technical document.

**Deliverables:**
- Complete technical documentation including all diagrams and explanations
- Introduction and overview of the HBnB project
- Structured sections for each component of the architecture

## Conditions and Constraints

- All diagrams must clearly represent interactions and data flow between different layers
- Use UML notation for all diagrams to ensure consistency and clarity
- Accurately reflect the business rules and requirements in the diagrams
- Provide sufficient detail in the diagrams to guide the implementation phase

## Resources

- UML Basics: [Concept Page] OOP - Introduction to UML
- Package Diagrams: UML Package Diagram Overview, UML Package Diagrams Guide
- Class Diagrams: UML Class Diagram Tutorial, How to Draw UML Class Diagrams
- Sequence Diagrams: UML Sequence Diagram Tutorial, Understanding Sequence Diagrams
- Diagram Tools: Mermaid.js Documentation, draw.io

## Expected Outcome

By the end of this project, you should have a complete set of technical documentation that provides a clear and detailed blueprint for the HBnB Evolution application. This documentation will guide the implementation phases and ensure a solid understanding of the application's design and architecture.

## Diagram Types

1. **Package Diagram**: Used for the high-level architecture representation (Task 0)
2. **Class Diagram**: Used for detailed representation of the Business Logic Layer (Task 1)
3. **Sequence Diagram**: Used to illustrate API call flows and interactions between layers (Task 2)
