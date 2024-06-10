
**Embed image from File ULR or Internal File**:
```sql
TABLE WITHOUT ID file.link as "Characters", EmbededPortraitImg as ""
FROM #characters AND !#index
FLATTEN choice( typeof(portrait)="link", 
	embed(link(meta( choice( typeof(portrait)="link", portrait, this.file.link ) ).path, "150")), 
	"![anyName|150](" + portrait + ")"
) AS EmbededPortraitImg
```