---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: e65367a94e946aee83df2087463bd0081e925862
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672707"
---
# Update-AzureRmContainerRegistryCredential

## Áttekintés
Újragenerálja a tároló beállításjegyzékének bejelentkezési hitelesítő adatait.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### NameResourceGroupParameterSet (alapértelmezett)
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RegistryObjectParameterSet
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
Az **Update-AzureRmContainerRegistryCredential** parancsmag a tároló beállításjegyzékének bejelentkezési hitelesítő adatait hozza létre.

## Példák

### 1. példa: bejelentkezési hitelesítő adatok újragenerálása a tároló beállításjegyzékében
```
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

Ez a parancs újragenerálja a megadott tároló beállításjegyzékének bejelentkezési hitelesítő adatait. A hitelesítő adatok újragenerálásához engedélyezni kell a rendszergazdai hozzáférést a tároló beállításjegyzékéhez `MyRegistry` .

## PARAMÉTEREK

### -Name (név)
A tároló beállításjegyzékének neve.

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PasswordName
Az újragenerálni kívánt jelszó neve.
Engedélyezett értékek: jelszó, password2.

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Registry
Tároló rendszerleíróadatbázis-objektum.

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Erőforráscsoporthoz tartozó név.

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSContainerRegistry
A "Registry" paraméter elfogadja a "PSContainerRegistry" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. Azure. Command. ContainerRegistry. PSContainerRegistryCredential

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmContainerRegistry](./New-AzureRmContainerRegistry.md)

[Update-AzureRmContainerRegistry](./Update-AzureRmContainerRegistry.md)

[Get-AzureRmContainerRegistryCredential](./Get-AzureRmContainerRegistryCredential.md)

