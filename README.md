# org.pdactylifera.db
org.Db package for date palm (_Phoenix dactylifera_ L)

# Created using the makeOrgPackageFromNCBI function from AnnotationForge.
makeOrgPackageFromNCBI(
    version = "0.1",
    author = "crowmane <crowmane290@gmail.com>",
    maintainer = "crowmane <crowmane290@gmail.com>",
    outputDir = ".",
    tax_id = "42345",
    genus = "Phoenix",
    species = "dactylifera",
    rebuildCache = TRUE,
    NCBIFilesDir = "~/Phoenix_db"
)

# Make sure to run the following commands to if r-base-dev is not present.
sudo apt-get update
sudo apt-get install r-base-dev

# Install AnnotationDbi: Open an R session and run the BiocManager commands to install AnnotationDbi and its dependencies.
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install("AnnotationDbi")

# Install Your Custom org.db Package: Once the above dependencies are met.
install.packages("path/to/org.Pdactylifera.eg.db_0.1.tar.gz", repos = NULL, type = "source")
