# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: web\end-to-end-shopping-flow.spec.ts >> End-to-End Shopping Flow @master @end-to-end @regression @web
- Location: tests\web\end-to-end-shopping-flow.spec.ts:23:5

# Error details

```
Test timeout of 30000ms exceeded.
```

```
Error: expect(received).toBe(expected) // Object.is equality

Expected: "1"
Received: ""
```

# Page snapshot

```yaml
- generic [active] [ref=f10e1]:
  - navigation [ref=f10e2]:
    - generic [ref=f10e3]:
      - button "$ Currency " [ref=f10e7] [cursor=pointer]:
        - strong [ref=f10e8]: $
        - text: Currency
        - generic [ref=f10e9]: 
      - list [ref=f10e11]:
        - listitem [ref=f10e12]:
          - link "" [ref=f10e13] [cursor=pointer]:
            - /url: http://localhost/opencart/upload/index.php?route=information/contact
          - text: "123456789"
        - listitem [ref=f10e15]:
          - link " My Account" [ref=f10e16] [cursor=pointer]:
            - /url: http://localhost/opencart/upload/index.php?route=account/account
            - generic [ref=f10e17]: 
            - text: My Account
        - listitem [ref=f10e19]:
          - link " Wish List (0)" [ref=f10e20] [cursor=pointer]:
            - /url: http://localhost/opencart/upload/index.php?route=account/wishlist
            - generic [ref=f10e21]: 
            - text: Wish List (0)
        - listitem [ref=f10e22]:
          - link " Shopping Cart" [ref=f10e23] [cursor=pointer]:
            - /url: http://localhost/opencart/upload/index.php?route=checkout/cart
            - generic [ref=f10e24]: 
            - text: Shopping Cart
        - listitem [ref=f10e25]:
          - link " Checkout" [ref=f10e26] [cursor=pointer]:
            - /url: http://localhost/opencart/upload/index.php?route=checkout/checkout
            - generic [ref=f10e27]: 
            - text: Checkout
  - banner [ref=f10e28]:
    - generic [ref=f10e30]:
      - link [ref=f10e33] [cursor=pointer]:
        - /url: http://localhost/opencart/upload/index.php?route=common/home
        - img "Your Store" [ref=f10e34]
      - generic [ref=f10e36]:
        - textbox "Search" [ref=f10e37]
        - button "" [ref=f10e39] [cursor=pointer]
      - generic [ref=f10e42]:
        - button " 1 item(s) - $602.00" [ref=f10e43] [cursor=pointer]:
          - generic [ref=f10e44]: 
          - text: 1 item(s) - $602.00
        - text:   
  - navigation [ref=f10e46]:
    - generic: 
    - list [ref=f10e48]:
      - listitem [ref=f10e49]:
        - link "Desktops" [ref=f10e50] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=20
      - listitem [ref=f10e51]:
        - link "Laptops & Notebooks" [ref=f10e52] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=18
      - listitem [ref=f10e53]:
        - link "Components" [ref=f10e54] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=25
      - listitem [ref=f10e55]:
        - link "Tablets" [ref=f10e56] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=57
      - listitem [ref=f10e57]:
        - link "Software" [ref=f10e58] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=17
      - listitem [ref=f10e59]:
        - link "Phones & PDAs" [ref=f10e60] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=24
      - listitem [ref=f10e61]:
        - link "Cameras" [ref=f10e62] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=33
      - listitem [ref=f10e63]:
        - link "MP3 Players" [ref=f10e64] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=product/category&path=34
  - generic [ref=f10e65]:
    - list [ref=f10e66]:
      - listitem [ref=f10e67]:
        - link "" [ref=f10e68] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=common/home
      - listitem [ref=f10e70]:
        - link "Shopping Cart" [ref=f10e71] [cursor=pointer]:
          - /url: http://localhost/opencart/upload/index.php?route=checkout/cart
    - generic [ref=f10e73]:
      - heading "Shopping Cart" [level=1] [ref=f10e74]
      - paragraph [ref=f10e75]: Your shopping cart is empty!
      - link "Continue" [ref=f10e78] [cursor=pointer]:
        - /url: http://localhost/opencart/upload/index.php?route=common/home
  - contentinfo [ref=f10e79]:
    - generic [ref=f10e80]:
      - generic [ref=f10e81]:
        - generic [ref=f10e82]:
          - heading "Information" [level=5] [ref=f10e83]
          - list [ref=f10e84]:
            - listitem [ref=f10e85]:
              - link "About Us" [ref=f10e86] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=information/information&information_id=4
            - listitem [ref=f10e87]:
              - link "Delivery Information" [ref=f10e88] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=information/information&information_id=6
            - listitem [ref=f10e89]:
              - link "Privacy Policy" [ref=f10e90] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=information/information&information_id=3
            - listitem [ref=f10e91]:
              - link "Terms & Conditions" [ref=f10e92] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=information/information&information_id=5
        - generic [ref=f10e93]:
          - heading "Customer Service" [level=5] [ref=f10e94]
          - list [ref=f10e95]:
            - listitem [ref=f10e96]:
              - link "Contact Us" [ref=f10e97] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=information/contact
            - listitem [ref=f10e98]:
              - link "Returns" [ref=f10e99] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=account/return/add
            - listitem [ref=f10e100]:
              - link "Site Map" [ref=f10e101] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=information/sitemap
        - generic [ref=f10e102]:
          - heading "Extras" [level=5] [ref=f10e103]
          - list [ref=f10e104]:
            - listitem [ref=f10e105]:
              - link "Brands" [ref=f10e106] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=product/manufacturer
            - listitem [ref=f10e107]:
              - link "Gift Certificates" [ref=f10e108] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=account/voucher
            - listitem [ref=f10e109]:
              - link "Affiliate" [ref=f10e110] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=affiliate/login
            - listitem [ref=f10e111]:
              - link "Specials" [ref=f10e112] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=product/special
        - generic [ref=f10e113]:
          - heading "My Account" [level=5] [ref=f10e114]
          - list [ref=f10e115]:
            - listitem [ref=f10e116]:
              - link "My Account" [ref=f10e117] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=account/account
            - listitem [ref=f10e118]:
              - link "Order History" [ref=f10e119] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=account/order
            - listitem [ref=f10e120]:
              - link "Wish List" [ref=f10e121] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=account/wishlist
            - listitem [ref=f10e122]:
              - link "Newsletter" [ref=f10e123] [cursor=pointer]:
                - /url: http://localhost/opencart/upload/index.php?route=account/newsletter
      - separator [ref=f10e124]
      - paragraph [ref=f10e125]:
        - text: Powered By
        - link "OpenCart" [ref=f10e126] [cursor=pointer]:
          - /url: http://www.opencart.com
        - text: Your Store © 2026
```

