# Appendix A:  Product Patterns

To correctly interpret "_one countable instance of a whole of medicinal product_ ", it is important that this is seen in the context of the overall description of a medicinal product, which is always presented from the manufacturer as a "packaged medicinal product". Note that description of packaged medicinal products is outside the scope of the international release but may be included within a national extension. The IDMP Medicinal Product model describes this, showing how the Manufactured Item is related to the Packaged Medicinal Product via the Package Item (Container). This is a recursive class that represents both the package as supplied by the manufacturer (and, for example, labelled with the GTIN, the batch number and the expiry), and through a recursive relationship, with any sub-packages inside the outer pack.

**

<figure><img src="https://confluence.ihtsdotools.org/download/attachments/123904118/App%20A.png?version=1&modificationDate=1615996337000&api=v2" alt="" title=""><figcaption><p>**</p></figcaption></figure>

By describing the various standard patterns of products with their basic dose forms and intimate containers, consistent representation of strength based on unit of presentation can be maintained.

Note: in all the patterns described below, although pack size may be mentioned, this is to show how information is sourced from "what is". Description of pack size is out of scope for the international release, although it will be in scope for the national extension model, as some nations may require medicinal products that include description of pack size for their national terminology. Therefore, it is useful to have it shown here for informational purposes only.

  * [Discrete manufactured dose form; similar unit of presentation](304775947.html)
  * [Continuous presentation: Metered dose unit of presentation](304775950.html)
  * [Continuous presentation: Oral liquids designed for administration by "metered" medicine spoon](304775952.html)
  * [Continuous presentation: bounded by unit of presentation; solid dose forms](304775954.html)
  * [Continuous presentation: bounded by container; liquid dose forms](304775957.html)
  * [Continuous presentation: bounded by container; liquid/semi-solid dose forms; concentration strength required](304775960.html)
  * [Continuous presentation: unbounded by container](304775964.html)

