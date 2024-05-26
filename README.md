# shacl-test-qualified-value-shape

The behaviour of sh:qualifiedValueShape does not appear to be working as specified in SHACL Spec https://www.w3.org/TR/shacl/#QualifiedValueShapeConstraintComponent

The example shape (shapes.ttl) can be used to specify the condition that the property ex:parent has exactly two values, and at least one of them is female.

This repo contains a data graph (data-pass.ttl) that passes, and a second data graph (data-fail.ttl) with no female parents that should fail but passes.

Run tests:
> rdf shacl data-pass.ttl --shape shapes.ttl #--> passes

> rdf shacl data-fail.ttl --shape shapes.ttl #--> expected to fail but passes