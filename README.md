# Official Diagram GitHub Package

https://github.com/mingrammer/diagrams?tab=readme-ov-file 

# Steps for writing the code Manually

## “Diagram” — Top level container of your diagram

`with Diagram("S3 to RDS", show=True, direction="LR", curvestyle="ortho", outformat="png"):`


S3 to RDS refers to the filename of the image to save

direction — It will start building the containers from Left to right(LR), Right to Left, Top to Bottom are options you can use if needed.

output format- currently supports "png", "jpg", "svg", "pdf" formats.


## “Cluster” — Second level container (you can specify the name or label of the container)

`with Cluster("AWS"):`

## Edge

“>>” — Right pointed arrow or edge

`event_bridge >> Edge(label="triggers") >> lambda1`

“<<”— Left pointed arrow or edge

“-” — Edge without direction or bidirectional

`s3_raw_layer - Edge(label="push") - lambda1`