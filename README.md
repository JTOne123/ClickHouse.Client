# ClickHouse.Client

ADO.NET client for [ClickHouse](https://github.com/ClickHouse/ClickHouse), ultra-fast 'big data' relational database

[![License](https://img.shields.io/github/license/DarkWanderer/ClickHouse.Client?style=for-the-badge)](https://github.com/DarkWanderer/ClickHouse.Client/blob/master/LICENSE)
[![NuGet status](https://img.shields.io/nuget/dt/ClickHouse.Client?style=for-the-badge)](https://www.nuget.org/packages/ClickHouse.Client/)
[![Build status](https://img.shields.io/appveyor/build/DarkWanderer/clickhouse-client/master?style=for-the-badge)](https://ci.appveyor.com/project/DarkWanderer/clickhouse-client/branch/master)
[![Tests status](https://img.shields.io/appveyor/tests/DarkWanderer/clickhouse-client/master?style=for-the-badge)](https://ci.appveyor.com/project/DarkWanderer/clickhouse-client/branch/master)

## Why another client?

Compared to other existing .NET clients, `ClickHouse.Client` has following advantages 
* Does not have to buffer response, reducing memory usage
* Is version-agnostic
* Offers wider support for ClickHouse-specific types
* Is more compliant to ADO.NET standards (e.g. does not require calling 'NextResult' on `SELECT` queries)

## Key features

* Uses HTTP(S), so is compatible with any server version
* Uses fast row-based binary protocol for communication
* Fully supports ClickHouse-specific types:
  * Composite types: `Array`, `Tuple`, `Nullable`, `Nested`, including combinations
  * Specialized types: `IPv4`, `IPv6`, `UUID`, `DateTime64`, `LowCardinality`, `Enum` etc.
* High-throughput
* Available for .NET Core/Framework/Standard
* Supports [bulk insertion](https://github.com/DarkWanderer/ClickHouse.Client/wiki/Bulk-insertion)
