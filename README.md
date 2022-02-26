<div align="center">
<img src="https://user-images.githubusercontent.com/1626923/137092657-fb398d20-b592-4661-a1f9-4135db0b61d5.png" height="80px"/>  
</div>

---------

# #TechForUkraine

<table>
  <tr>
    <td style="width:40%;">
       <img src="https://user-images.githubusercontent.com/1626923/155853691-d6d0a541-d3b9-40bf-b8f5-2d38303e9e49.png" />
    </td>
    <td>
      <h2><strong>Ongoing tensions on Ukrainian territory close the space for civil society.</strong></h2>
      <h3>How can you support Ukrainian civil society?</h3>
      All the help is valid, and if you are not able to help locally, by giving shelter to a fellow Ukraine, there are some ways that you can help also:
      <ul>
        <li>
          Support the Ukraine Armed forces directly by sending funding to the open special accounts.<br />
          <a href="https://bank.gov.ua/en/news/all/natsionalniy-bank-vidkriv-spetsrahunok-dlya-zboru-koshtiv-na-potrebi-armiyi" target="_blank">NBU Opens Special Account to Raise Funds for Ukraine’s Armed Forces</a>
        </li>
        <li>
          Help the ICRC (Red Cross) with donations.<br />
          <a href="https://www.icrc.org/en/where-we-work/europe-central-asia/ukraine" target="_blank">Ukrainian Red Cross Society</a>
        </li>
        <li>
          Donate to the United Help Ukraine.<br />
          <a href="https://unitedhelpukraine.org/" target="_blank">United Help Ukraine</a>
        </li>
        <li>
          Donate to Voices of Children<br />
          <a href="https://voices.org.ua/en/" target="_blank">Voices of Children</a>
        </li>
    </td>
  </tr>
</table>

---------

## Vue Storefront 2 integration with woocommerce

<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

## Wordpress config
1. Install the following open source Wordpress Plugins into your WP store:
   - [WPGraphQL CORS](https://github.com/funkhaus/wp-graphql-cors)
   - [WPGraphQL WooCommerce (WooGraphQL)](https://github.com/wp-graphql/wp-graphql-woocommerce)
2. add this to wp-config.php: `define( 'LOGGED_IN_COOKIE', 'wordpress_logged_in_vsf' );`
3. If you want favourites function you must add a plugin for this. See example plugin [here](https://github.com/Oxyssweden/vsf-woocommerce-plugin-examples/tree/main). You also need to enable favourites in middleware config:
```
module.exports = {
   integrations: {
      woocommerce: {
         location: '@vue-storefront/woocommerce-api/server',
         configuration: {
            api: process.env.WOOCOMMERCE_GRAPHQL,
            wishlist: true
         }
      }
   }
};
```
4. If you want to keep using the woocommerce checkout you need to change the woo cart session handling. See example plugin [here](https://github.com/Oxyssweden/vsf-woocommerce-plugin-examples/tree/main).

## How to start?

1. Prepare your wordpress installation as above.

2. Copy .env.example to .env inside packages/theme and enter your wordpress site URL with GraphQL endpoint.

3. Install all required dependencies:

```sh
yarn install
```

5. (optional) Then you can verify if everything works properly by building all three projects:

```sh
yarn build
```

6. If everything built properly, you can start developing with:

```sh
yarn dev
```

## How to start if you want to contribute?

Want to contribute? Ping us on `woocommerce` channel on [our Discord](https://discord.vuestorefront.io)!

### Requirements:
- NodeJS v14 or later

### Steps
1. Fork the repo
2. Clone your fork of the repo
    ```
    example:
    git clone https://github.com/vuestorefront/woocommerce.git
    cd woocommerce
    ```
3. Run `yarn` to install dependencies
4. Build dependencies `yarn build:api-client && yarn build:composables`
5. Run `yarn dev:theme` to run theme. You can find other commands in `package.json`

- If you need HMR on Api Client/Composables run `yarn dev:api-client` or `yarn dev:composables` on a separate terminal window.

## Resources

- [Vue Storefront Documentation](https://docs.vuestorefront.io/v2/)
- [woocommerce integration Documentation](https://docs.vuestorefront.io/woocommerce)
- [Community Chat](https://discord.vuestorefront.io)

## Support

If you have any questions about this integration we will be happy to answer them on `woocommerce` channel on [our Discord](discord.vuestorefront.io).

## Contributors ✨

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://github.com/andreasradloff"><img src="https://avatars.githubusercontent.com/u/1256982?v=4?s=80" width="80px;" alt=""/><br /><sub><b>andreasradloff</b></sub></a><br /><a href="https://github.com/vuestorefront/woocommerce/commits?author=andreasradloff" title="Code">💻</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
