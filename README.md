# A basic concept on YAML

**Before starting with YAML here is some concept of serialization**

## **SERIALIZATION**
---------------------
It is a process of translating data structure/object in a format for storage purpose. The storage format later can be used to reconstruct into original object. The bits order in serialization can be used to create semantically identical clone. Marshalling is the process of object serialization. **Deserialization** is extracting a data structure from a series of bytes, opposite of serialization.

## **Uses of Serialization:**
==============================

1. Transferring data through wire
2. Storing data
3. Remote procedure calls (ex: SOAP)
4. Detecting changes in time varying data.

***Serialization mainly helps data structure to be architecture-independent format for storing, transferring or other uses among different programming languages. It also helps in byte-ordering, memory layout and provides simple different ways of representing data.***

## **Limitations:**
====================

It breaks opacity of the abstract data types by exposing implementation details. Other way, it violates encapsulation.

