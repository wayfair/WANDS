# WANDS - Wayfair ANnotation Dataset

[![OSS Template Version](https://img.shields.io/badge/OSS%20Template-0.3.5-7f187f.svg)](https://github.com/wayfair/WANDS/blob/main/CHANGELOG.md)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.0-4baaaa.svg)](CODE_OF_CONDUCT.md)

## About The Project

WANDS is a Wayfair product search relevance dataset that is published as a companion to the paper from ECIR 2022:

> WANDS: Dataset for Product Search Relevance Assessment  
> Yan Chen, Shujian Liu, Zheng Liu, Weiyi Sun, Linas Baltrunas and Benjamin Schroeder

The dataset allows objective benchmarking and evaluation of search engines on an E-Commerce dataset. Key features of this dataset includes:

1. 42,994 candidate products
2. 480 queries
3. 233,448 (query,product) relevance judgements

Please refer to the paper for more details.

## Getting Started

To get a local copy up and running follow these simple steps.

### Installation

Clone the repo

   ```sh
   git clone https://github.com/wayfair/WANDS.git
   ```

## Dataset Details

The data is stored in the ```dataset``` folder in three files:

1. ```product.csv``` - Stores all candidate products, columns include:  
   a. product_id - ID of a product  
   b. product_name - String of product name  
   c. product_class - Category which product falls under  
   d. category_hierarchy - Parent categories of product, delimited by ```/```  
   e. product_description - String description of product  
   f. product_features -  ```|``` delimited string of attribute:value pairs which describe the product  
   g. rating_count - Number of user ratings for product  
   h. average_rating - Average rating the product received  
   i. review_count - Number of user reviews for product  

2. ```query.csv``` - Stores search queries, columns include:  
   a. query_id - unique ID for each query  
   b. query - query string  
   c. query_class - category to which the query falls under  

3. ```label.csv``` - Stores annotated (product,relevance judgement) pairs, columns include  
   a. id - Unique ID for each annotation  
   b. query_id - ID of the query this annotation is for  
   c. product_id - ID of the product this annotation applies to  
   d. label - Relevance label, one of 'Exact', 'Partial', or 'Irrelevant'  

### Sample Notebook

We have included a sample notebook ```read_dataset.ipynb``` to show you how you can read the data from the three CSV files easily.

### Annotation Guidelines

We released [annotation guidelines](Product%20Search%20Relevance%20Annotation%20Guidelines.pdf) as a supplement to the dataset.

## Roadmap

See the [open issues](https://github.com/wayfair/WANDS/issues) for a list of proposed features (and known issues).

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**. For detailed contributing guidelines, please see [CONTRIBUTING.md](CONTRIBUTING.md)

## License

Distributed under the `MIT` License. See `LICENSE` for more information.

## Contact

For questions or feedback, please reach out to `ecir2022data@gmail.com` or the first author of the referenced paper.

Project Link: [https://github.com/wayfair/WANDS](https://github.com/wayfair/WANDS)

## Citation

Please cite this paper if you are building on top of or using this dataset:

```
@InProceedings{wands,  
  title = {WANDS: Dataset for Product Search Relevance Assessment},  
  author = {Chen, Yan and Liu, Shujian and Liu, Zheng and Sun, Weiyi and Baltrunas, Linas and Schroeder, Benjamin},  
  booktitle = {Proceedings of the 44th European Conference on Information Retrieval},  
  year = {2022},  
  numpages = {12}  
}
```
