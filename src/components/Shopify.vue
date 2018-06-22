
<script>
export default {
  name: 'Shopify',
  template: '<Shopify />',
  render: function render(createElement) {
    const el = createElement('div', { attrs: { id: 'product-component-32413fdd2db' } });
    /* eslint-disable */
    var scriptURL = 'https://sdks.shopifycdn.com/buy-button/latest/buy-button-storefront.min.js';
    if (window.ShopifyBuy) {
      if (window.ShopifyBuy.UI) {
        ShopifyBuyInit();
      } else {
        loadScript();
      }
    } else {
      loadScript();
    }

    function loadScript() {
      var script = document.createElement('script');
      script.async = true;
      script.src = scriptURL;
      (document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(script);
      script.onload = ShopifyBuyInit;
    }

    function ShopifyBuyInit() {
      var client = ShopifyBuy.buildClient({
        domain: 'garlic-rocks.myshopify.com',
        apiKey: '382e4af896f38bb877c6ca6002823fa9',
        appId: '6',
      });

      ShopifyBuy.UI.onReady(client).then(function (ui) {
        ui.createComponent('product', {
          id: [1348004184182],
          node: document.getElementById('product-component-32413fdd2db'),
          moneyFormat: '%24%7B%7Bamount%7D%7D',
          options: {
            "product": {
              "buttonDestination": "checkout",
              "layout": "horizontal",
              "variantId": "all",
              "width": "100%",
              "contents": {
                "img": false,
                "imgWithCarousel": true,
                "variantTitle": false,
                "description": true,
                "buttonWithQuantity": true,
                "button": false,
                "quantity": false
              },
              "text": {
                "button": "BUY NOW"
              },
              "styles": {
                "product": {
                  "@media (min-width: 601px)": {
                    "max-width": "100%",
                    "margin-left": "0",
                    "margin-bottom": "50px"
                  }
                },
                "button": {
                  "background-color": "#363636",
                  "font-family": "Lato, sans-serif",
                  ":hover": {
                    "background-color": "#313131"
                  },
                  "font-weight": "bold",
                  ":focus": {
                    "background-color": "#313131"
                  }
                },
                "variantTitle": {
                  "font-family": "Lato, sans-serif",
                  "font-weight": "normal"
                },
                "title": {
                  "font-family": "Lato, sans-serif",
                  "font-weight": "normal",
                  "font-size": "26px"
                },
                "description": {
                  "font-family": "Lato, sans-serif",
                  "font-weight": "normal"
                },
                "price": {
                  "font-family": "Lato, sans-serif",
                  "font-size": "18px",
                  "font-weight": "normal"
                },
                "compareAt": {
                  "font-size": "15px",
                  "font-family": "Lato, sans-serif",
                  "font-weight": "normal"
                }
              },
              "googleFonts": [
                "Lato",
                "Lato",
                "Lato",
                "Lato",
                "Lato",
                "Lato"
              ]
            },
            "cart": {
              "contents": {
                "button": true
              },
              "styles": {
                "button": {
                  "background-color": "#363636",
                  "font-family": "Lato, sans-serif",
                  ":hover": {
                    "background-color": "#313131"
                  },
                  "font-weight": "bold",
                  ":focus": {
                    "background-color": "#313131"
                  }
                },
                "footer": {
                  "background-color": "#ffffff"
                }
              },
              "googleFonts": [
                "Lato"
              ]
            },
            "modalProduct": {
              "contents": {
                "img": false,
                "imgWithCarousel": true,
                "variantTitle": false,
                "buttonWithQuantity": true,
                "button": false,
                "quantity": false
              },
              "styles": {
                "product": {
                  "@media (min-width: 601px)": {
                    "max-width": "100%",
                    "margin-left": "0px",
                    "margin-bottom": "0px"
                  }
                },
                "button": {
                  "background-color": "#363636",
                  "font-family": "Lato, sans-serif",
                  ":hover": {
                    "background-color": "#313131"
                  },
                  "font-weight": "bold",
                  ":focus": {
                    "background-color": "#313131"
                  }
                },
                "variantTitle": {
                  "font-family": "Lato, sans-serif",
                  "font-weight": "normal"
                },
                "title": {
                  "font-family": "Lato, sans-serif",
                  "font-weight": "normal"
                },
                "description": {
                  "font-family": "Lato, sans-serif",
                  "font-weight": "normal"
                },
                "price": {
                  "font-family": "Lato, sans-serif",
                  "font-weight": "normal"
                },
                "compareAt": {
                  "font-family": "Lato, sans-serif",
                  "font-weight": "normal"
                }
              },
              "googleFonts": [
                "Lato",
                "Lato",
                "Lato",
                "Lato",
                "Lato",
                "Lato"
              ]
            },
            "toggle": {
              "styles": {
                "toggle": {
                  "font-family": "Lato, sans-serif",
                  "background-color": "#363636",
                  ":hover": {
                    "background-color": "#313131"
                  },
                  "font-weight": "bold",
                  ":focus": {
                    "background-color": "#313131"
                  }
                },
                "count": {
                  "color": "#ffffff",
                  ":hover": {
                    "color": "#ffffff"
                  }
                },
                "iconPath": {
                  "fill": "#ffffff"
                }
              },
              "googleFonts": [
                "Lato"
              ]
            },
            "option": {
              "styles": {
                "label": {
                  "font-family": "Lato, sans-serif"
                },
                "select": {
                  "font-family": "Lato, sans-serif"
                }
              },
              "googleFonts": [
                "Lato",
                "Lato"
              ]
            },
            "productSet": {
              "styles": {
                "products": {
                  "@media (min-width: 601px)": {
                    "margin-left": "-20px"
                  }
                }
              }
            }
          }
        });
      });
    }
    /* eslint-enable */
    return el;
  },
};
</script>

