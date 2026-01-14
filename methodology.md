# Methodology

How we collect, verify, and maintain terminal emulator comparison data.

## Data Collection Principles

### 1. Hard Facts Only
We include **only** objective, verifiable information:
- ✅ Official feature lists from documentation
- ✅ Benchmark results with documented methodology
- ✅ Platform support confirmed by official sources
- ✅ License information from repositories
- ✅ Installation methods from official guides
- ✅ Performance metrics from official benchmarks

We explicitly **exclude**:
- ❌ Subjective opinions ("best", "easiest", "most beautiful")
- ❌ Unverified user reviews or Reddit comments
- ❌ Personal preferences or recommendations
- ❌ Speculation about future features (unless officially announced)

### 2. Source Hierarchy

Data is collected in this priority order:

1. **Official Documentation** (highest priority)
   - Project websites (e.g., ghostty.org, alacritty.org)
   - Official documentation sites
   - Official blog posts by creators

2. **Official Repositories**
   - GitHub repositories
   - README files
   - CHANGELOG files
   - Release notes
   - Issue/discussion threads with developer responses

3. **Official Benchmarks**
   - Performance pages maintained by projects
   - Benchmark tools created by projects (e.g., vtebench by Alacritty)
   - Published benchmark results with methodology

4. **Authoritative Third-Party Sources**
   - LWN.net technical articles
   - Academic benchmarks (Dan Luu's terminal latency research)
   - Industry-recognized benchmarking sites

### 3. Verification Process

Every claim must be:
1. **Sourced** - Linked to authoritative documentation
2. **Cross-referenced** - Verified across multiple sources when possible
3. **Dated** - Timestamp of when data was collected
4. **Versioned** - Note which version specifications apply to

## Data Categories

### Platform Support
- Check official installation documentation
- Verify available binaries/packages
- Note minimum OS version requirements
- Distinguish between "supported", "planned", and "not supported"

### Features
- Reference official feature lists
- Test claims in documentation (where possible)
- Note implementation details (e.g., "Metal" vs "OpenGL")
- Distinguish between full support, partial support, and no support

### Performance Metrics
- Use official benchmark results when available
- Reference benchmarking methodology
- Note hardware/OS configuration for benchmarks
- Include multiple metrics (startup time, latency, throughput, memory)

### Configuration & Customization
- Document configuration file format
- Count themes from official repositories
- Verify customization capabilities in documentation

## Update Process

### When to Update
- New major version releases
- Significant feature additions
- Performance improvements
- Platform support changes
- Corrections from community

### How to Update
1. Check official release notes
2. Update affected fields
3. Update "Last accessed" date
4. Update version numbers
5. Add new sources if needed

## Quality Standards

### Accuracy
- Never guess or estimate values
- Use "~" prefix for approximate values (e.g., "~50MB")
- Use ranges when exact values unavailable (e.g., "100-150ms")
- Note when data is unavailable rather than omitting

### Consistency
- Use same format across all terminals
- Use same terminology (e.g., "splits" vs "panes")
- Use same emoji/symbols (✅ ❌ 🚧 ⚠️)
- Maintain parallel structure in tables

### Neutrality
- Describe features, don't evaluate them
- "Supports GPU acceleration via Metal" ✅
- "Has the best GPU acceleration" ❌
- State facts without interpretation

## Sources for Initial Data (2026-01-14)

### Ghostty
- Official Documentation: https://ghostty.org/docs
- GitHub Repository: https://github.com/ghostty-org/ghostty
- Mitchell Hashimoto's Blog: https://mitchellh.com/writing
- LWN.net Article: https://lwn.net/Articles/1004377/

### Alacritty
- Official Website: https://alacritty.org
- GitHub Repository: https://github.com/alacritty/alacritty
- vtebench Benchmarking Tool: https://github.com/alacritty/vtebench
- LWN.net Terminal Analysis: https://lwn.net/Articles/751763/

### Kitty
- Official Documentation: https://sw.kovidgoyal.net/kitty/
- Performance Documentation: https://sw.kovidgoyal.net/kitty/performance/
- GitHub Repository: https://github.com/kovidgoyal/kitty
- Graphics Protocol Specification: https://sw.kovidgoyal.net/kitty/graphics-protocol/

## Contributing Corrections

If you find incorrect information:

### Create an Issue
Include the following:
1. **Terminal name** and **field** that's incorrect
2. **Current value** shown on this site
3. **Correct value** with explanation
4. **Source link** to official documentation
5. **Date accessed** for the source

### Submit a Pull Request
1. Update the affected markdown file
2. Add source link in "Sources" section
3. Update "Last accessed" date
4. Explain changes in PR description

### Guidelines
- One terminal per PR for clarity
- Always include source links
- Follow existing markdown formatting
- Maintain neutral, factual tone

## Limitations

This comparison has intentional limitations:

- **No subjective ratings** - We don't rate "user experience" or "ease of use"
- **No feature recommendations** - We don't suggest which features matter
- **No use-case guidance** - We don't recommend terminals for specific users
- **No completeness guarantee** - Some terminals may have features we haven't documented
- **Point-in-time accuracy** - Data is accurate as of collection date but may become outdated

Our goal is to provide raw data so you can make your own informed decisions.

## Contact

- **Issues:** https://github.com/marcsteffen/terminal-emulators/issues
- **Pull Requests:** https://github.com/marcsteffen/terminal-emulators/pulls

[← Back to Home](README.md)