# Test source

```ts
  1   | /**
  2   |  * Test Case: End-to-End Shopping Flow
  3   |  *
  4   |  * Tags: @master @end-to-end @regression @web
  5   |  *
  6   |  * Steps:
  7   |  * 1) Open the application
  8   |  * 2) Register a new customer
  9   |  * 3) Verify successful registration
  10  |  * 4) Log out
  11  |  * 5) Log in again with the new credentials
  12  |  * 6) Verify successful authentication
  13  |  * 7) Search for a known product
  14  |  * 8) Open the product details page
  15  |  * 9) Add the product to the cart
  16  |  * 10) Open the shopping cart
  17  |  * 11) Verify the correct product, quantity, price, and total
  18  |  */
  19  | 
  20  | import { test, expect } from '../../fixtures/pageFixtures';
  21  | import { RandomDataUtil } from '../../utils/dataGenerator';
  22  | 
  23  | test('End-to-End Shopping Flow @master @end-to-end @regression @web', async ({ homePage, registerPage, successPage, accountPage, loginPage, searchPage, productPage, cartPage, page }) => {
  24  | 
  25  |     // Generate unique customer data
  26  |     const firstName = RandomDataUtil.getFirstName();
  27  |     const lastName = RandomDataUtil.getLastName();
  28  |     const email = RandomDataUtil.getEmail();
  29  |     const telephone = RandomDataUtil.getPhoneNumber();
  30  |     const password = RandomDataUtil.getPassword(10);
  31  |     const productName = 'MacBook';
  32  |     const quantity = '1';
  33  | 
  34  |     await test.step('1) Navigate to the registration page', async () => {
  35  |         await homePage.clickRegister();
  36  |     });
  37  | 
  38  |     await test.step('2) Register a new customer', async () => {
  39  |         await registerPage.setFirstName(firstName);
  40  |         await registerPage.setLastName(lastName);
  41  |         await registerPage.setEmail(email);
  42  |         await registerPage.setTelephone(telephone);
  43  |         await registerPage.setPassword(password);
  44  |         await registerPage.setConfirmPassword(password);
  45  |         await registerPage.acceptPrivacyPolicy();
  46  |         await registerPage.clickContinue();
  47  |     });
  48  | 
  49  |     await test.step('3) Verify successful registration', async () => {
  50  |         const isSuccess = await successPage.isAccountCreatedSuccessPage();
  51  |         expect(isSuccess).toBeTruthy();
  52  |     });
  53  | 
  54  |     await test.step('4) Log out', async () => {
  55  |         await page.goto(`${process.env.WEB_APP_URL || 'http://localhost/opencart/upload/'}index.php?route=account/logout`);
  56  |         await page.locator('a:has-text("Continue")').click({ force: true });
  57  |     });
  58  | 
  59  |     await test.step('5) Log in with the new credentials', async () => {
  60  |         await page.goto(`${process.env.WEB_APP_URL || 'http://localhost/opencart/upload/'}index.php?route=account/login`);
  61  |         await loginPage.login(email, password);
  62  |     });
  63  | 
  64  |     await test.step('6) Verify successful authentication', async () => {
  65  |         const isLoggedIn = await accountPage.isMyAccountPageExists();
  66  |         expect(isLoggedIn).toBeTruthy();
  67  |     });
  68  | 
  69  |     await test.step('7) Search for a known product', async () => {
  70  |         await page.goto(`${process.env.WEB_APP_URL || 'http://localhost/opencart/upload/'}`);
  71  |         await homePage.searchProduct(productName);
  72  |     });
  73  | 
  74  |     await test.step('8) Open the product details page', async () => {
  75  |         await searchPage.clickProduct(productName);
  76  |     });
  77  | 
  78  |     await test.step('9) Add the product to the cart', async () => {
  79  |         await productPage.setQuantity(quantity);
  80  |         await productPage.clickAddToCart();
  81  |     });
  82  | 
  83  |     await test.step('10) Open the shopping cart', async () => {
  84  |         await cartPage.goto();
  85  |     });
  86  | 
  87  |     await test.step('11) Verify the product, quantity, and total', async () => {
  88  |         const isCart = await cartPage.isCartPageExists();
  89  |         expect(isCart).toBeTruthy();
  90  | 
  91  |         const cartProductNames = await cartPage.getCartProductNames();
  92  |         const found = cartProductNames.some(name => name.includes(productName));
  93  |         expect(found).toBeTruthy();
  94  | 
  95  |         const cartQty = await cartPage.getCartQuantity();
> 96  |         expect(cartQty).toBe(quantity);
      |                         ^ Error: expect(received).toBe(expected) // Object.is equality
  97  |     });
  98  | 
  99  |     console.log('✅ End-to-End Shopping Flow completed successfully!');
  100 | });
```