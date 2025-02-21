# React Native FlatList/SectionList: KeyExtractor Unique Key Violation

This repository demonstrates a common yet subtle bug in React Native's FlatList and SectionList components: the use of non-unique keys in the `keyExtractor` function.

## The Problem

The `keyExtractor` function is crucial for efficient rendering and data management within FlatList and SectionList. It must provide a unique key for *every* item in the data array.  If duplicate keys are used, React Native's rendering mechanism can become confused, leading to unexpected behavior such as:

* Items not updating correctly.
* Items disappearing randomly.
* Poor performance.

## How to Reproduce

The `bug.js` file demonstrates the problematic code. Run the app and observe the inconsistencies in item rendering.

## Solution

The `bugSolution.js` file shows the corrected code. The solution is to ensure that the `keyExtractor` function always returns unique keys, such as using a combination of fields or generating unique identifiers (UUIDs).