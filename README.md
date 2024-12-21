
# Software design document for the myappmaker (working title) app

Author: Kennedy Richard S. Guerra ([kennedyrichard.com](https://kennedyrichard.com) | [@KennedyRichard](https://github.com/KennedyRichard))


## Overview

This [software design document](https://en.wikipedia.org/wiki/Software_design_description) was created to help manage the development of myappmaker ([GitHub repo](https://github.com/IndiePython/myappmaker)) for both its maintainer (me, Kennedy R. S. Guerra) and other developers who desire to contribute code to the project. It aims to do that by offering detailed information on myappmaker's design, including its definition, goals, current and planned features/behaviour and also brief analyses of alternative software that offer further insight into design decisions made for myappmaker.

## Table of contents

1. Software design document for the myappmaker (working title) app/README (you are here)
1. [Definition, requirements and challenges](ch-definition-requirements-challenges.md)
1. [Usage and basic design](ch-usage-basic-design.md)
1. [Goals](ch-goals.md)


## Stakeholders

myappmaker (working title) aims to be a versatile software in the Python ecosystem of tools. As the name implies, it is meant to be an app builder, that is, an app that allows users to create apps. It will do that using no-code/low-code tools such as drag-and-drop interfaces and block coding. By providing that, it should reach a wide range of applications for countless different tasks.

Being free of charge and placed in the public domain grants unlimited access to the software and its source to anyone. The underlying GUI library (PySide6) is also made available by its provider under the very permissive LGPL license.

Although created and maintained by Kennedy Guerra, the original idea and requirements were provided by William Adams ([@WillAdams](https://github.com/WillAdams)) and many other users who have wished for a replacement for HyperCard, or that there was some similar tool for creating software applications.

All those facts make myappmaker's importance evident. This is why this design document is important as a tool to help drive its development, keeping the software healthy and maintainable. It has a unique role and wide application both inside and outside the Python ecosystem, since users not proficient at programming are expected to be able to use it as well.


## Context

In order to improve the chances of success of this document and of myappmakers's development, it is necessary to understand the context of its development. This includes knowing both what the project is and what it is not.

myappmaker is not a commercial project led by industry professionals using state-of-the-art processes and with access to enough resources and budget. It was created by me, (Kennedy Richard S. Guerra), a self-taught software developer whose formal education consists of a degree in Business Administration (although I do not work on the field), with the idea to create a general-purpose no/low-code software/application development environment.

Despite not having a formal education and training in software development/engineering, I have learned programming through diligent study of technical books and thousands of hours of practice poured into many different software projects. Such projects range from simple CLI scripts to full-fledged desktop GUI applications.

Since I'm a single software developer and myappmaker is expected to turn into a relatively large application, it is crucial that its design planning and development are devoid of complex management structures/practices. Instead, we must rely on simple and manageable practices that ensure the sustainability and progress of its development. We aim to reflect this is in this design document. It is meant to be a very lean document.

Most notably, it aims to describe existing behaviours/features in detail so that they can be implemented and inspected in detail and maybe, in the future, be used as the basis for tests (specially automated GUI tests). Automated tests are one of the most important and reliable tools to guarantee the sustainability of the project. This is so simply because they attest the quality and reliability of the application and ensure such quality and reliability are kept in new releases.

Perhaps the only tool more important than tests is this design document itself, since in a sense it is in itself a test that is used by developers to ensure the automated tests they write/update/remove are relevant or not to the design. Tests test code, design tests tests.

Another notable aspect of this design document is the absence of specific dates in the timeline for features/changes/improvements. This is so because, like most small personal open-source projects, we are still underfunded and understaffed. In other words, we are not a well-managed organization with paid staff. Thus, pretending we have the resources required to present and follow strict deadlines would only amount to unnecessary bureaucracy and lead to frustration.

Instead, we prefer to just list the items to be pursued and strive to deliver changes and improvements regularly or at least semi-regularly, showing competence through our achievements over time instead of relying on displaying deadlines solely for the amusement of our users/audience.

This document may also prove useful to other developers that want to learn one possible way of making an app maker tool. It may also be useful if we or other developers ever want to implement this app in some other GUI framework/library.

In conclusion, in order to be successful, this design document must effectively serve as a basis for myappmaker's development.

