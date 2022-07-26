# JAM Stack

Jamstack—one of the key concepts is pre-rendering. In Jamstack sites the entire front end is prepared at the build time, and the 
resulting static output is served from a content delivery network (CDN).

As a Jamstack developer, you don't want to write all the logic for transforming your project into static files. Instead, you want 
to use some tools for this pre-rendering. These tools are doing a lot of fancy stuff for you—usually they allow you to apply 
templates, handle all the bundling and minification, and provide you with a rich ecosystem of plugins for specific use cases like 
data fetching from CMS, site map generating, or optimizing images. These tools are called static site generators. But let's talk .
NET now, where a generator called Statiq is quickly becoming a popular option.

## how to jam on .NET?
With Statiq! Statiq is a static site generator for .NET. It brings the first-class experience of both Visual Studio and VS Code 
- including Intellisense and debugging - to the Jamstack world. In combination with the .NET platform and many built-in features 
like pipelines, modules, preview server, and shortcodes, it is a great entry ticket for .NET developers and teams into Jamstack.

The Statiq project contains a general-purpose static generation framework called Statiq Framework and a convention-based static 
site generator called Statiq Web that’s built on top of it. From now on, we will be referring to Statiq.Web when talking about 
Statiq.

### The basics of Statiq
For a start, let's explain some key concepts and specifics of Statiq. I believe these are essential to having a solid base when 
starting with this static site generator.

### Documents
A document is a primary unit of information in Statiq. It consists of content and metadata. Imagine that Statiq is like a 
document database that can process these documents. To be more precise, these documents are immutable. When a document is 
processed, it's returned a new instance of the document. Documents are manipulated by modules.

### Modules
A module is a component that performs a specific action with documents. A module takes documents as input, does an operation 
based on those documents (possibly transforming them), and outputs documents as a result of whatever operation was performed. 
Modules are typically chained in a sequence called a pipeline.

### Pipelines
A pipeline is a document processing unit. A pipeline consists of one or more modules. Basically, the pipeline is a workflow 
blueprint of how your modules should handle documents. One might find a slight analogy with a controller in .NET MVC, 
nevertheless, it's good to think about pipelines in a more declarative way. You just specify what your output should be rather 
than how to transform and produce it.

Pipelines have their own lifecycle process defined by phases. When pipelines and modules are executed, the current state is 
passed in the execution context.

## steps to ose it 

1. Create a new project
2. Create an index page with a custom Razor template
3. Create a listing page with a Razor template
4. Create a detail page with default markdown rendering
5. Prepare content in the headless CMS Kontent
6. Integrate content from the CMS into our Statiq site
7. Let's publish it on Netlify
8. Unpublished preview content on Netlify

### Constructing your app
With Scully in the picture, you can pretty much pick your favorite flavor of UI framework and get off the ground running. Here’s a few popular ones to get started, but by no means is it exhaustive.

1.11ty
2.Gatsby
3.Hugo
4.Nift
5.Scully (for you Angular fans)

### Serving your app
I like to think of this as the easy part depending on your setup. Tools like Netlify and Zeit make this a breeze to configure by 
hooking into your Github repo and building anytime a new commit gets pushed, but of course you have options like AWS if you want 
more control.

1.AWS
2.Azure
3.GCP
4.Github Pages
5.Netlify
6.Surge
7.Zeit
















