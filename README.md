# AWS-VPC-CODE
Terraform AWS VPC code


resource "aws_vpc" "abu_jan" {
  cidr_block = "10.0.0.0/16"

  tags = {

      Name= "abu_jan"
  }
}
