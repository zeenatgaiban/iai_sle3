# Contribution Log

**Project:** BFS vs DFS -- 26-Node (A--Z) Empirical Performance Analysis
System\
**Student:** Jeenat Faiyaz Gaiban\
**PRN:** 25UAM121\
**Course:** Introduction to Artificial Intelligence (02AML204)

## Purpose

This log records the division between student work and AI assistance for
the project documentation and architecture. It is based on the submitted
SLE-3 report and its four C4 diagrams. It does not claim that AI wrote
or executed source-code lines.

## Contribution entries

  ----------------------------------------------------------------------------------
  Area / artifact       Student contribution    AI-assisted        Verification /
                                                contribution       evidence
  --------------------- ----------------------- ------------------ -----------------
  System definition     Defined/submitted the   Helped organize    Checked against
                        project topic and its   the project        the SLE-3
                        intended comparison of  description into a report's system
                        BFS and DFS on a        concise README     title and
                        26-node graph, as       structure.         description.
                        represented in the                         
                        report.                                    

  C4 Level 1 -- Context Supplied the context    Helped describe    Compared with the
                        diagram showing the     the diagram's      supplied Level 1
                        user/researcher,        inputs and outputs diagram and
                        system, and results.    in documentation.  report.

  C4 Level 2 --         Supplied the container  Helped turn the    Compared with the
  Container             diagram for graph       diagram labels     supplied Level 2
                        configuration, search   into a readable    diagram and
                        engine, BFS, DFS,       architecture       report.
                        profiler, and results.  section.           

  C4 Level 3 --         Supplied the component  Helped explain the Compared with the
  Component             diagram covering        responsibilities   supplied Level 3
                        frontier, visited set,  of the shown       diagram and
                        goal test, and node     components.        report.
                        counter/timer.                             

  C4 Level 4 -- Code    Supplied the code-level Helped format      Compared with the
                        diagram identifying     these              supplied Level 4
                        `graph`, `bfs()`,       responsibilities   diagram and
                        `dfs()`, `test_cases`,  in the README.     report.
                        and                                        
                        `benchmark_search()`.                      

  README.md             Reviewed the generated  Drafted this       Implementation
                        documentation for       README from the    filename and
                        consistency with the    supplied report    measured output
                        submitted project       and diagrams,      are explicitly
                        report.                 including          left unspecified
                                                architecture,      because they were
                                                requirements,      not present in
                                                running guidance,  the supplied
                                                and limitations.   materials.

  CONTRIBUTION_LOG.md   Should review this log  Drafted this       This log should
                        and make any            contribution log   be updated if the
                        corrections needed to   and separated      actual coding
                        accurately reflect the  documentation      history or AI
                        work performed.         assistance from    contribution
                                                implementation     records provide
                                                claims.            more detail.
  ----------------------------------------------------------------------------------

## Code-level AI contribution record

The supplied SLE-3 report states that AI tools were used to format the
architecture across the four C4 levels, generate draw.io-ready Mermaid
diagrams, and align the report layout with submission guidelines. It
also states that code implementation, empirical execution, node
counting, and `py-spy` profiling runs were performed independently by
the student.

Based on that report:

-   **AI assistance reported:** architecture/documentation formatting,
    diagram-generation assistance, and report-layout support.
-   **Student work reported:** code implementation, benchmark execution,
    node counting, and profiler runs.
-   **Source-code line-by-line attribution:** not available from the
    supplied files because the Python source and a line-level AI
    contribution record were not provided. Do not treat this document as
    a line-by-line code log.

## How to maintain this log

For each later change, add a row with the date, file/function changed, a
short description, whether AI assistance was used, what was accepted or
modified by the student, and how the result was tested. Record
code-level details from the actual edit history rather than
reconstructing them from the architecture diagram.
