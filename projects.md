# Ernest Chiu – Projects and Experience

## Experience Summaries

**Unique Device ID Notarization** (Persona, Graph Team; Sep 2022–Jan 2023): Developed a Ruby on Rails + React feature in Persona’s Graph product to fingerprint devices and flag malicious users. This device-­fingerprinting system reduced over 15,000 fraudulent accounts. The Graph product is a link-analysis fraud tool, and Ernest worked closely with Persona’s engineering and product teams on weekly Graph product reviews
withpersona.com
.
**ElasticSearch Graph Query Integration** (Persona; Sep 2022–Jan 2023): Integrated ElasticSearch into Persona’s Graph service to enable real-time search over the data graph. This enhancement allowed instant querying on 45,000+ imported customer data records using ElasticSearch. (Worked as part of the Graph Team.)
**Product Review Pipeline** (Wish API Team; Jan–Apr 2022): Architected and built a Go/Temporal backend pipeline to validate Wish’s merchant product listings. The pipeline processed 12,000+ merchant items for accuracy, improving overall product data quality. (Role: Software Engineer Intern on Wish’s API team.)
**API Rate Limiting System** (Wish; Jan–Apr 2022): Enhanced over 40 merchant-facing Wish API endpoints by adding per-customer rate limiting (implemented in Go). This change reduced Wish’s API server load by ~22%, improving performance under peak traffic.
**External Merchant Integration** (Wish; Jan–Apr 2022): Built a Go microservice to import products from an external ecommerce partner. In collaboration with 3 external engineers, Ernest’s service onboarded 4,000+ new products into Wish, expanding the Wish catalog.
**Authentication Microservice Migration** (Snapcommerce; May–Aug 2021): Developed a central authentication microservice in Golang and gRPC to migrate 650,000+ user accounts from the Snaptravel product to Snapcommerce’s other offerings. This centralized auth service enabled seamless user access across Snapcommerce’s platforms.
**Chatbot Conversation Expansion** (Snapcommerce; May–Aug 2021): Enhanced the Snaptravel chatbot (Python) by adding 20+ new conversation states with internationalization support. These improvements enriched the chat experience for ~300,000 daily users, enabling more dynamic travel-booking conversations.
**RPA Workflow Orchestration** (BorgIQ; Jan–Dec 2020): Implemented an AWS-based workflow system for robotic process automation tasks. Using AWS SQS and Lambda (with Node.js), Ernest automated execution orchestration for BorgIQ’s cloud RPA platform, enabling scalable management of automated business workflows.
**Cloud Storage for RPA Metadata** (BorgIQ; Jan–Dec 2020): Designed and built a Node.js + AWS S3 service to store execution metadata for BorgIQ. This feature allowed users to save 20,000+ assets (logs, data files) related to their RPA executions, supporting audit and traceability of automated processes.
**Pipeline Risk Visualization Dashboard** (JANA Corporation; May–Aug 2019): As part of a 9-person engineering team (Ernest + 8 others), built a GIS-aligned risk dashboard for gas pipeline operators. The web-based tool visualized key risk metrics (e.g. cross-bore hotspots) across 5,000+ pipeline regions in Canada, aiding engineers’ integrity assessment.
**Risk Calculation Algorithm Optimization** (JANA; May–Aug 2019): Optimized a SQL Server–based pipeline risk algorithm for JANA’s integrity software. By analyzing SQL Profiler traces and rewriting queries, Ernest reduced the calculation runtime by 65%, greatly improving update speed for risk models.

## Experience

**Persona** – Software Engineer (Platform Team, July 2023–May 2025)
Persona is a San Francisco–based identity verification startup (valuation ~$2B) whose Graph product is a link-analysis fraud detection tool
withpersona.com

Projects:

### Server-Driven UI Components System

### Project Overview

A revolutionary architectural transformation that migrated complex UI configuration logic from frontend hardcoded implementations to dynamic, server-controlled schemas. This system enables rapid product iteration by allowing UI changes through backend configuration without requiring frontend deployments.

### Technical Architecture

#### Core Component Configuration Engine

- **Dynamic Schema Generation**: Built a sophisticated Ruby-based component configuration system that generates JSON schemas describing UI component properties, validation rules, and behavioral logic
- **Type-Safe Configuration**: Implemented strongly-typed configuration classes with inheritance hierarchies supporting primitive types (text, number, boolean, select, multi-select, date ranges) and complex composite types
- **Runtime Schema Validation**: Created validation layers ensuring configuration integrity and preventing invalid UI states from reaching the frontend

#### Combined Step Configuration System

