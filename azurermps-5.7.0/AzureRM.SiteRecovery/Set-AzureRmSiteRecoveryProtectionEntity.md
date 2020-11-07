---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryprotectionentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 21bf19ba4a4d17ef41f6741deedd5cac486bbb32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672510"
---
# Set-AzureRmSiteRecoveryProtectionEntity

## Áttekintés
Beállítja a webhely-helyreállítási védelem entitás állapotát.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

### Letiltó (alapértelmezett)
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### EnterpriseToEnterprise
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### EnterpriseToAzure
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HyperVSiteToAzure
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
A **set-AzureRmSiteRecoveryProtectionEntity** parancsmag engedélyezi vagy letiltja a védelmet az Azure webhely-helyreállítási védelmi entitások számára.

## Példák

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -OS
Az operációs rendszer típusát adja meg.
A paraméter elfogadható értékei a következők:

- Windows
- Linux

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSDiskName
Az operációs rendszert tartalmazó lemez nevét adja meg.

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Házirend
A webhely-helyreállítási házirend objektumát adja meg.

```yaml
Type: ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Védelem
Megadja, hogy engedélyezve vagy le kell-e tiltani a védelmet.
A paraméter elfogadható értékei a következők:

- Engedélyezése
- Megbénít

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionEntity
A védelmi entitás objektumát adja meg.

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryAzureStorageAccountId
A cél Azure-tároló fiók AZONOSÍTÓját adja meg.

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForCompletion
Jelzi, hogy a parancs a visszatérés előtt várja a befejezést.

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
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

A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### ASRProtectionEntity
A ' ProtectionEntity ' paraméter az "ASRProtectionEntity" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### Microsoft. Azure. Command. SiteRecovery. ASRJob

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmSiteRecoveryProtectionEntity](./Get-AzureRmSiteRecoveryProtectionEntity.md)
