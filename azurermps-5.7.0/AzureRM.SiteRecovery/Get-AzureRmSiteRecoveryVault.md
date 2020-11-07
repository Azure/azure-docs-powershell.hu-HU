---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: f3988d28633ba879ebf78c57e235f4f07d6deced
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679682"
---
# Get-AzureRmSiteRecoveryVault

## Áttekintés
Webhely-helyreállítási boltozatokat kap a jelenlegi előfizetésből.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzureRmSiteRecoveryVault** parancsmag a jelenlegi előfizetésből kapja meg az Azure webhelyek helyreállítási boltozatai vagy egy bizonyos webhely-helyreállítási tároló listáját.

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

### -Name (név)
A boltozat nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az Azure erőforrás-csoportnak a nevét adja meg, amelyből a helyreállítási szolgáltatások objektumot be szeretné szerezni.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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

### System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. SiteRecovery. ASRVault]

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmSiteRecoveryVault](./New-AzureRmSiteRecoveryVault.md)

[Remove-AzureRmSiteRecoveryVault](./Remove-AzureRmSiteRecoveryVault.md)
