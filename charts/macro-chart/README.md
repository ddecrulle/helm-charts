# Running the Charts Locally

This guide outlines the steps required to run the Helm charts locally for the MacroChart. This is a POC chart to test tpl and pass values between sub charts.

## Prerequisites

Before running the charts locally, ensure that you have the following prerequisites installed:

- Helm: [Installation Guide](https://helm.sh/docs/intro/install/)

## Steps

1. **Package Subcharts:**

   Navigate to the `sub1` and `sub2` directories, and package each Helm chart using the following command:

   ```bash
   helm package .
   ```

   This command creates a `.tgz` package for each subchart.

2. **Run Helm Install:**

   Once the subcharts are packaged and the dependency repository is updated, you can template the MacroChart locally using the following command:

   ```bash
   helm template my-macrochart .
   ```

   Replace `my-macrochart` with your desired release name.