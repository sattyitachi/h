 if (productInfo && productInfo.description !== 'Verizon Cloud Unlimited') {
        list.push({
          icon: {
            name: productInfo.icon,
            ariaHidden: 'true',
          },
          title: {
            children: productInfo.description,
          },
          subtitle: {
            children:
              productInfo?.marketingDesc?.subTitle
                
          },
        });
      }
      else if (productInfo && productInfo.description !== 'Verizon Cloud Unlimited') {
        list.push({
          icon: {
            name: productInfo.icon,
            ariaHidden: 'true',
          },
          title: {
            children: productInfo.description,
          },
          subtitle: {
            children:
              productInfo?.groupDescription === productInfo?.marketingDesc
                ? renderHTML(productInfo?.marketingDesc)
                : renderHTML(`${productInfo.marketingDesc}<br><br>${productInfo.groupDescription}`),
          },
        });
      }
