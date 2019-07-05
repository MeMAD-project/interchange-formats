# MeMAD Metadata Interchange Formats

[![MeMAD](https://pbs.twimg.com/profile_images/950264367261548546/bcBS5FT__400x400.jpg)](https://memad.eu)

This repository contains definitions of the interchange formats used for the EU H2020 MeMAD projects. It also provides examples of each of these formats such that component developers (inside the project or external integrators) can easily get acqainted with the formats and implement them in their systems. 

Interchange formats are defined for the following metadata for describing audiovisual content:

- Speech segmentation information (IO3)
- Audio classification information (IO4)
- Timed speech transcripts (IO5).
- Speaker identification (IO6)
- Visual person identification (IO7).
- Shot-cut boundaries (IO8).
- Translated text fragments (IO9).
- Text with detected and disambiguated named entities (IO10).
- Semantically enriched text with detected and disambiguated named entities and links to related resources (IO11).
- Subtitles (IO12)
- A list of segments with disambiguated descriptive metadata (IO13)
- Natural language video captions (IO14).
- Audio descriptions (IO15)
- Ranked segments with disambiguated descriptive metadata (IO16)
- Production Scripts (IO17)
- Edit Decision Lists (IO18)
- Audiovisual program context metadata (IO19)

## The MeMAD Base Framework

We use a metadata framework that can be re-used for many forms of data exchanges. For this **MeMAD Base**, we integrate other specifications or custom extensions to model exchange formats for each of the input/output data mentioned above. 
The framework consists of the following components:
1.	We use the [EBUCore](https://tech.ebu.ch/MetadataEbuCore) metadata framework for describing the context of the metadata, i.e., for pointing to the information that refers to the audiovisual content being described. Typically, this involves identifying the program that is being annotated, listing its contributors and basic properties (e.g., owner, subject, etc.) and defining its relation to the audiovisual media and information systems where the item is stored.
2.	We use the [Web Annotation Data Model](https://www.w3.org/TR/annotation-model/) for describing actual annotations or metadata that describe the audiovisual content. Annotations can be made of various types and contents, which we will describe below. The Web Annotation Data Model is supported by the [Media Fragments](https://www.w3.org/TR/media-frags/) mechanism to enable annotations to refer to segments (temporal, spatial or audio and video track-wise) of the audiovisual content.

On top of this framework, we specify a number of extensions where required, e.g., for representing ASR data or dealing with translated text fragments.

## RDF-based

Because the MeMAD Base and most other metadata models we propose for use are defined using RDF, their serialization can be done in various different forms, including [RDF/XML](https://www.w3.org/TR/rdf-syntax-grammar/) to better align with legacy systems, in [N3](https://www.w3.org/TeamSubmission/n3/) for better readability, but also as [JSON-LD](https://www.w3.org/TR/json-ld/) for easier integration with recent web development frameworks and APIs.




![EU emblem](img/euflag.png)                         | MeMAD project has received funding from the European Union’s Horizon 2020 research and innovation programme under grant agreement No 780069. This document has been produced by the MeMAD project. The content in this document represents the views of the authors, and the European Commission has no liability in respect of the content.
------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

