# 2Wee

**The terminal application browser.**

Most internal tools get built twice. Once in Laravel — the models, the logic, the validation. Then again in the frontend — the forms, the components, the build pipeline. Two layers to maintain, two places for things to drift apart.

2Wee removes the second layer entirely.

You describe your screens in PHP. The 2Wee client renders them as a fast, keyboard-driven terminal interface. Your users never touch a mouse. Experienced operators move through records at the speed of muscle memory — faster than any web form.

---

## How it works

Your Laravel app returns JSON screen descriptions. The 2Wee client renders them as a rich terminal interface. The user interacts with keyboard only.

```
User ──keyboard──> 2Wee Client ──HTTPS──> Your Laravel App ──database──> Data
                      │                         │
                      │<── ScreenContract (JSON) ┘
                      │
                      v
                   Terminal
```

The client contains zero business logic. It does not know what a customer is, what an invoice looks like, or how to calculate a balance. It renders what your server sends.

---

## What you can build

- **Cards** — single-record forms with sections, fields, and drill-downs
- **Lists** — scrollable tables with type-to-search filtering
- **Documents** — headers with editable line item grids (sales orders, purchase orders)
- **Journals** — full-screen editable grids with totals and posting
- **Lookups** — relational field selection with autofill
- **Actions** — send email, print, export, post — any custom server-side operation
- **Menus** — nested navigation with tabs

All driven by your server. All keyboard-only. All fast.

---

## Try it

A live demo is running at **[demo.2wee.dev](https://demo.2wee.dev)** — a sample ERP with customers, sales orders, and purchase documents. No login required.

Or connect with the native client:

```sh
two_wee_client https://demo.2wee.dev
```

---

## Get started

→ **[docs.2wee.dev](https://docs.2wee.dev)**

---

## Heritage

In the 1980s, Navision built the fastest enterprise data entry system the world had ever seen. It ran in a terminal, was keyboard-only, and was so fast that experienced users could process invoices faster than the system could print them. The pattern was brilliant: the server owns all logic, the client just renders. No state, no sync, no drift.

2Wee picks up where that era left off — not as a clone, but as an evolution using modern technology. The same philosophy, the same speed, the same respect for the keyboard as the fastest input device ever made.

---

## Open protocol

2Wee is protocol-first. The JSON contract between client and server is open and documented. Laravel is the official server implementation, but any backend that speaks the protocol works — Rails, Django, Go, Express. The client does not know or care what generated the JSON.