- **Unified Component Management**: Developed "combined step configs" that logically group related UI components (identity verification, document capture, biometric collection) into cohesive configuration units
- **Inheritance and Composition**: Implemented object-oriented design patterns allowing configuration reuse and extension across similar component types
- **Localization Integration**: Built comprehensive translation management system supporting dynamic text content across multiple languages and regions

#### Backend-Frontend Communication Layer

- **Independent Schema Endpoints**: Designed REST API endpoints that serve component schemas independently from business logic, enabling frontend to dynamically construct UI based on server responses
- **Configuration Add-Ons System**: Created extensible add-on architecture for handling edge cases and component-specific configurations that couldn't be generalized into the main schema system
- **Caching and Performance**: Implemented intelligent caching strategies for schema delivery, reducing API calls and improving UI responsiveness

#### Migration Strategy and Backwards Compatibility

- **Incremental Migration**: Developed feature flag system allowing gradual migration from hardcoded frontend logic to server-driven configurations
- **Dual-Mode Operation**: Built compatibility layer supporting both legacy hardcoded components and new server-driven components during transition period
- **Rollback Mechanisms**: Implemented safety mechanisms allowing instant rollback to frontend-controlled configurations if server-side issues occurred

### Technical Challenges Solved

#### Schema Flexibility vs. Type Safety

- **Challenge**: Balancing flexible configuration capabilities with compile-time type safety
- **Solution**: Developed TypeScript interface generation from Ruby schema definitions, ensuring frontend type safety while maintaining backend flexibility

#### Performance Optimization

- **Challenge**: Preventing UI lag from dynamic schema fetching and parsing
- **Solution**: Implemented schema pre-loading, client-side caching, and progressive schema loading based on user interaction patterns

#### Complex State Management

- **Challenge**: Managing interdependent component configurations where changes to one component affect others
- **Solution**: Built dependency resolution engine that automatically updates related configurations and validates cross-component constraints

### Business Impact

- **Development Velocity**: Reduced UI iteration time from weeks (requiring frontend deployments) to hours (configuration changes only)
- **A/B Testing Capabilities**: Enabled rapid experimentation with different UI flows without code changes
- **Maintenance Efficiency**: Centralized UI logic maintenance in backend, reducing frontend complexity and potential inconsistencies

### Flow Editor Version Diff System

### Project Overview

A comprehensive visual comparison system for complex configuration objects, enabling users to understand differences between versions of multi-layered templates and workflows. The system handles deeply nested data structures with sophisticated visual representations and interactive navigation.

### Technical Architecture

#### Abstract Diff Engine

- **Generic Comparison Framework**: Built extensible diff engine using abstract base classes that can compare arbitrary object types while maintaining semantic understanding of different data structures
- **Deep Object Traversal**: Implemented recursive comparison algorithms that handle nested objects, arrays, and complex relationships while preserving object hierarchy context
- **Change Classification**: Developed intelligent change detection that categorizes modifications as additions, deletions, updates, or moves, with context-aware significance scoring

#### Specialized Differ Implementations

- **Template Structure Differs**: Created specific differ classes for form fields, validation rules, UI flow definitions, and business logic configurations
- **Workflow Step Analysis**: Built workflow-specific comparison logic handling conditional branches, parallel execution paths, and step dependency relationships
- **Component Configuration Diffing**: Implemented component-level comparison for UI elements, including style changes, behavioral modifications, and content updates

#### Visual Representation System

- **Interactive Diff Components**: Developed React-based visualization components with syntax highlighting, expandable/collapsible sections, and side-by-side comparison views
- **Change Navigation**: Built navigation system allowing users to jump between changes, filter by change type, and focus on specific areas of interest
- **Semantic Highlighting**: Implemented intelligent highlighting that emphasizes semantically important changes while de-emphasizing minor formatting or ordering differences

#### Tree-Based Diff Visualization

- **Hierarchical Change Display**: Created tree visualization showing change relationships and impact scope across complex object hierarchies
- **Interactive Exploration**: Built pan/zoom interfaces for navigating large diff trees with performance optimization for massive configuration objects
- **Summary Views**: Developed high-level summary interfaces showing change statistics and impact analysis

### Technical Challenges Solved

#### Recursive Schema Handling

- **Challenge**: Preventing infinite loops when comparing self-referential or cyclical data structures
- **Solution**: Implemented traversal tracking with visited node detection and cycle-breaking algorithms while preserving comparison accuracy

#### Performance with Large Objects

