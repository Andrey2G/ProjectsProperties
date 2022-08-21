In case when solution have a lot of projects/libraries it's very hard to manage the Product details such as author, company, product name, version details.
There is a simple solution how to make life easier.

Just create a common file like Common.targets with the following content

```
<Project>
  <PropertyGroup>
    <Authors>It's me</Authors> 
    <Company>My Company</Company> 
    <Copyright>Copyright (C) 2022</Copyright> 
    <Product>The Product</Product> 
    <ProductName>The Product Name</ProductName> 
    <VersionPrefix>1.2.0.0</VersionPrefix> 
    <AssemblyVersion>1.2.3.0</AssemblyVersion> 
    <FileVersion>1.2.3.4</FileVersion> 
  </PropertyGroup> 
</Project>
```

And then just add a reference to this file in each .proj file from your big solution like this

```
<Import Project="..\Common.targets" />
```

In result you will get all those properties in all your assemlies like on ![this image!](/docs/sample.png)
