# Eyball
Anomaly detection engine

Implement a class to detect anomalies, using an AI model in images based which call be called from visual checking automation.

![Eyball](eyball3.png "Eyball")

Date: 5/23/2024

Fulmine Labs LLC

## Overview

This Python code implements a class wrapper around an Anomaly Detection model which can be used to visually check if an image is anomalous or not. The supported architecture for this model is 'Siamese Network'. In order to perform reduce false negatives the code compares the image against a jury of randomly selected known good images of configurable size 'jury_size'. These images were studies obtained from the Cancer Imaging Archive database, stored in Orthanc. If the number of jurors who vote that the image is simlar to the chosen known good image is below a configurable 'threshold' then the code returns a verdict of 'Anomalous', otherwise it returns a verdict of 'Normal'. If an image path is not specified but screen coordinates are, these will be used instead, enabling direct integration with automated visual checking scripts.

One goal is to use this class as part of automating visual checking of a medical image (PACS) production pipeline, although it could theoretically visually check any type of image on which the model has been trained.

It also has the capability of describing the images, using GPT-4 Turbo Vision, if an OpenAI key is supplied in the 'Eyball-OpenAI_key.txt' file.

## Datasources used

Cancer Imaging Archive images, stored in Orthanc
CT images randomly selected from internet sources for testing

## Current Version
The current stable version of the project is 0.1
See the [CHANGELOG.md](CHANGELOG.md) file for details about this version.

## Prerequisites

* Anaconda, with an environment having the Python libraries listed in [requirements.txt](requirements.txt)


## Usage

Install Anaconda, create an environment and install the dependencies in requirements.txt


## Testing


## Known issues


## Acknowledgements

This code was written collaboratively with [GPT-4V](https://chat.openai.com/). Thank you Assistant!


## License
MIT open source license

## Collaboration
We welcome contributions at all levels of experience, whether it's with code, documentation, tests, bug reports, feature requests, or other forms of feedback. If you're interested in helping improve this tool, here are some ways you can contribute:

Ideas for Improvements: Have an idea that could make the Fulmine Labs mini-PACS better? Open an issue with the tag enhancement to start a discussion about your idea.

Bug Reports: Notice something amiss? Submit a bug report under issues, and be sure to include as much detail as possible to help us understand the problem.

Feature Requests: If you have a suggestion for a new feature, describe it in an issue with the tag feature request.

Documentation: Good documentation is just as important as good code. Although this is currently a very simple tool, if you'd like to contribute documentation, we'd greatly appreciate it.

Code: If you're looking to update or write new code, check out the open issues and look for ones tagged with good first issue or help wanted.

## Contact
Duncan Henderson, Fulmine Labs LLC henderson.duncanj@gmail.com
