# Philosophy
The goal of the TTPbase is to provide a structured methodology to define specific tool use scenarios, their prerequisites, and their outcomes.

# Structure
TTPBase used YAML files for overall structure.

**id** *string* REQUIRED

This is a unique string value that should not have spaces. It can be human meaningful or not. We're not your mom. 

**info** *info*

Metadata about the thing. Use it or not. 


## info
**name** *string*

A name for the TTP and it's collective pre-reqs. This can have spaces, unlike the **id**
**description** *string*

A hopefully useful description of the TTP.

**Author** *string*

Who we can blame for this

**Version** *string*

We suggest that if you use this, it be some kind of semantic versioning. 

## requirements

**source-node** *node*

**destination-node** *node*

**edge** *edge*

## node
**type** *string*

The type of edge

**export** *string*

This is the value that will be made available to the execution engine.

**matchers** *list of matcher*


## edge
**type** *string*
The type of node

## matcher

**type** *string*

**property** *string*

The property name

**value** *string*

The value that we are comparing to.

**operator** *string*
This is the comparison operation. 
- ==
- !=
- contains
- startswith
- endswith

## execution
**command** *string*

The commmand with arguments to be called. 

## outcomes
What we expect to get out of it. 

**scoring** *int*
This is the scoring factor that will be used for ranking options for the execution engine (if the execution is successful)

**node** *outcomenode*
If the command is successful, we're going to get one or more new nodes

##outcomenode

**type** *string*

This is the type of the node

**properties** *list of string*
These are the properties that we're expecting to gain new information. 





# Examples
See the /examples directory of this repo 