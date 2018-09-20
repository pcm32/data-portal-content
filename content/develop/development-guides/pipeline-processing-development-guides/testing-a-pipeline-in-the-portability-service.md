---
path: "/develop/development-guides/pipeline-processing-development-guides/testing-pipelines"
date: "2018-07-12"
title: "Pipeline Testing Guide"
---

## How do I test my pipeline in the portability service?

Currently, the portability service exists as an API that can be leveraged using command line or continuous integration tools. With this interface you can demonstrate that your pipeline runs in HCA DCP execution environments as well as other execution environments. The service records whether the pipeline was able to execute to completion without error and whether it produced the expected output results in each environment.

In order to run the test, you need the following:

1. **A pipeline.** The service supports pipelines written in WDL or CWL.
2. **Input data.** Standard test data to use when running the pipeline. This should be small, allowing for the pipeline to execute quickly.
3. **Expected output.** Expected results from executing the pipeline on the standardized data.
4. **Checker step.** A step at the end of the pipeline to verify that the pipeline produced the expected results. The portability service only checks for the success or failure of a pipeline, so if the expected results are not produced, this step should raise an error.

The portability service sends the candidate pipeline, the associated checker tool, and the test input data to one or multiple execution infrastructures, which run the pipeline in that environment and succeed or fail depending on whether expected outputs are returned.

## Example Pipeline Submission 
(TBD)
## Best practices in pipeline development

As we learn more about portability it is important to share that knowledge with others. We are currently defining our best practices; please check back with us.