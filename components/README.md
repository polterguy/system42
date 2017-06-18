
System42 components
========

This folder contains all of your System42 components. A component is a reusable piece of logic, written in Hyperlambda, 
that you can reuse across multiple apps.

There is one file which most components would declare called "startup.hl", expected to do the initialization of your 
component. Usually, if this file exists, it will create the Active Events necessary to consume your component.

This allows you to distribute your System42 using x-copy deployment. By default, System42 contains several pre-built 
components. If you wish to remove these, simply delete the folder containing your component. Preferably _before_ you 
start your server the first time, such that the component's initialization logic does not run.

To see the documentation for your specific components, please refer to the specific component folders inside of this project.

A component can either be a piece of logic, or a reusable widget of some sort, or some other piece of reusable thing that
you can utilize in your own projects.

## Component list

Below is a list of all the components in this folder, with a short explanation of what they do.

- [Bootstrap CSS](bootstrap/) contains the Bootstrap CSS framework
- [Common widgets](common-widgets/) contains common widgets, such as Ajax datagrids, tab controls, tree view, uploaders, etc
- [Common windows](common-windows/) contains some common windows, such as a debugging window, and an info tip window
- [CSS helpers](css-helpers/) contains a couple of CSS helper Active Events, to remove and add CSS classes from widgets
- [CSV helpers](csv-helpers/) contains events for importing CSV files
- [Image helpers](image-helpers/) contains events for manipulating images
- [jQuery](jquery/) contains events to include jQuery
- [Settings](settings/) contains events for accessing and changing settings of your applications
- [Speech](speech/) contains events for synthesizing speech from a piece of text
- [Translate](translate/) contains events for translating between different languages