- **Challenge**: Maintaining responsive UI when comparing massive configuration objects with thousands of properties
- **Solution**: Developed streaming diff algorithms, lazy loading for diff sections, and virtualized rendering for large change sets

#### Semantic vs. Syntactic Changes

- **Challenge**: Distinguishing between meaningful business logic changes and irrelevant formatting/ordering changes
- **Solution**: Built semantic analysis layer that understands domain-specific object structures and applies appropriate comparison logic

#### Change Context Preservation

- **Challenge**: Maintaining meaningful context when displaying isolated changes from deeply nested structures
- **Solution**: Implemented breadcrumb navigation and contextual information display showing change location within overall object hierarchy

### Advanced Features

- **Change Impact Analysis**: Built dependency analysis showing how changes in one area affect other parts of the configuration
- **Version History Integration**: Created timeline views showing change evolution across multiple versions
- **Collaboration Features**: Implemented change annotation and commenting system for team review processes

### Case Template Query Editor System

### Project Overview

A sophisticated data querying and analysis platform providing secure, multi-source data access with real-time preview capabilities, comprehensive debugging tools, and advanced query assistance features. The system supports multiple query languages and data sources while maintaining security and performance.

### Technical Architecture

#### Multi-Source Query Engine

- **Database Abstraction Layer**: Built unified query interface supporting SQL databases (Snowflake, PostgreSQL, MySQL) and NoSQL sources with consistent API and error handling
- **Query Translation Layer**: Implemented query dialect translation allowing users to write queries in preferred syntax while automatically adapting to target database requirements
- **Connection Management**: Developed secure connection pooling and credential management system with encryption and access control

#### Schema Introspection System

- **Dynamic Schema Discovery**: Built real-time schema exploration that fetches and caches table structures, column definitions, and relationship information from connected data sources
- **Interactive Schema Browser**: Created searchable, filterable interface for exploring available tables, columns, and data types with auto-completion support
- **Relationship Visualization**: Implemented foreign key relationship mapping and dependency visualization for complex database schemas

#### Variable Substitution Engine

- **Template Processing**: Developed sophisticated variable substitution system supporting dynamic parameter injection with type validation and SQL injection prevention
- **Dependency Management**: Built dependency resolution system tracking variable relationships and automatically updating dependent queries when source variables change
- **Context-Aware Substitution**: Implemented intelligent variable resolution based on query context and available data sources

#### Real-Time Query Execution

- **Sandboxed Execution**: Created secure query execution environment with resource limits, timeout controls, and permission verification
- **Streaming Results**: Implemented streaming result processing for large datasets with progressive loading and memory management
- **Result Transformation**: Built flexible result transformation pipeline supporting data formatting, aggregation, and visualization preparation

#### Advanced Debugging Infrastructure

- **Console Log Capture**: Developed iframe-based execution sandbox with secure parent-child communication for capturing and displaying execution logs
- **Query Performance Analysis**: Implemented query execution plan analysis and performance metrics collection
- **Error Diagnostics**: Built comprehensive error reporting system with contextual information, suggested fixes, and documentation links

### Technical Challenges Solved

#### Security and Isolation

- **Challenge**: Providing powerful querying capabilities while preventing unauthorized data access and SQL injection attacks
- **Solution**: Implemented multi-layered security including query parsing, parameter sanitization, execution sandboxing, and result filtering based on user permissions

#### Performance Optimization

- **Challenge**: Maintaining responsive UI while executing potentially long-running queries against large datasets
- **Solution**: Developed asynchronous query execution with progress indicators, result streaming, and intelligent query optimization suggestions

#### Cross-Database Compatibility

- **Challenge**: Supporting multiple database types with different SQL dialects and capabilities
- **Solution**: Built database-agnostic query abstraction layer with dialect-specific optimization and feature detection

#### Complex Variable Resolution

- **Challenge**: Managing interdependent variables and preventing circular dependencies in template systems
- **Solution**: Implemented dependency graph analysis with cycle detection and intelligent resolution ordering

### Advanced Features

- **Query Version Control**: Built query versioning system with diff visualization and rollback capabilities
- **Collaborative Editing**: Implemented real-time collaborative query editing with conflict resolution
- **Automated Testing**: Created query validation framework with automated testing against sample datasets
- **Performance Monitoring**: Built query performance tracking and optimization recommendation system

### Platform Connections Architecture

### Project Overview

A comprehensive graph-based relationship management system that tracks, visualizes, and manages complex dependencies between platform entities. The system provides deep insights into how different components interconnect and enables impact analysis for changes across the platform.

### Technical Architecture

#### Graph Database Design

