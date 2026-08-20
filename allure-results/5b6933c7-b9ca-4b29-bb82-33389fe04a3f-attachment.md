# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: api\carts.spec.ts >> Carts API Tests >> POST - Create Cart @master @regression @api
- Location: tests\api\carts.spec.ts:95:9

# Error details

```
Error: Days must be greater than 0.
```

# Test source

```ts
  1   | import { faker } from '@faker-js/faker';
  2   | 
  3   | export class RandomDataUtil {
  4   | 
  5   |     // ─── Person ─────────────────────────────────────────────────
  6   |     static getFirstName(): string {
  7   |         return faker.person.firstName();
  8   |     }
  9   | 
  10  |     static getLastName(): string {
  11  |         return faker.person.lastName();
  12  |     }
  13  | 
  14  |     static getFullName(): string {
  15  |         return faker.person.fullName();
  16  |     }
  17  | 
  18  |     static getEmail(): string {
  19  |         return faker.internet.email();
  20  |     }
  21  | 
  22  |     static getPhoneNumber(): string {
  23  |         return faker.phone.number();
  24  |     }
  25  | 
  26  |     static getUsername(): string {
  27  |         return faker.internet.username();
  28  |     }
  29  | 
  30  |     static getPassword(length: number = 10): string {
  31  |         return faker.internet.password({ length });
  32  |     }
  33  | 
  34  |     static getCountry(): string {
  35  |         return faker.location.country();
  36  |     }
  37  | 
  38  |     static getState(): string {
  39  |         return faker.location.state();
  40  |     }
  41  | 
  42  |     static getCity(): string {
  43  |         return faker.location.city();
  44  |     }
  45  | 
  46  |     static getStreet(): string {
  47  |         return faker.location.street();
  48  |     }
  49  | 
  50  |     static getStreetAddress(): string {
  51  |         return faker.location.streetAddress();
  52  |     }
  53  | 
  54  |     static getZipCode(): string {
  55  |         return faker.location.zipCode();
  56  |     }
  57  | 
  58  |     static getLatitude(): string {
  59  |         return faker.location.latitude().toString();
  60  |     }
  61  | 
  62  |     static getLongitude(): string {
  63  |         return faker.location.longitude().toString();
  64  |     }
  65  | 
  66  |     // ─── Date & Time ────────────────────────────────────────────
  67  |     static getCurrentDate(): string {
> 68  |         return faker.date.recent({ days: 0 }).toISOString().split('T')[0];
      |                           ^ Error: Days must be greater than 0.
  69  |     }
  70  | 
  71  |     static getRecentDate(days: number = 10): string {
  72  |         return faker.date.recent({ days }).toISOString().split('T')[0];
  73  |     }
  74  | 
  75  |     static getFutureDate(years: number = 1): string {
  76  |         const date = new Date();
  77  |         date.setFullYear(date.getFullYear() + years);
  78  |         return faker.date.between({ from: new Date(), to: date }).toISOString().split('T')[0];
  79  |     }
  80  | 
  81  |     static getPastDate(years: number = 1): string {
  82  |         const date = new Date();
  83  |         date.setFullYear(date.getFullYear() - years);
  84  |         return faker.date.between({ from: date, to: new Date() }).toISOString().split('T')[0];
  85  |     }
  86  | 
  87  |     // ─── Commerce ───────────────────────────────────────────────
  88  |     static getProductName(): string {
  89  |         return faker.commerce.productName();
  90  |     }
  91  | 
  92  |     static getProductDescription(): string {
  93  |         return faker.commerce.productDescription();
  94  |     }
  95  | 
  96  |     static getProductPrice(): string {
  97  |         return faker.commerce.price({ min: 1, max: 500, dec: 2 });
  98  |     }
  99  | 
  100 |     static getDepartment(): string {
  101 |         return faker.commerce.department();
  102 |     }
  103 | 
  104 |     static getImageUrl(): string {
  105 |         return faker.image.url();
  106 |     }
  107 | 
  108 |     static getNumber(): number {
  109 |         return faker.number.int({ min: 1, max: 999 });
  110 |     }
  111 | 
  112 |     // ─── API Payload Generators ─────────────────────────────────
  113 |     static generateInvalidLoginPayload() {
  114 |         return {
  115 |             username: this.getUsername(),
  116 |             password: this.getPassword(),
  117 |         };
  118 |     }
  119 | 
  120 |     static generateProductPayload() {
  121 |         return {
  122 |             title: this.getProductName(),
  123 |             price: parseFloat(this.getProductPrice()),
  124 |             description: this.getProductDescription(),
  125 |             image: this.getImageUrl(),
  126 |             category: this.getDepartment().toLowerCase(),
  127 |         };
  128 |     }
  129 | 
  130 |     static generateUpdatedProductPayload() {
  131 |         return {
  132 |             title: `Updated ${this.getProductName()}`,
  133 |             price: parseFloat(this.getProductPrice()),
  134 |             description: this.getProductDescription(),
  135 |             image: this.getImageUrl(),
  136 |             category: this.getDepartment().toLowerCase(),
  137 |         };
  138 |     }
  139 | 
  140 |     static generateUserPayload() {
  141 |         const firstname = this.getFirstName();
  142 |         const lastname = this.getLastName();
  143 |         return {
  144 |             email: this.getEmail(),
  145 |             username: this.getUsername(),
  146 |             password: this.getPassword(),
  147 |             name: {
  148 |                 firstname,
  149 |                 lastname,
  150 |             },
  151 |             address: {
  152 |                 city: this.getCity(),
  153 |                 street: this.getStreet(),
  154 |                 number: this.getNumber(),
  155 |                 zipcode: this.getZipCode(),
  156 |                 geolocation: {
  157 |                     lat: this.getLatitude(),
  158 |                     long: this.getLongitude(),
  159 |                 },
  160 |             },
  161 |             phone: this.getPhoneNumber(),
  162 |         };
  163 |     }
  164 | 
  165 |     static generateUserUpdatePayload() {
  166 |         const payload = this.generateUserPayload();
  167 |         payload.username = `updated-${payload.username}`;
  168 |         return payload;
```