---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://go.microsoft.com/fwlink/?LinkId=690162
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 2a30a190fbf257142e1c1e4fb4329fd6c4f41e3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502696"
---
# Remove-AzureRmKeyVault

## Áttekintés
Egy kulcs boltozatának törlése

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### ByAvailableVault
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDeletedVault
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **Remove-AzureRmKeyVault** parancsmag törli a megadott kulcs boltozatát.
Az adott példányban található összes kulcsot és titkot is törli.

Fontos tudni, hogy az erőforráscsoport megadása esetén a parancsmag nem kötelező.

## Példák

### 1. példa: kulcs-boltozat eltávolítása
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

Ez a parancs eltávolítja a Contoso03Vault nevű kulcs-boltozatot a jelenlegi előfizetésből.

### 2. példa: kulcs-boltozat eltávolítása egy megadott erőforráscsoporthoz
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

Ez a parancs eltávolítja a Contoso03Vault nevű kulcspárt a megnevezett erőforrás csoportból.
Ha nem adja meg az erőforráscsoport nevét, a parancsmag a megnevezett kulcs boltozatát keresi a jelenlegi előfizetésben.

## PARAMÉTEREK

### -Force
Azt jelzi, hogy a parancsmag nem kér megerősítést.
Ez a parancsmag alapértelmezés szerint arra kéri, hogy erősítse meg, hogy törölni szeretné-e a kulcs boltozatát.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
Törölje véglegesen a korábban törölt boltozatot.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hely
A törölt boltozat helye.

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Egy erőforráscsoport nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Az eltávolítandó kulcsfájl nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut. Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmKeyVault](./Get-AzureRmKeyVault.md)

[Új – AzureRmKeyVault](./New-AzureRmKeyVault.md)
