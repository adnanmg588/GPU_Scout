Changelog

#### Version 3.0.3
- Added 'available_count' value for DRCC customers and whitelisted tenancies.

#### Version 3.0.2
- Handled specific use case exceptions with flexible shapes.
- Increased region connectivity timeout and improved exception handling.

#### Version 3.0.1
- Minor fixes and improvements.

#### Version 3.0.0
**New Features**
- **Interactive Support for Admin and Non-Admin Users:**
  - Administrators can bypass prompts using the `-su` argument.
  - Non-admin users can specify their compartment with the `-comp` argument.

- **Resource Filters and Display:**
  - Introduced oCPU and Memory filters for targeted analysis.

- **Script Relaunch Loop:**
  - The script automatically relaunches after completing a query or encountering an error.

- **Enhanced Authentication:**
  - Re-authentication functionality prompts the user for a config file if all other authentication methods fail.

- **Error Handling and Code Management:**
  - Improved exception handling and code structure for better performance.

#### Version 2.0.1
**New Features**
- **Support for Non-Admin Users:**
  - Added `set_user_compartment` function in `./modules/identity.py`.
  - Introduced `-su` argument for administrators to bypass prompts.
  - Included `-comp` argument for non-admin users to specify their compartment.

- **Compartment State Verification:**
  - Implemented checks to ensure valid compartment states before execution.

- **Error Logging:**
  - Enhanced error log messages in the `create_and_print_report` function.

#### Version 2.0.0
**New Features**
- **Automated Authentication Testing:**
  - The script now tests all available authentication methods by default, removing the need for manual specification.

- **Manual Authentication Selection:**
  - Users can enforce specific authentication methods using the `-auth` argument with options `cs`, `cf`, or `ip`.

- **Dynamic Region Handling:**
  - Connectivity to a region is verified before any requests are made.
  - Users can analyze the home region by default, specify a target region with `-region`, or analyze all subscribed regions using `-region all_regions`.

- **Shape Verification and Input Handling:**
  - Ensures the specified shape exists before running capacity reports.
  - Prompts users for input and displays available shapes if no shape is provided.

- **Support for DenseIO Flexible VM Shapes:**
  - Added support for DenseIO Flexible VM shape configurations.

- **Custom oCPUs and Memory:**
  - Enabled users to configure specific oCPUs and memory for requested shapes.

- **Automatic Shape List Update:**
  - Automatically updates the list of available shapes to provide the most current options.