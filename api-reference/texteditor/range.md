# Range

A range represents an ordered pair of two positions and is used to reference an area of text inside of a TextEditor object. Range objects are **immutable**.

## Constructor

`new Range(start:` [`Position`](position.md)`, end:` [`Position`](position.md)`):` [`Range`](range.md)``

## Properties



<details>

<summary>end: <a href="position.md">Position</a></summary>



</details>

<details>

<summary>isEmpty: boolean</summary>



</details>

<details>

<summary>isSingleLine: boolean</summary>



</details>

<details>

<summary>length: number</summary>



</details>

<details>

<summary>start: <a href="position.md">Position</a></summary>



</details>

## Methods

<details>

<summary>isEqual(other: <a href="range.md">Range</a>): boolean</summary>

Returns <mark style="color:blue;">true</mark> if the specified range is equal to the range instance, else <mark style="color:blue;">false</mark>.

</details>

<details>

<summary>contains(positionOrRange: <a href="position.md">Position</a> | <a href="range.md">Range</a>): boolean</summary>

Returns <mark style="color:blue;">true</mark> or <mark style="color:blue;">false</mark> depending on if a specified position or range is contained within the range instance.

</details>

<details>

<summary>intersection(range: <a href="range.md">Range</a>): <a href="range.md">Range</a> | undefined</summary>

Returns a new <mark style="color:blue;">range</mark> object representing the portion of the specified range that overlaps (intersects) the range instance. <mark style="color:blue;">Undefined</mark> is returned if the compared ranges do not overlap.

</details>

<details>

<summary>union(other: <a href="range.md">Range</a>): <a href="range.md">Range</a></summary>

Returns a new <mark style="color:blue;">range</mark> representing the combination (union) of the specified range and the range instance.

</details>

<details>

<summary>with(start?: <a href="position.md">Position</a>, end?: <a href="position.md">Position</a>): <a href="range.md">Range</a></summary>

Returns a new range derived from the range instance and the specified start or end parameter.

</details>

## Examples
