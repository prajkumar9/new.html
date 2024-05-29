<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Product Viewer</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        .product {
            border: 1px solid #ddd;
            padding: 10px;
            margin: 10px;
        }
        .contact-info {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>My Products</h1>
    <div id="product-list">
        <!-- Products will be loaded here dynamically -->
    </div>

    <div class="contact-info">
        <h2>Contact Information</h2>
        <p>Email: <a href="mailto:your-email@example.com">your-email@example.com</a></p>
        <p>Phone: 123-456-7890</p>
    </div>

    <script>
        const products = [
            { name: "Product 1", description: "Description for product 1", price: "$10" },
            { name: "Product 2", description: "Description for product 2", price: "$20" },
            // Add more products as needed
        ];

        const productList = document.getElementById('product-list');

        products.forEach(product => {
            const productDiv = document.createElement('div');
            productDiv.className = 'product';

            const productName = document.createElement('h2');
            productName.textContent = product.name;
            productDiv.appendChild(productName);

            const productDescription = document.createElement('p');
            productDescription.textContent = product.description;
            productDiv.appendChild(productDescription);

            const productPrice = document.createElement('p');
            productPrice.textContent = product.price;
            productDiv.appendChild(productPrice);

            productList.appendChild(productDiv);
        });
    </script>
</body>
</html>