- **Adjacency List Implementation**: Built high-performance graph storage using MongoDB with optimized adjacency list structures supporting efficient traversal and relationship queries
- **Node Type Abstraction**: Designed flexible node system supporting heterogeneous object types (templates, workflows, configurations, accounts) with unified relationship modeling
- **Relationship Semantics**: Implemented typed relationships with directionality, strength indicators, and contextual metadata describing connection nature and impact

#### Synchronization Engine

- **Real-Time Sync Processing**: Developed event-driven synchronization system that automatically updates graph relationships when platform objects change
- **Batch Processing**: Built efficient batch synchronization for handling large-scale updates and initial graph construction
- **Conflict Resolution**: Implemented intelligent conflict resolution for concurrent updates and relationship changes

#### Connection Discovery Algorithms

- **Multi-Hop Traversal**: Built sophisticated graph traversal algorithms supporting configurable depth limits, path filtering, and cycle detection
- **Relationship Inference**: Developed algorithms for inferring implicit relationships based on configuration analysis and usage patterns
- **Impact Analysis**: Implemented dependency impact calculation showing how changes propagate through the relationship graph

#### Visualization System

- **Mermaid Diagram Generation**: Created dynamic diagram generation using Mermaid syntax with customizable layouts, styling, and interactive features
- **Interactive Filtering**: Built comprehensive filtering system allowing users to focus on specific relationship types, node categories, or connection strengths
- **Performance Optimization**: Implemented virtualization and progressive loading for large graph visualizations

#### Permission and Security Layer

- **Organization Scoping**: Built multi-tenant architecture ensuring users only see relationships within their organizational boundaries
- **Role-Based Access**: Implemented granular permission system controlling access to different node types and relationship information
- **Data Isolation**: Ensured complete data isolation between organizations while maintaining system performance

### Technical Challenges Solved

#### Scalability with Large Graphs

- **Challenge**: Maintaining performance with graphs containing millions of nodes and relationships
- **Solution**: Implemented graph partitioning, intelligent indexing, and distributed processing for large-scale deployments

#### Real-Time Consistency

- **Challenge**: Maintaining graph consistency during high-frequency updates across distributed systems
- **Solution**: Developed eventually consistent update model with conflict resolution and state reconciliation mechanisms

#### Complex Relationship Modeling

- **Challenge**: Accurately representing diverse relationship types between heterogeneous platform objects
- **Solution**: Built flexible relationship schema supporting typed connections, metadata attributes, and semantic relationship hierarchies

#### Cross-Organization Data Security

- **Challenge**: Preventing information leakage between organizations while maintaining system functionality
- **Solution**: Implemented comprehensive data isolation with organization-scoped queries and encrypted relationship metadata

### Advanced Analytics Features

- **Relationship Strength Analysis**: Built algorithms calculating relationship importance based on usage patterns, configuration dependencies, and business impact
- **Change Impact Prediction**: Developed predictive models showing potential impact of proposed changes across the relationship graph
- **Optimization Recommendations**: Created analysis tools identifying redundant relationships, optimization opportunities, and architectural improvements
- **Historical Relationship Tracking**: Implemented temporal graph capabilities tracking relationship evolution over time

### Performance Optimizations

- **Intelligent Caching**: Built multi-layer caching system for frequently accessed relationship data and traversal results
- **Query Optimization**: Implemented query plan optimization for complex graph traversals with cost-based execution planning
- **Incremental Updates**: Developed incremental synchronization minimizing processing overhead for small changes
- **Parallel Processing**: Built distributed processing capabilities for large-scale graph analysis and synchronization operations

Persona – Software Engineer Intern (Graph Team, Sep 2022–Jan 2023)
Persona is a San Francisco–based identity verification startup (valuation ~$2B) whose Graph product is a link-analysis fraud detection tool
withpersona.com
. Ernest’s role on the Graph Team involved enhancing Persona’s anti-fraud platform. Key contributions included:
Device Fingerprinting: Developed a Ruby on Rails + React feature to notarize device IDs (unique device fingerprints) for each account. This allowed Persona to flag suspicious devices and reduce over 15,000 fraudulent accounts.
Real-Time Search: Integrated ElasticSearch into the Graph service to enable instant querying of the data graph (handles ~45,000 imported records). This provided rapid fraud link discovery and improved the investigator workflow.
Collaborative Reviews: Conducted weekly product review sessions with fellow engineers and product managers to test the Graph UI, identify blockers, and roadmap new features. Through agile sprint planning, Ernest helped prioritize Graph improvements.
Technologies: Ruby on Rails, React, ElasticSearch, PostgreSQL. Worked closely with Persona’s engineering team and PMs on Graph product iterations. (Persona’s Graph tool helps “spot connections between user accounts” to catch fraud
withpersona.com
.)

