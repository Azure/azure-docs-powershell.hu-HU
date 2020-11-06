---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: bfda87b4a0810dc440da63949d17f52cf611fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502484"
---
# Remove-AzureRmADSpCredential

## Áttekintés
Hitelesítő adatok eltávolítása egy egyszerű szolgáltatótól.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ObjectIdWithKeyIdParameterSet (alapértelmezett)
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ObjectIdWithAllParameterSet
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNWithKeyIdParameterSet
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNWithAllParameterSet
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A Remove-AzureRmADSpCredential parancsmag használatával kompromisszum vagy a hitelesítő adatok kulcsának lejárati dátuma részeként eltávolíthatja a hitelesítő adatok kulcsát a megbízótól.
A rendszer az objektumazonosító vagy az egyszerű szolgáltatásnév (SPN) megadásával azonosítja a megbízót.

Az eltávolítani kívánt hitelesítő adatokat a program annak AZONOSÍTÓját azonosítja, ha az egyes hitelesítő adatok törlődnek, vagy egy "minden" kapcsolóval törli a szolgáltatóhoz társított összes hitelesítő adatokat.

## Példák

### Példa 1
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

Ez a parancs eltávolítja a hitelesítő kulcsot egy egyszerű szolgáltatótól.
Ebben a példában a "9044423a-60a3-45ac--9ab1 – 09534157ebb" azonosítójú kulcs törlődik a szolgáltatótól.

### 2. példa
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

Ez a parancs eltávolítja a hitelesítő kulcsot egy egyszerű szolgáltatótól.
Ebben a példában az összes hitelesítő adat törlődik a szolgáltatás fő nevéhez társított szolgáltatótól: " http://test123 ".

## PARAMÉTEREK

### -All (mind)
Váltson a szolgáltatóhoz társított összes hitelesítő adat eltávolításához.

```yaml
Type: SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Váltás a hitelesítő adatok törlésére megerősítés nélkül.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyId
Az eltávolítandó hitelesítőadat-kulcsot adja meg.
A megbízó kulcs-azonosítói a Get-AzureRmADSpCredential parancsmag használatával szerezhetők be.

```yaml
Type: Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Annak az objektumnak az azonosítója a szolgáltatónál, akinek a hitelesítő adatait el szeretné távolítani.

```yaml
Type: String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
A szolgáltatás megbízójának neve (SPN) a hitelesítő adatok eltávolításához.

```yaml
Type: String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmADSpCredential](./Get-AzureRmADSpCredential.md)

[Új – AzureRmADSpCredential](./New-AzureRmADSpCredential.md)

[Get-AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)

