# SmartSplines:

### Namespace:
Kitbashery.SmartGO

## Methods:

| Method | Summary | Parameters | Returns |
| --- | --- | --- | --- |
| CalculateBezierPoint |  | `Single` t, `Vector3` p0, `Vector3` p1, `Vector3` p2, `Vector3` p3 | `Vector3` |
| CalculateHermitePoint |  | `Single` t, `Vector3` p0, `Vector3` p1, `Vector3` m0, `Vector3` m1 | `Vector3` |
| CalculateCatmullRomPoint |  | `Single` t, `Vector3` p0, `Vector3` p1, `Vector3` p2, `Vector3` p3 | `Vector3` |
| CalculateBSplinePoint |  | `Single` t, `Vector3` p0, `Vector3` p1, `Vector3` p2, `Vector3` p3 | `Vector3` |
| CalculateLinearPoint |  | `Single` t, `Vector3` p0, `Vector3` p1 | `Vector3` |
| GetEvenlySpacedPoints |  | `Vector3]` splinePoints "Must have at least 2 points.", `Int32` numPoints "Must be at least 2." | `Vector3]` |
