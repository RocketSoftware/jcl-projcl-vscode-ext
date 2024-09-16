# PRO/JCL for JCL Management

PRO/JCL is a comprehensive Job Control Language (JCL) management tool that provides JCL validation, standards enforcement, and reformatting. It is designed to help developers streamline their JCL workflows on the z/OS mainframe. This extension allows you to access the most important features of PRO/JCL from your Visual Studio Code IDE.

## Features

PRO/JCL for VS Code offers a modern and easy-to-use user interface (UI) to interact with PRO/JCL on your z/OS system. Through this extension, you can:

* Evaluate JCLs for syntax errors.
* Enforce site-specific JCL standards.
* Provide an effective reporting facility.
* Leverage RESTful web services API to automate PRO/JCL scans in a DevOps toolchain.
* Submit jobs to the mainframe for execution.
* Validate input data for popular JCL utility programs.
* Restructure JCL into a standard and easy-to-read format.
* (New) Validate JCLs on remote machines.
* (New) Propose commonly used JCL code snippets as you type.
* (New) Suggest dataset names based on JCL in editor.
* (Upcoming Release) Validate multiple JCLs, in user-defined order if specified.

With PRO/JCL for VS Code, errors in JCL are clearly described in **PROBLEMS View** and summarized in an informational message, as shown below. The source lines associated with these errors are underlined with a wavy line, in colors that identify their severity. Hovering over one of these lines displays the errors on that line. The relative positions of these errors in the source file are displayed as color dots in the right margin, allowing easy navigation to these errors.

![Result of JCL Scan](client/resources/animated_scan_result_demo.gif "Result of JCL Scan")

Enhancements added in the latest release of **PRO/JCL for VS Code** include the following:

* JCL validation on a remote machine

![JCL Scan on a Remote Machine](client/resources/projcl_vscode_remote_scan.gif "JCL Scan on a Remote Machine")

* Auto code suggestions in JCL editor

![JCL Code Snippets](client/resources/projcl_vscode_code_suggestion.gif "JCL Code Snippets")

* Context-sensitive dataset name proposal

![Context-Sensitive DSN Proposal](client/resources/projcl_vscode_dsn_proposal.gif "Context-Sensitive DSN Proposal")

## Requirements

The following are the minimum requirements for **PRO/JCL for VS Code**:

* **Zowe Explorer VS Code Extension**: This extension provides the user interface and services required to authenticate & access resources (datasets and jobs) on the mainframe using PRO/JCL extension. Search for **Zowe Explorer** in Marketplace to find out more about this extension and install it.
* **Connection Profile Using zosmf**: The **Zowe Explorer** must be able to connect to the mainframe using a connection profile of the type **zosmf**. This implies a z/OSMF server must be running on the mainframe and accepting REST API requests.
* A valid user ID and credential for accessing mainframe resources & services using **Zowe Explorer** in VS Code.
* **PRO/JCL 3.6.1** or higher version must be installed in the z/OS system. See [PRO/JCL Installation](https://docs.rocketsoftware.com/bundle/projcl_364/page/qgk1680148808788.html) for information on installing PRO/JCL for z/OS.
* The latest cumulative service for PRO/JCL must be applied.
* **IBM Liberty Profile Server for z/OS** must be installed & configured to enable PRO/JCL REST Services. See [Building a Liberty Profile server for PRO/JCL REST Services](https://docs.rocketsoftware.com/bundle/projcl_364/page/reb1680014883070.html) for details on installing & configuring the Liberty Profile server.
* **PRO/JCL REST Services** must be installed & operational in the IBM Liberty server. See [PRO/JCL® REST Services Quick Start Guide](https://docs.rocketsoftware.com/bundle/projcl_364/page/htd1680014857177.html) for instructions on installing & deploying the PRO/JCL REST Services.

In addition, the following extensions are ideal companions to the features in **PRO/JCL for VS Code**:

* **IBM Z Open Editor**: This extension provides language-sensitive highlighting for JCL files, perfectly complementing the syntax checking & standards validation capabilities in PRO/JCL.

## Configuration Settings

The following configuration properties are available:

* `projcl-vscode.displayOptions`: Display options to use before PRO/JCL operations
* `projcl-vscode.saveListings`: Save Structured JCL Listing from PRO/JCL operations
* `projcl-vscode.saveListingsIntoLocation`: Default location is .projcl/JclListings folder in user’s home directory
* `projcl-vscode.validateBeforeReformattingJCL`: Validate JCL before Reformatting
* `projcl-vscode.workFileHLQ`: HLQ used for PRO/JCL work files on z/OS

The setting is accessible from the user interface by clicking the gear icon (Manage) in the lower left and selecting Settings, or by pressing **Ctrl+,** (**Ctrl** and **comma** keys pressed at the same time), followed by entering **PRO/JCL** in the **Search settings** input box.

## Documentation

For full documentation, visit the [Rocket Software PRO/JCL documentation](https://docs.rocketsoftware.com/bundle/projcl_364/page/fok1680013680554.html) site.

## Known Issues

Win the bragging right as one of the first users to find a non-trivial issue and report to PRO/JCL's support team. All types of issues are welcome, from outright internal errors to future enhancement ideas. All suggestions are considered as proprietary to Rocket Software and will be acknowledged, with permission, in future release notes when adopted.

## Technical Assistance and Support

The PRO/JCL extension is made available to customers on the Visual Studio Code Marketplace. If you are on active support for PRO/JCL, you can get **Technical Support** using [Support](https://my.rocketsoftware.com/RocketCommunity).

Kindly report any issue encountered in the extension to **Technical Support**.

## Release Notes

### 1.1.0

* Support JCL validation on remote systems as defined in PRO/JCL for z/OS
* Provide JCL statement completion & dataset name proposals in edit session
* Provide commonly used JCL fragments as auto suggestions in edit session

### 1.0.9

* Update links for support & documentation

### 1.0.8

* Rebranding of ASG as Rocket Software
* Update links for support & documentation
* Add input type at top of saved listing
* Validate length of JMP parameter

### 1.0.7

* Support user-specified HLQ for creation of work files on z/OS
* Support CSRF_SWITCH ON in z/OSMF configuration settings
* Support '#' in RTS and reformat member names
* Improvement in reporting of server errors

### 1.0.6

* Enhanced logging to aid field diagnostics
* Updates to product logos to reflect new branding for Rocket Software

### 1.0.2

* Support reformatting of JCL using rules defined in PRO/JCL for z/OS
* Validation of input data for common JCL utility programs

### 1.0.1

* Ensure PRO/JCL Extension meets or exceeds the criteria for **Zowe V2 Conformance - Zowe Explorer for Visual Studio Code Zowe**.

### 0.6.1

* Add Options in Effect in listing if Include Summary is selected in scan profile
* Save Structured JCL Listing in user specified location

### 0.6.0

* Support scanning of JCL from the local file system, e.g., Windows
* Submit JCL for execution after successful validation
* Use credential from Zowe Explorer for PRO/JCL connection to z/OS

### 0.5.0

Initial release of PRO/JCL for VS Code, as part of PRO/JCL 3.6.1 release. See **Features** above for a list of features.
