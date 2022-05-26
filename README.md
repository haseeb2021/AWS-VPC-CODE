# AWS-VPC-CODE
Terraform AWS VPC code


resource "aws_vpc" "abu_jan" {
  cidr_block = "10.0.0.0/16"

  tags = {

      Name= "abu_jan"
  }
}

##Subnet Code: below subnet resource refer to above VPC, so Subnet will be created in above VPC.

resource "aws_subnet" "New-subnet1" {
                vpc_id = aws_vpc.abu_jan.id
                cidr_block =  "10.0.0.0/24"
                tags = {
                  "Name" = "new_subnet1"
                }
}
