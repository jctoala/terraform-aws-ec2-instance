# Terraform script to create a VPC, Subnet, Internet Gateway, Route Table, Security Group, and EC2 instance in AWS

Este proyecto usa Terraform para crear una instancia de Amazon EC2 e instalar un servidor web. La instancia permite el acceso desde internet. Los recursos son desplegados desde una VPC con una subred publica y igw para que los recursos accedan a internet.

## Recursos creados

Grupo de recursos (aws_resourcegroups_group): Agrupa recursos etiquetados como Environment = dev.

VPC (aws_vpc): Red privada con el rango CIDR 172.16.0.0/16.

Subred pública (aws_subnet): Subred dentro de la VPC, ubicada en us-east-1a.

Internet Gateway (aws_internet_gateway): Permite acceso a internet desde la VPC.

Tabla de rutas (aws_route_table): Permite salida a internet a través del Internet Gateway.

Asociación de tabla de rutas (aws_route_table_association): Conecta la subred pública con la tabla de rutas.