# Instructions

- Following Playwright test failed.
- Explain why, be concise, respect Playwright best practices.
- Provide a snippet of code with the fix, if possible.

# Test info

- Name: api\users.spec.ts >> Users API Tests >> PUT - Update User @master @regression @api
- Location: tests\api\users.spec.ts:80:9

# Error details

```
Error: expect(received).toBe(expected) // Object.is equality

Expected: 1
Received: undefined
```

# Test source

```ts
  1  | import { test, expect } from '@playwright/test';
  2  | import dotenv from 'dotenv';
  3  | import { Routes } from '../../api/endpoints/routes';
  4  | import { RandomDataUtil } from '../../utils/dataGenerator';
  5  | 
  6  | dotenv.config();
  7  | 
  8  | const BASE_URL = process.env.API_BASE_URL || Routes.BASE_URL;
  9  | const USER_ID = Number(process.env.USER_ID ?? 1);
  10 | const USER_LIMIT = Number(process.env.LIMIT ?? 3);
  11 | const userById = (id: number) => Routes.GET_USER_BY_ID.replace('{id}', String(id));
  12 | const userLimit = (limit: number) => Routes.GET_USERS_WITH_LIMIT.replace('{limit}', String(limit));
  13 | const userSort = (order: 'asc' | 'desc') => Routes.GET_USERS_SORTED.replace('{order}', order);
  14 | const userUpdate = (id: number) => Routes.UPDATE_USER.replace('{id}', String(id));
  15 | const userDelete = (id: number) => Routes.DELETE_USER.replace('{id}', String(id));
  16 | 
  17 | function assertUser(user: Record<string, unknown>): void {
  18 |     expect(user.id).toEqual(expect.any(Number));
  19 |     expect(user.email).toEqual(expect.any(String));
  20 |     expect(user.username).toEqual(expect.any(String));
  21 |     expect(user.name).toEqual(expect.objectContaining({ firstname: expect.any(String), lastname: expect.any(String) }));
  22 |     expect(user.address).toEqual(expect.any(Object));
  23 | }
  24 | 
  25 | // ---------------------------------------------------------
  26 | // Users - GET
  27 | // ---------------------------------------------------------
  28 | 
  29 | test.describe('Users API Tests', () => {
  30 |     test('GET - All Users @master @sanity @api', async ({ request }) => {
  31 |         const response = await request.get(`${BASE_URL}${Routes.GET_ALL_USERS}`);
  32 |         expect(response.status()).toBe(200);
  33 |         const users = await response.json();
  34 |         expect(Array.isArray(users)).toBeTruthy();
  35 |         expect(users.length).toBeGreaterThan(0);
  36 |         users.forEach(assertUser);
  37 |     });
  38 | 
  39 |     test('GET - User by ID @master @sanity @api', async ({ request }) => {
  40 |         const response = await request.get(`${BASE_URL}${userById(USER_ID)}`);
  41 |         expect(response.status()).toBe(200);
  42 |         const user = await response.json();
  43 |         assertUser(user);
  44 |         expect(user.id).toBe(USER_ID);
  45 |     });
  46 | 
  47 |     test('GET - Users with Limit @master @regression @api', async ({ request }) => {
  48 |         const response = await request.get(`${BASE_URL}${userLimit(USER_LIMIT)}`);
  49 |         expect(response.status()).toBe(200);
  50 |         const users = await response.json();
  51 |         expect(Array.isArray(users)).toBeTruthy();
  52 |         expect(users).toHaveLength(USER_LIMIT);
  53 |     });
  54 | 
  55 |     for (const order of ['asc', 'desc'] as const) {
  56 |         test(`GET - Users Sorted ${order} @master @regression @api`, async ({ request }) => {
  57 |             const response = await request.get(`${BASE_URL}${userSort(order)}`);
  58 |             expect(response.status()).toBe(200);
  59 |             const ids = (await response.json()).map((user: { id: number }) => user.id);
  60 |             const expected = [...ids].sort((a, b) => order === 'asc' ? a - b : b - a);
  61 |             expect(ids).toEqual(expected);
  62 |         });
  63 |     }
  64 | 
  65 |     // ---------------------------------------------------------
  66 |     // Users - CRUD
  67 |     // ---------------------------------------------------------
  68 | 
  69 |     test('POST - Create User @master @regression @api', async ({ request }) => {
  70 |         const payload = RandomDataUtil.generateUserPayload();
  71 |         const response = await request.post(`${BASE_URL}${Routes.CREATE_USER}`, { data: payload });
  72 |         expect(response.status()).toBe(201);
  73 |         const created = await response.json();
  74 |         expect(created.id).toEqual(expect.any(Number));
  75 |         expect(created.email).toBe(payload.email);
  76 |         expect(created.username).toBe(payload.username);
  77 |         expect(created.name).toEqual(payload.name);
  78 |     });
  79 | 
  80 |     test('PUT - Update User @master @regression @api', async ({ request }) => {
  81 |         const payload = RandomDataUtil.generateUserUpdatePayload();
  82 |         const response = await request.put(`${BASE_URL}${userUpdate(USER_ID)}`, { data: payload });
  83 |         expect(response.status()).toBe(200);
  84 |         const updated = await response.json();
> 85 |         expect(updated.id).toBe(USER_ID);
     |                            ^ Error: expect(received).toBe(expected) // Object.is equality
  86 |         expect(updated.username).toBe(payload.username);
  87 |         expect(updated.email).toBe(payload.email);
  88 |     });
  89 | 
  90 |     test('DELETE - User @master @regression @api', async ({ request }) => {
  91 |         const response = await request.delete(`${BASE_URL}${userDelete(USER_ID)}`);
  92 |         expect(response.status()).toBe(200);
  93 |         const deleted = await response.json();
  94 |         expect(deleted.id).toBe(USER_ID);
  95 |     });
  96 | });
  97 | 
```