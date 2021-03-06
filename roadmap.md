## Roadmap
With the open sourcing of the Visual Studio Test Platform behind us, it is time to look ahead. We typically **plan for a quarter**, establish a set of themes we want to work towards, and then schedule work each sprint supporting those themes. Here are the themes we will work on this quarter.

### Rich analysis using data collectors
Rich analysis of a test run requires the ability to configure and analyze auxiliary data collected during the run. This could be screen shots at various points during a UI test, or code coverage information gathered when a particular test suite runs. **vstest** enables this using data collectors. As with other [stages in the test life cycle](https://blogs.msdn.microsoft.com/visualstudioalm/2016/07/25/evolving-the-visual-studio-test-platform-part-1/), data collectors are extensible.
 - Enable data collector infrastructure

### Extensible application platform support
Every application platform comes with its own nuances. **vstest** supports the notion of a "host" that is architecture/framework specific and this is responsible for loading in each test container and discovering/executing the tests therein for each such platform. Desktop application targeting the .NET Framework, or .NET Core applications targeting a particular API level are examples of application platforms supported. We will extend this by adding support for UWP applications. This will serve as reference for adding support for more application platforms in future.
 - Enable support for UWP applications.

### Open Editor integration
The Visual Studio editor already supports discovering and executing tests using the new test platform. The editor and **vstest** interact using a JSON protocol, exchanging specific messages and payloads. We will open-up this [editor integration protocol](https://github.com/Microsoft/vstest-docs/blob/master/RFCs/0007-Editors-API-Specification.md) so that other editors from the community may suitably and equally consume **vstest**.
 - Open the editor integration protocol

### Configurable CLI integration
**vstest** ought to allow tapping into the rich and powerful capabilities of various test frameworks in a convenient and consistent manner – both from the editor as well as from the command line. This will require the ability to configure almost every capability (from discovering and executing tests, to what gets reporting, to how is the output formatted, etc.).
 - Enable configurable CLI integration with various test framework/runner capabilies.

## Summary
These are examples of the work we will be focusing on in the next quarter. We will provide much more detail through individual issues. Follow along, and let us know what you think. We look forward to working with you!
