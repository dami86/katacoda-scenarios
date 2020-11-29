1. Prepere action in controller
Go to your controller file
Inside aciton index put:

`
        $product = new Product();
        $category = new Category();

        $productForm = $this->createForm(ProductType::class, $product);
        $categoryForm = $this->createForm(CategoryType::class, $category);
        return $this->render('product/index.html.twig', [
            'productForm' => $productForm->createView(),
            'categoryForm' => $categoryForm->createView()
        ]);
`

2. After create controller there is also prepared view in 
`templates/form/index.html.twig`{{open}}

Open this file and put between block body
{% block body %}
{{ form(productForm) }}
{{ form(categoryForm) }}
{% endblock %}