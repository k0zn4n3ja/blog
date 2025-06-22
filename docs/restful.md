Fan of dbs and RESTful specification. strange paradox - "REST"ful apis often aren't, and nonRESTful apis are still massively influenced by the work of fielding


REST is defined by four interface constraints:
identification of resources; manipulation of resources through representations; selfdescriptive messages; and, hypermedia as the engine of application state. 



In order to further improve behavior for Internet-scale requirements, we add layered
system constraints (Figure 5-7). As described in Section 3.4.2, the layered system style
allows an architecture to be composed of hierarchical layers by constraining component
behavior such that each component cannot “see” beyond the immediate layer with which they are interacting. By restricting knowledge of the system to a single layer, we place a
bound on the overall system complexity and promote substrate independence. 



More precisely, a resource R is a temporally varying membership function MR(t),
which for time t maps to a set of entities, or values, which are equivalent. The values in the
set may be resource representations and/or resource identifiers. A resource can map to the
Table 5-1. REST Data Elements
Data Element Modern Web Examples
resource the intended conceptual target of a hypertext reference
resource identifier URL, URN
representation HTML document, JPEG image
representation metadata media type, last-modified time
resource metadata source link, alternates, vary
control data if-modified-since, cache-control
89
empty set, which allows references to be made to a concept before any realization of that
concept exists — a notion that was foreign to most hypertext systems prior to the Web
[61]. Some resources are static in the sense that, when examined at any time after their
creation, they always correspond to the same value set. Others have a high degree of
variance in their value over time. The only thing that is required to be static for a resource
is the semantics of the mapping, since the semantics is what distinguishes one resource
from another.

RESTful is a great idea: 

- abstraction 
- resource organisation
- agreement between server and client on hypermedia transfer


This abstract definition of a resource enables key features of the Web architecture.
First, it provides generality by encompassing many sources of information without
artificially distinguishing them by type or implementation. S

A representation is a sequence of bytes, plus representation metadata to
describe those bytes. Other commonly used but less precise names for a representation
include: document, file, and HTTP message entity, instance, or variant.(or JSON)



- extension of HTTP (wow, fits with the chaotic 2000s internet)
- extensible and future proof (www guys and fielding thought of that)
- layered client server style enabled more complicated distributed architectures


The definition of resource in REST is based on a simple premise: identifiers should
change as infrequently as possible. Because the Web uses embedded identifiers rather than
link servers, authors need an identifier that closely matches the semantics they intend by a
111
hypermedia reference, allowing the reference to remain static even though the result of
accessing that reference may change over time. 

- abstraction of resource -  permanence of API, predictability and security of contract

Information hiding is one of the key software engineering principles that motivates the
uniform interface of REST. Because a client is restricted to the manipulation of
representations rather than directly accessing the implementation of a resource, the
implementation can be constructed in whatever form is desired by the naming authority
without impacting the clients that may use its representations. I