# Carleton Computer Science Course Tree

This repo breaks down some sample graphs of what the courses required for CS at
Carleton look like when it comes to requirements.

## Dependency Tree

This a visualization of the requirements tree for the different CS courses in
different years.

```mermaid
flowchart TB
    subgraph firstyear [First Year]
    1405
    1406
    1805
    end
    1405-->1406

    1805-->2804
    1805-->3005
    1805-->3007

    1406-->2401
    1406-->2402
    1406-->2406

    subgraph secondyear [Second Year]
    2401
    2402
    2404
    2406
    2804
    end

    2401-->2404
    2401-->3004

    2402-->3000
    2402-->3005
    2402-->3007
    
    2404-->3004

    2406-->3004

    2804-->3804

    subgraph thirdyear [Third Year]
    3000
    3004
    3005
    3007
    3804
    end
```

## Example Timeline

Although this graph isn't the only way to do it, here is an example timeline of
what your first few years might look like. The timeline from left to right is
one semester after another, excluding summer semesters. This doesn't take into
consideration any electives.

```mermaid
    gantt
        axisFormat %M
        section First Year
        1405 :1405, 2014-01-01, 1m
        1805 :1805, 2014-01-01, 1m
        STAT 2507 :2507, after 1405, 1m
        1406 :1406, after 1405, 1m

        section Second Year
        2401 :2401, after 1406, 1m
        2402 :2402, after 1406, 1m
        2404 :2404, after 2401, 1m
        2406 :2406, after 2401, 1m
        2804 :2804, after 2401, 1m

        section Third Year
        3000 :3000, after 2404, 1m
        3004 :3004, after 3000, 1m
        3005 :3005, after 3000, 1m
        3007 :3007, after 2404, 1m
        3804 :3804, after 2404, 1m
```
