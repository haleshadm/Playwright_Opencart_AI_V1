# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: web\add-to-cart-flow.spec.ts >> Add Product to Cart @master @sanity @regression @web
- Location: tests\web\add-to-cart-flow.spec.ts:21:5

# Error details

```
Test timeout of 30000ms exceeded.
```

```
Error: expect(received).toBeTruthy()

Received: false
```

# Page snapshot

```yaml
- generic [active] [ref=f3e1]:
  - navigation [ref=f3e2]:
    - generic [ref=f3e3]:
      - button "$ Currency " [ref=f3e7] [cursor=pointer]:
        - strong [ref=f3e8]: $
        - text: Currency
        - generic [ref=f3e9]: 
      - list [ref=f3e11]:
        - listitem [ref=f3e12]:
          - link "" [ref=f3e13] [cursor=pointer]:
            - /url: http://localhost/opencart/upload/index.php?route=information/contact
          - text: "123456789"
        - listitem [ref=f3e15]:
          - link " My Account" [ref=f3e16] [cursor=pointer]:
            - /url: http://localhost/opencart/upload/index.php?route=account/account
            - generic [ref=f3e17]: 
            - text: My Account
        - listitem [ref=f3e19]:
          - link " Wish List (0)" [ref=f3e20] [cursor=pointer]:
            - /url: http://localhost/opencart/upload/index.php?route=account/wishlist
            - generic [ref=f3e21]: 
            - text: Wish List (0)
        - listitem [ref=f3e22]:
          - link " Shopping Cart" [ref=f3e23] [cursor=pointer]:
            - /url: http://localhost/opencart/upload/index.php?route=checkout/cart
            - generic [ref=f3e24]: 
            - text: Shopping Cart
        - listitem [ref=f3e25]:
          - link " Checkout" [ref=f3e26] [cursor=pointer]:
            - /url: http://localhost/opencart/upload/index.php?route=checkout/checkout
            - generic [ref=f3e27]: 
            - text: Checkout
  - banner [ref=f3e28]:
    - generic [ref=f3e30]:
      - link [ref=f3e33] [cursor=pointer]:
        - /url: http://localhost/opencart/upload/index.php?route=common/home
        - img "Your Store" [ref=f3e34]
      - generic [ref=f3e36]:
        - textbox "Search" [ref=f3e37]
        - button "" [ref=f3e39] [cursor=pointer]
      - generic [ref=f3e42]:
        - button " 2 item(s) - $1,204.00" [ref=f3e43] [cursor=pointer]:
          - generic [ref=f3e44]: 
          - text: 2 item(s) - $1,204.00
        - text:   
  - navigation [ref=f3e46]:
    - generic: 
    - list [ref=f3e48]:
      - listitem [ref=f3e49]:
        - link "Desktops" [ref=f3e50] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=20
      - listitem [ref=f3e51]:
        - link "Laptops & Notebooks" [ref=f3e52] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=18
      - listitem [ref=f3e53]:
        - link "Components" [ref=f3e54] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=25
      - listitem [ref=f3e55]:
        - link "Tablets" [ref=f3e56] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=57
      - listitem [ref=f3e57]:
        - link "Software" [ref=f3e58] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=17
      - listitem [ref=f3e59]:
        - link "Phones & PDAs" [ref=f3e60] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=24
      - listitem [ref=f3e61]:
        - link "Cameras" [ref=f3e62] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=33
      - listitem [ref=f3e63]:
        - link "MP3 Players" [ref=f3e64] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=34
  - generic [ref=f3e65]:
    - list [ref=f3e66]:
      - listitem [ref=f3e67]:
        - link "" [ref=f3e68] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=common/home
      - listitem [ref=f3e70]:
        - link "Shopping Cart" [ref=f3e71] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=checkout/cart
    - generic [ref=f3e73]:
      - heading "Shopping Cart (0.00kg)" [level=1] [ref=f3e74]
      - table [ref=f3e77]:
        - rowgroup [ref=f3e78]:
          - row [ref=f3e79]:
            - cell "Image" [ref=f3e80]
            - cell "Product Name" [ref=f3e81]
            - cell "Model" [ref=f3e82]
            - cell "Quantity" [ref=f3e83]
            - cell "Unit Price" [ref=f3e84]
            - cell "Total" [ref=f3e85]
        - rowgroup [ref=f3e86]:
          - row [ref=f3e87]:
            - cell [ref=f3e88]:
              - link [ref=f3e89] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=product/product&product_id=43
                - img "MacBook" [ref=f3e90]
            - cell [ref=f3e91]:
              - link "MacBook" [ref=f3e92] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=product/product&product_id=43
              - text: "Reward Points: 1200"
            - cell "Product 16" [ref=f3e93]
            - cell [ref=f3e94]:
              - generic [ref=f3e95]:
                - textbox [ref=f3e96]: "2"
                - generic [ref=f3e97]:
                  - button "" [ref=f3e98] [cursor=pointer]
                  - button "" [ref=f3e100] [cursor=pointer]
            - cell "$602.00" [ref=f3e102]
            - cell "$1,204.00" [ref=f3e103]
      - heading "What would you like to do next?" [level=2] [ref=f3e104]
      - paragraph [ref=f3e105]: Choose if you have a discount code or reward points you want to use or would like to estimate your delivery cost.
      - generic [ref=f3e106]:
        - heading [level=4] [ref=f3e109]:
          - link "Use Coupon Code " [ref=f3e110] [cursor=pointer]:
            - /url: "#collapse-coupon"
            - text: Use Coupon Code
            - generic [ref=f3e111]: 
        - heading [level=4] [ref=f3e114]:
          - link "Use Gift Certificate " [ref=f3e115] [cursor=pointer]:
            - /url: "#collapse-voucher"
            - text: Use Gift Certificate
            - generic [ref=f3e116]: 
      - table [ref=f3e119]:
        - rowgroup [ref=f3e120]:
          - row [ref=f3e121]:
            - cell [ref=f3e122]:
              - strong [ref=f3e123]: "Sub-Total:"
            - cell "$1,000.00" [ref=f3e124]
          - row [ref=f3e125]:
            - cell [ref=f3e126]:
              - strong [ref=f3e127]: "Eco Tax (-2.00):"
            - cell "$4.00" [ref=f3e128]
          - row [ref=f3e129]:
            - cell [ref=f3e130]:
              - strong [ref=f3e131]: "VAT (20%):"
            - cell "$200.00" [ref=f3e132]
          - row [ref=f3e133]:
            - cell [ref=f3e134]:
              - strong [ref=f3e135]: "Total:"
            - cell "$1,204.00" [ref=f3e136]
      - generic [ref=f3e137]:
        - link "Continue Shopping" [ref=f3e139] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=common/home
        - link "Checkout" [ref=f3e141] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=checkout/checkout
  - contentinfo [ref=f3e142]:
    - generic [ref=f3e143]:
      - generic [ref=f3e144]:
        - generic [ref=f3e145]:
          - heading "Information" [level=5] [ref=f3e146]
          - list [ref=f3e147]:
            - listitem [ref=f3e148]:
              - link "About Us" [ref=f3e149] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=information/information&information_id=4
            - listitem [ref=f3e150]:
              - link "Delivery Information" [ref=f3e151] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=information/information&information_id=6
            - listitem [ref=f3e152]:
              - link "Privacy Policy" [ref=f3e153] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=information/information&information_id=3
            - listitem [ref=f3e154]:
              - link "Terms & Conditions" [ref=f3e155] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=information/information&information_id=5
        - generic [ref=f3e156]:
          - heading "Customer Service" [level=5] [ref=f3e157]
          - list [ref=f3e158]:
            - listitem [ref=f3e159]:
              - link "Contact Us" [ref=f3e160] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=information/contact
            - listitem [ref=f3e161]:
              - link "Returns" [ref=f3e162] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=account/return/add
            - listitem [ref=f3e163]:
              - link "Site Map" [ref=f3e164] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=information/sitemap
        - generic [ref=f3e165]:
          - heading "Extras" [level=5] [ref=f3e166]
          - list [ref=f3e167]:
            - listitem [ref=f3e168]:
              - link "Brands" [ref=f3e169] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=product/manufacturer
            - listitem [ref=f3e170]:
              - link "Gift Certificates" [ref=f3e171] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=account/voucher
            - listitem [ref=f3e172]:
              - link "Affiliate" [ref=f3e173] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=affiliate/login
            - listitem [ref=f3e174]:
              - link "Specials" [ref=f3e175] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=product/special
        - generic [ref=f3e176]:
          - heading "My Account" [level=5] [ref=f3e177]
          - list [ref=f3e178]:
            - listitem [ref=f3e179]:
              - link "My Account" [ref=f3e180] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=account/account
            - listitem [ref=f3e181]:
              - link "Order History" [ref=f3e182] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=account/order
            - listitem [ref=f3e183]:
              - link "Wish List" [ref=f3e184] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=account/wishlist
            - listitem [ref=f3e185]:
              - link "Newsletter" [ref=f3e186] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=account/newsletter
      - separator [ref=f3e187]
      - paragraph [ref=f3e188]:
        - text: Powered By
        - link "OpenCart" [ref=f3e189] [cursor=pointer]:
          - /url: http://www.opencart.com
        - text: Your Store © 2026
```

