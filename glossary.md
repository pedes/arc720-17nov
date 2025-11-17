# API Integration Glossary for Insurance Platform

## Core API Concepts

**API (Application Programming Interface)**
A set of protocols and specifications that allows different software systems to communicate and exchange data with each other.

**REST API (Representational State Transfer)**
An architectural style for APIs that uses HTTP methods (GET, POST, PUT, DELETE) and stateless communication. Most common pattern for synchronous integrations.

**Endpoint**
A specific URL where an API can be accessed, representing a particular resource or operation (e.g., `/api/v1/policies`).

**API Contract**
The formal specification defining how an API should behave, including request/response formats, data types, and business rules. Often documented using OpenAPI/Swagger.

**Payload**
The actual data transmitted in an API request or response body, typically in JSON or XML format.

## Integration Patterns

**Synchronous Communication**
Real-time request-response pattern where the client waits for the server to process and return a response before proceeding.

**Asynchronous Communication**
Fire-and-forget or event-driven pattern where the sender doesn't wait for immediate response. Used for long-running processes or decoupled systems.

**Pub/Sub (Publish-Subscribe)**
Messaging pattern where publishers send messages to topics/channels, and subscribers receive messages they're interested in without direct coupling.

**Event-Driven Architecture**
Design pattern where system components react to events (state changes or notifications) rather than direct API calls.

**Point-to-Point Integration**
Direct connection between two systems, typically tightly coupled and less scalable.

**Hub-and-Spoke Architecture**
Integration pattern where a central hub (like MuleSoft) manages all connections to various systems (spokes), reducing integration complexity.

## MuleSoft-Specific Terms

**Anypoint Platform**
MuleSoft's complete integration platform including API management, design, implementation, and monitoring capabilities.

**Mule Runtime**
The lightweight Java-based engine that executes integration applications and processes API calls.

**API-Led Connectivity**
MuleSoft's architectural approach organizing APIs into three layers: Experience, Process, and System APIs.

**Experience API**
Top layer providing tailored data and functionality for specific user experiences or channels (mobile, web, partner portals).

**Process API**
Middle layer orchestrating business processes and logic, often combining data from multiple system APIs.

**System API**
Bottom layer providing direct access to core systems of record (like Salesforce, policy admin systems, claims systems).

**Mule Flow**
The sequence of message processors that handle API requests and transformations within a Mule application.

**DataWeave**
MuleSoft's expression language for transforming data between different formats (JSON to XML, etc.).

**Connector**
Pre-built module in MuleSoft for integrating with specific systems (Salesforce Connector, Database Connector, etc.).

**API Manager**
MuleSoft component for governing APIs, applying policies, managing access, and monitoring usage.

**CloudHub**
MuleSoft's cloud-based integration Platform as a Service (iPaaS) for deploying and running integration applications.

## Salesforce-Specific Terms

**Salesforce Object**
Standard or custom data structures in Salesforce (Account, Contact, Policy__c, Claim__c).

**SOQL (Salesforce Object Query Language)**
SQL-like query language for retrieving data from Salesforce.

**Platform Events**
Salesforce's pub/sub messaging service for event-driven integrations within and outside Salesforce.

**Apex REST Services**
Custom REST APIs built using Salesforce's Apex programming language.

**External Services**
Salesforce feature allowing declarative integration with external REST APIs.

**Connected App**
OAuth-based authentication mechanism for external applications to securely access Salesforce.

**Change Data Capture (CDC)**
Salesforce feature that publishes change events when records are created, updated, deleted, or undeleted.

## Security & Authentication

**OAuth 2.0**
Industry-standard authorization framework used for secure API access without sharing credentials.

**JWT (JSON Web Token)**
Compact token format for securely transmitting information between parties, commonly used for authentication.

**API Key**
Simple authentication method using a unique identifier to control API access.

**mTLS (Mutual Transport Layer Security)**
Two-way authentication where both client and server verify each other's certificates.

**Client Credentials Flow**
OAuth flow for server-to-server authentication without user interaction.

**API Gateway**
Entry point for all API traffic, handling authentication, rate limiting, and routing.

## Data & Message Formats

**JSON (JavaScript Object Notation)**
Lightweight data-interchange format, most common for modern REST APIs.

**XML (eXtensible Markup Language)**
Markup language for encoding documents, still common in legacy insurance systems.

**Schema**
Formal definition of data structure, constraints, and validation rules.

**Canonical Data Model**
Standardized internal data format used within the integration layer to reduce transformation complexity.

## Asynchronous Messaging

**Message Queue**
System for storing messages temporarily until they can be processed by receiving applications.

**Message Broker**
Middleware that routes messages between producers and consumers (e.g., Apache Kafka, RabbitMQ, AWS SQS).

**Dead Letter Queue (DLQ)**
Repository for messages that couldn't be processed successfully after multiple attempts.

**Idempotency**
Property ensuring an operation produces the same result regardless of how many times it's executed.

**Message Acknowledgment**
Confirmation from consumer that a message was successfully received and processed.

**Polling**
Regularly checking for new data or messages at defined intervals.

**Webhook**
HTTP callback triggered by an event, allowing real-time push notifications instead of polling.

## Insurance Domain Terms

**Policy Administration System (PAS)**
Core system managing insurance policy lifecycle (quotes, issuance, renewals, endorsements).

**Claims Management System**
System handling claim submission, adjudication, and payment processes.

**Rating Engine**
System calculating insurance premiums based on risk factors and underwriting rules.

**Underwriting**
Process of evaluating risk and determining policy terms and pricing.

**Quote-to-Cash**
End-to-end business process from initial quote through policy issuance to premium collection.

**ACORD**
Insurance industry standards organization; ACORD XML is common format for insurance data exchange.

## API Management & Governance

**API Versioning**
Strategy for managing changes to APIs while maintaining backward compatibility (v1, v2, etc.).

**Rate Limiting**
Controlling the number of API requests a client can make in a time period.

**API Throttling**
Slowing down request processing when limits are approached to prevent system overload.

**SLA (Service Level Agreement)**
Guaranteed performance metrics for API availability, response time, and throughput.

**API Policy**
Configurable rules applied to APIs (security, logging, transformation, caching).

**API Analytics**
Monitoring and reporting on API usage, performance, errors, and trends.

## Integration Quality & Operations

**Circuit Breaker**
Pattern that prevents cascading failures by stopping requests to failing services temporarily.

**Retry Logic**
Automatic re-attempt of failed operations with exponential backoff strategies.

**Timeout**
Maximum time allowed for an API operation before it's considered failed.

**Error Handling**
Systematic approach to catching, logging, and responding to integration failures.

**Monitoring & Alerting**
Real-time tracking of integration health with notifications for anomalies or failures.

**Transaction**
Logical unit of work that must be completed fully or rolled back entirely (ACID properties).

**Compensation**
Process of undoing completed steps when a distributed transaction fails partway through.

This glossary covers the essential concepts for your insurance integration project using MuleSoft and Salesforce. Would you like me to expand on any specific area or add additional domain-specific terms?
