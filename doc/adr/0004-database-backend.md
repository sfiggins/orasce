# 4. database backend

Date: 2020-08-25

## Status

Accepted

## Context

Using a database is a requirement of this project. While this is small and
could likely get by with some sqlite, I want to exercise some of my ability to
create and network Docker containers. So I want to choose a data backend that
will run in its own process. This could be an SQL or no-SQL solution. There
isn't any real need for relational data for this project. The persistent
information can fit in a single table.

## Decision

Use Postgresql.

This is way more than this project needs, but it is the database with which I
am most familiar. I dont' want to make the database I use to distract from
learning and implementing the necessary elements of this project. 

Another factor in this choice is documentation. Most documentation and
tutorials that use an SQL backend use Postgresql. So there are plenty of
examples to draw from.


## Consequences

I will use a system with which I am already familiar. Postgresql is well
documented in go-lang tutorials. 