# Test source

```ts
  1  | /**
  2  |  * Test Case: Add Product to Cart
  3  |  *
  4  |  * Tags: @master @sanity @regression @web
  5  |  *
  6  |  * Steps:
  7  |  * 1) Open the application
  8  |  * 2) Search for a known product
  9  |  * 3) Open the product details page
  10 |  * 4) Verify the product details are displayed
  11 |  * 5) Set the required quantity
  12 |  * 6) Click Add to Cart
  13 |  * 7) Verify the success confirmation message
  14 |  * 8) Open the shopping cart
  15 |  * 9) Verify the product is present
  16 |  * 10) Verify the quantity matches
  17 |  */
  18 | 
  19 | import { test, expect } from '../../fixtures/pageFixtures';
  20 | 
  21 | test('Add Product to Cart @master @sanity @regression @web', async ({ homePage, searchPage, productPage, cartPage }) => {
  22 | 
  23 |     const productName = 'MacBook';
  24 |     const quantity = '2';
  25 | 
  26 |     await test.step('1) Search for a known product', async () => {
  27 |         await homePage.searchProduct(productName);
  28 |     });
  29 | 
  30 |     await test.step('2) Open the product details page', async () => {
  31 |         await searchPage.clickProduct(productName);
  32 |     });
  33 | 
  34 |     await test.step('3) Verify the product details are displayed', async () => {
  35 |         const isProductPage = await productPage.isProductPageExists();
  36 |         expect(isProductPage).toBeTruthy();
  37 |         const name = await productPage.getProductName();
  38 |         expect(name).toContain(productName);
  39 |     });
  40 | 
  41 |     await test.step('4) Set the quantity and add to cart', async () => {
  42 |         await productPage.setQuantity(quantity);
  43 |         await productPage.clickAddToCart();
  44 |     });
  45 | 
  46 |     await test.step('5) Verify the success message is displayed', async () => {
  47 |         const successMsg = await productPage.getSuccessMessage();
  48 |         expect(successMsg).toContain('Success: You have added');
  49 |     });
  50 | 
  51 |     await test.step('6) Open the shopping cart', async () => {
  52 |         await cartPage.goto();
  53 |     });
  54 | 
  55 |     await test.step('7) Verify the product is present in the cart', async () => {
  56 |         const isCart = await cartPage.isCartPageExists();
  57 |         expect(isCart).toBeTruthy();
  58 |         const cartProductNames = await cartPage.getCartProductNames();
  59 |         const found = cartProductNames.some(name => name.includes(productName));
> 60 |         expect(found).toBeTruthy();
     |                       ^ Error: expect(received).toBeTruthy()
  61 |     });
  62 | 
  63 |     await test.step('8) Verify the quantity matches', async () => {
  64 |         const cartQty = await cartPage.getCartQuantity();
  65 |         expect(cartQty).toBe(quantity);
  66 |     });
  67 | 
  68 |     console.log('✅ Add Product to Cart completed successfully!');
  69 | });
```