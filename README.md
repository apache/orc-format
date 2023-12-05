<!--
  - Licensed to the Apache Software Foundation (ASF) under one
  - or more contributor license agreements.  See the NOTICE file
  - distributed with this work for additional information
  - regarding copyright ownership.  The ASF licenses this file
  - to you under the Apache License, Version 2.0 (the
  - "License"); you may not use this file except in compliance
  - with the License.  You may obtain a copy of the License at
  -
  -   http://www.apache.org/licenses/LICENSE-2.0
  -
  - Unless required by applicable law or agreed to in writing,
  - software distributed under the License is distributed on an
  - "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
  - KIND, either express or implied.  See the License for the
  - specific language governing permissions and limitations
  - under the License.
  -->

# [Apache ORC](https://orc.apache.org/)

ORC is a self-describing type-aware columnar file format designed for
Hadoop workloads. It is optimized for large streaming reads, but with
integrated support for finding required rows quickly. Storing data in
a columnar format lets the reader read, decompress, and process only
the values that are required for the current query. Because ORC files
are type-aware, the writer chooses the most appropriate encoding for
the type and builds an internal index as the file is written.
Predicate pushdown uses those indexes to determine which stripes in a
file need to be read for a particular query and the row indexes can
narrow the search to a particular set of 10,000 rows. ORC supports the
complete set of types in Hive, including the complex types: structs,
lists, maps, and unions.

## ORC Format

This project includes ORC specification and the protobuf definitions

Releases:
* Latest: <a href="http://orc.apache.org/releases">Apache ORC releases</a>
* Maven Central: <a href="http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22org.apache.orc%22">![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.apache.orc/orc/badge.svg)</a>
* Downloads: <a href="http://orc.apache.org/downloads">Apache ORC downloads</a>
* Release tags: <a href="https://github.com/apache/orc/releases">Apache ORC release tags</a>
* Plan: <a href="https://github.com/apache/orc/milestones">Apache ORC future release plan</a>

The current build status:
* Main branch <a href="https://github.com/apache/orc/actions/workflows/build_and_test.yml?query=branch%3Amain">
  ![main build status](https://github.com/apache/orc/actions/workflows/build_and_test.yml/badge.svg?branch=main)</a>

Bug tracking: <a href="http://orc.apache.org/bugs">Apache Jira</a>

## Building

```
./mvnw install
```