**Wish** – Software Engineer Intern (API Team, Jan–Apr 2022)
Wish is a popular San Francisco–based e-commerce platform for consumer goods
en.wikipedia.org
. As an API Team intern, Ernest focused on backend services to improve Wish’s merchant product data and API performance. Responsibilities included:

- Product Review Pipeline: Proposed and implemented a Temporal + Go service pipeline to verify merchant product listings. The pipeline checked 12,000+ item listings for accuracy, catching listing errors and improving product quality.
- API Rate Limiting: Enhanced 40+ merchant-facing API endpoints by adding per-customer rate limiting in Go. This throttling system reduced Wish’s API load by ~22%, decreasing server strain during peak shopping periods.
- Merchant Integration: Built a Go microservice to integrate an external partner’s product catalog. In collaboration with 3 external engineers, Ernest’s service onboarded 4,000+ new products into Wish, expanding the marketplace offerings.
  Technologies: Go (Golang), Temporal.io workflow, REST APIs. Collaborated with Wish’s API/Platform engineers and partner teams to design and deploy these features. (Wish is known for visual, low-cost shopping
  en.wikipedia.org
  , and these backend improvements targeted inventory accuracy and scalability.)

### **Snapcommerce (Snaptravel)** – Software Engineer Intern (May–Aug 2021)

Snapcommerce (formerly SnapTravel, now Super.com) is a Toronto‐based startup specializing in travel deals and mobile commerce
betakit.com
. During this internship Ernest built backend services to support Snaptravel’s user platform and chatbot. Highlights:

- Authentication Microservice: Developed a Golang + gRPC service to migrate 650,000+ Snaptravel user accounts into a central auth system across Snapcommerce’s products. This migration unified login for all Snaptravel users.
- Chatbot Conversation Expansion: Enhanced the Snaptravel chatbot (Python) by adding 20+ new conversation states and internationalization support. This enriched dialogues for ~300,000 daily users, enabling multi-lingual itineraries and inquiries.
  Technologies: Go, gRPC, Python, REST. Worked on a small engineering team in Toronto. (Snapcommerce’s flagship was SnapTravel, a travel deals SMS/chat app
  betakit.com
  .)

### **BorgIQ** – Software Engineer Intern (Jan–Dec 2020)

BorgIQ is a Toronto startup providing cloud-based Robotic Process Automation (RPA) solutions to automate routine business tasks
borgiq.com
. In this role, Ernest contributed to the core RPA platform:

- RPA Workflow System: Designed and implemented a new orchestration layer for RPA jobs using AWS SQS and Lambda. This microservices-based workflow managed task queues and execution flows, enabling users to define complex automation pipelines.
- Cloud Metadata Storage: Built a Node.js + AWS S3 service to store execution metadata and assets. This system archived over 20,000 execution artifacts (logs, screenshots) for user robot runs, allowing BorgIQ users to review and audit automated tasks.
  Technologies: Node.js, AWS (Lambda, SQS, S3). Collaborated with the BorgIQ dev team and CTO to integrate these features into the RPA cloud platform
  borgiq.com
  .

### **JANA Corporation** – Software Developer Intern (May–Aug 2019)

JANA Corporation is a Canadian company that provides predictive risk modeling and integrity management software for natural gas pipeline operators
janacorporation.com
. As a developer intern, Ernest worked on pipeline risk analytics tools:

- Risk Visualization Dashboard: Collaborated with 8 other engineers to build a GIS-based web dashboard that visualized pipeline cross-bore hotspots and risk metrics over 5,000+ regions. The dashboard helped engineers inspect pipeline integrity graphically.
- Algorithm Optimization: Analyzed and optimized a SQL Server–based pipeline risk algorithm for JANA’s integrity software. By profiling queries and rewriting the core algorithm, Ernest cut computation time by 65%, enabling faster risk updates.
  Technologies: SQL Server, .NET/JavaScript (front-end), geospatial mapping. Worked within JANA’s engineering team to improve analytics performance

## Personal Projects

### Capsule Budget Tracking App (Personal Project; Jun 2019–Jun 2020)

Created Capsule, a MERN-stack (MongoDB, Express, React, Node.js) web app for budgeting. Capsule tracked 3,000+ monthly user expenses, persisting transaction data via Mongoose/MongoDB for 20+ users. (Solo project: designed frontend, backend, and database storage.)
