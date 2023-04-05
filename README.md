# CPG Generator

```
 ██████╗██████╗  ██████╗
██╔════╝██╔══██╗██╔════╝
██║     ██████╔╝██║  ███╗
██║     ██╔═══╝ ██║   ██║
╚██████╗██║     ╚██████╔╝
 ╚═════╝╚═╝      ╚═════╝
```

This action wraps CPG Generator (cpggen) a python cli tool to generate [Code Property Graph](https://cpg.joern.io) for multiple languages. The generated CPG can be directly imported to [Joern](https://joern.io) or uploaded to [Qwiet.AI](https://docs.shiftleft.io/home) for analysis.

## Usage

Autodetect languages storing CPGs in a directory called `cpg_out`

```
- uses: AppThreat/cpggen-action@main
  with:
    out_dir: "/github/workspace/cpg_out"
```

Use `lang` argument to push the language type

```
- uses: AppThreat/cpggen-action@main
  with:
    out_dir: "/github/workspace/cpg_out"
    lang: java
```

## Languages supported

| Language    | Requires build |
| ----------- | -------------- |
| C           | No             |
| C++         | No             |
| Java        | No (\*)        |
| Scala       | Yes            |
| Jsp         | Yes            |
| Jar/War     | No             |
| JavaScript  | No             |
| TypeScript  | No             |
| Kotlin      | No (\*)        |
| Php         | No             |
| Python      | No             |
| C# / dotnet | Yes            |
| Go          | Yes            |

(\*) - Precision could be improved with dependencies

## Environment variables

| Name                    | Purpose                                                      |
| ----------------------- | ------------------------------------------------------------ |
| AT_DEBUG_MODE           | Set to debug to enable debug logging                         |

## License

Apache-2.0
