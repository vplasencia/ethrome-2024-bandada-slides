---
# try also 'default' to start simple
theme: default
# background: "black"
# some information about your slides, markdown enabled
fonts:
  # basically the text
  sans: Poppins
  # use with `font-serif` css class from UnoCSS
  serif: Poppins
  # for code blocks, inline code, etc.
  mono: Fira Code
title: Bandada - Managing Privacy-Preserving Groups
info: |
  ## Bandada ETHDam 2024
  Presentation slides for ETHDam 2024.

  Learn more at [Bandada](https://docs.bandada.pse.dev)
# apply any unocss classes to the current slide
class: text-center
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# https://sli.dev/guide/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/guide/syntax#mdc-syntax
mdc: true
hideInToc: true
---

# Bandada: Managing Privacy-Preserving Groups

<div class="text-25px opacity-85">
Vivian Plasencia
</div>

<img
  class="absolute top-2 left-2 w-10"
  src="/flock-1.svg"
  alt="Flock"
/>

<div class="abs-b mb-12 ml-6 flex text-12px opacity-70">
  <p>ETHDam 2024</p>
</div>

<div class="abs-b m-6 flex text-12px opacity-70">
  <p>Privacy & Scaling Explorations | Ethereum Foundation</p>
</div>

<div class="abs-br m-6">
  <a href="https://github.com/vplasencia/ethdam-2024-bandada-slides" target="_blank" alt="GitHub" title="Open in GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #FF5242 10%, #EB179B 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
layout: two-cols
layoutClass: gap-16
hideInToc: true
---

# Structure

<br>

<Toc minDepth="1" maxDepth="1" listClass=""></Toc>

::right::

<img
  src="/bandada-birds.svg"
  alt=""
/>

---
transition: slide-left
layoutClass: gap-16
layout: two-cols
---

# What is Bandada?

<br>

<img
  class="center"
  src="/birds.jpeg"
  alt="Birds"
/>

<a href="https://docs.bandada.pse.dev/" target="_blank" alt="Docs" title="Bandada docs" class="text-center">
<span>https://docs.bandada.pse.dev/</span>
</a>

::right::

Bandada is an infrastructure to manage privacy-preserving groups. It also provides antisybil mechanisms by using credential groups so that you can only join a group if you meet a specific criteria.

Bandada is a public good project. It is free and open source. Everyone can use it and contribute to it.

<br>

- Bandada is a Spanish word that means group of birds. It is the same as the English word flock.

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<!--
Here is another comment.
-->

---
transition: slide-left
---

# Use cases

<br>

- Platforms for DAOs

- Group of people in a private organization

- Group with members who have contributed to a specific GitHub repository

- Groups of wallets holding a specific NFT

- Group of members with +500 Twitter (X) followers

- Group of people with +300 number of transactions on a specific network

<br>

Ideas to build with Bandada: [https://github.com/orgs/bandada-infra/discussions/367](https://github.com/orgs/bandada-infra/discussions/367)

---
transition: slide-left
layout: center
---

<img
  class="center w-[50rem]"
  src="/bandada-infrastructure.svg"
  alt=""
/>

---
transition: slide-up
---

# Functionalities

<br>

| Functionalities             | Off-chain | On-chain |
| --------------------------- | --------- | -------- |
| Create group(s)             | ✅        | ✅       |
| Update group(s)             | ✅        | ❌       |
| Remove group(s)             | ✅        | ❌       |
| Invite code to join a group | ✅        | ❌       |
| Credentials to join a group | ✅        | ❌       |
| Add member(s)               | ✅        | ✅       |
| Remove member(s)            | ✅        | ❌       |

---
transition: slide-up
---

# Credential Groups

<div class="flex justify-center items-center mt-[2rem]">
<img
  class="center w-[35rem]"
  src="/bandada-credentials.svg"
  alt="Bandada Credentials"
/>
</div>

<br>

<div class="flex justify-center items-center gap-2">
<div>Credentials package:</div>
<a href="https://github.com/bandada-infra/bandada/tree/main/libs/credentials" target="_blank">https://github.com/bandada-infra/bandada/tree/main/libs/credentials</a>
</div>

---
transition: slide-left
---

# Interact with Bandada

<br>

| Tools     | Off-chain | On-chain |
| --------- | --------- | -------- |
| API       | ✅        | ❌       |
| API SDK   | ✅        | ❌       |
| Dashboard | ✅        | ✅       |

<br>
<br>

❌ The Bandada on-chain groups are Semaphore groups at the moment, you can work with them using the Semaphore packages. More about Semaphore: https://semaphore.pse.dev/

---
transition: slide-up
layout: two-cols
layoutClass: gap-16
---

# Start using Bandada

<br>

There are 3 ways you can start using Bandada in your project:

<br>

- [API]()

- [API SDK]()

- [Boilerplate]()

::right::

<img
  class="center w-[12rem] rounded-md"
  src="/bandada-docs-qrcode.png"
  alt="Bandada docs"
/>

Bandada documentation

https://docs.bandada.pse.dev/

---
transition: slide-up
hideInToc: true
layout: iframe-right
url: https://api.bandada.pse.dev/
class: api-website
---

# API

<br>

The API has a list of endpoints to interact with the Bandada infrastructure.

It is compatible with any programming language that supports REST API requests.

<img
  class="center w-[10rem] rounded-md"
  src="/bandada-api-docs-qrcode.png"
  alt="Bandada API docs"
/>

[https://api.bandada.pse.dev/](https://api.bandada.pse.dev/)

---
transition: slide-up
layout: two-cols
hideInToc: true
layoutClass: gap-16
---

# API SDK

<br>

The API SDK is a wrapper of the API.

It is a JavaScript package that provides a list of functions to make it easier to work with the Bandada API.

<br>

#### Install the API SDK package

```bash
npm install @bandada/api-sdk
```

<br>

https://docs.bandada.pse.dev/api/api-sdk

::right::

<img
  class="center w-[12rem] rounded-md"
  src="/bandada-api-sdk-demo-qrcode.png"
  alt="Bandada API SDK demo"
/>

API SDK Demo

https://github.com/bandada-infra/bandada-sdk-demo

---
transition: slide-up
hideInToc: true
---

# API SDK Example

```ts {all|1-3|5-14|16-18|20|all}
import { ApiSdk, GroupCreationDetails } from "@bandada/api-sdk"

const apiSdk = new ApiSdk()

const apiKey = "70f07d0d-6aa2-4fe1-b4b9-06c271a641dc"

const groupCreationDetails: GroupCreationDetails = {
  name: "Group 1",
  description: "This is Group 1",
  treeDepth: 16,
  fingerprintDuration: 3600
}

const group = await apiSdk.createGroup(groupCreationDetails, apiKey)

const members = ["1", "2", "3"]

await apiSdk.addMembersByApiKey(group.id, members, apiKey)

await apiSdk.removeMemberByApiKey(group.id, "1", apiKey)
```

---
transition: slide-left
hideInToc: true
---

# Boilerplate

<br>

<div class="flex justify-between items-center">
<div>
<div>Boilerplate live app:</div>
<a href="https://demo.bandada.pse.dev/" target="_blank">https://demo.bandada.pse.dev/</a>
</div>
<img
  class="w-[10rem] rounded-md"
  src="/bandada-boilerplate-live-app-qrcode.png"
  alt="Bandada API SDK demo"
/>
</div>

<br>

You can fork it, clone it or use it as a template:

https://github.com/bandada-infra/boilerplate

<img
  class="center"
  src="/bandada-boilerplate-repo.png"
  alt="Bandada boilerplate repo"
/>

---
transition: slide-left
layout: center
---

<img
  class="center w-[38rem]"
  src="/bandada-semaphore-off-chain-app-architecture.svg"
  alt="Bandada Semaphore off-chain app architecture"
/>

---
transition: slide-left
---

# Roadmap

<br>

- Improve user experience and developer experience (Documentation, SDKs, CLI, templates).

- Integrate other protocols like POAP, Zupass, etc.

- Logical operators for credentials, create groups with multiple credentials.

- Work on on-chain groups to have the same functionalities that off-chain groups have now (join groups with invite link, credential groups, etc.).

- Build a modular architecture that supports several data structures and different types of groups.

https://github.com/orgs/bandada-infra/discussions/350

---
transition: slide-up
layout: two-cols
layoutClass: gap-16
---

# Hacker Guide

<br>

Document with the main Bandada information and links for hackers.

<br>

<img
  class="w-[15rem] rounded-md"
  src="/bandada-hackathon-guide-qrcode.png"
  alt="Bandada hackathon guide qrcode"
/>

::right::

<img
  src="/bandada-birds.svg"
  alt="Bandada birds"
/>

---
transition: slide-left
layout: two-cols
layoutClass: gap-16
hideInToc: true
---

# Presentation slides

<br>

This presentation is open source, you can check the slides and code.

<br>

<img
  class="w-[15rem] rounded-md"
  src="/presentation-qrcode.png"
  alt="Presentation qrcode"
/>

::right::

<img
  src="/bandada-birds.svg"
  alt="Bandada birds"
/>

---
transition: slide-up
layout: two-cols
layoutClass: gap-16
hideInToc: true
---

# Connect

<br>

<div class="text-center w-50">

<img
  class="rounded-full w-50"
  src="/vivianAvatar.jpg"
  alt=""
/>

<div>Vivian Plasencia</div>
</div>

::right::

<img
  class="flex top-2 left-2 w-50 justify-center align-center rounded-md"
  src="/vivian-telegram-qrcode.png"
  alt="Flock"
/>

<div class="flex gap-2 items-center">
<h3>Telegram</h3>
<a href="https://t.me/vivianpc" target="_blank" alt="Telegram" class="text-center">
<span>vivianpc</span>
</a>
</div>

<br>
<br>
<br>

<div class="flex gap-2 items-center">
<h3>GitHub</h3>
<a href="https://github.com/vplasencia" target="_blank" alt="Github" class="text-center">
<span>vplasencia</span>
</a>
</div>

<br>
<br>

<div class="flex gap-2 items-center">
<h3>Discord - </h3>
<span>vivianplasencia</span>
</div>
