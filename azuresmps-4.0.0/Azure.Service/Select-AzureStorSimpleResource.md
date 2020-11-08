---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015448"
---
# Select-AzureStorSimpleResource

## Áttekintés
Erőforrást állít be aktuális erőforrásként.

## SZINTAXISA

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
A **Select-AzureStorSimpleResource** parancsmag aktuális erőforrásként állítja be az erőforrást.
Miután kiválasztott egy erőforrást, az egyéb parancsmagok az adott erőforrás környezetén belül érvényesek.

## Példák

### 1. példa: erőforrás kijelölése első alkalommal
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

A parancs kijelöli az Contoso64-Tsqa nevű erőforrást az aktuális környezetben.
Ebben a példában a számítógépen nem volt ilyen környezet inicializálva korábban, ezért a *RegistrationKey* paraméter értékét is meg kell adnia.

### 2. példa: erőforrás kiválasztásának kísérlete
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### 3. példa: egy korábban kijelölt erőforrás kijelölése
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

A parancs kijelöli az Contoso64-Tsqa nevű erőforrást az aktuális környezetben.
Ebben a példában ez a környezet korábban ki volt jelölve, ezért nem kell megadni a *RegistrationKey* paraméter értékét.

## PARAMÉTEREK

### -Profil
Egy Azure-profilt ad meg.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistrationKey
A regisztrációs kulcsot adja meg.
Adjon meg egy billentyűt az első alkalommal, amikor kijelöl egy erőforrást.
Miután a parancsmag kijelöli az aktuális erőforrást, a parancsmagok szükség szerint ezt a billentyűt használják.
További információt a [szolgáltatás regisztrációs kulcsának beszerzése](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  ( https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) a Microsoft fejlesztői hálózatán) című témakörben talál.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Annak az erőforrásnak a nevét adja meg, amelyet az aktuális erőforrásként szeretne kijelölni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs

## KIMENETEK

### StorSimpleResourceContext
Ez a parancsmag egy **StorSimpleResourceContext** objektumot ad eredményül, amely tartalmazza az erőforrás környezetének részleteit.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[Get-AzureStorSimpleResourceContext](./Get-AzureStorSimpleResourceContext.md)


