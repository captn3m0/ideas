# Mars: Terraform Remote HTTP Backend with End-to-End encryption

A fork of <https://www.terraform.io/docs/backends/types/http.html>, which changes the configuration format to:

```hcl
terraform {
  backend "mars" {
    address = "https://mars.com/03fa43d6-adbe-4e03-8e25-ffdf8a3e456a"
    encryption_key = "${var.MARS_ENCRYPTION_KEY}"
  }
}
```

The lock/unlock address can be inferred. The service can be made public as well, since the backend just needs to be a simple/dumb storage for blobs (back it by S3 perhaps?)


## Why

- For casual projects, Terraform Enterprise is too much
- Separate Infrastructure for Terraform State store makes sense
- Not everyone has S3 available

## Extras

- This needs to be Highly Available if folks are gonna use it
