---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: 1c89db6267fffeb73820150d1c73c3225f45cde2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493582"
---
# Enable-AzureRmBackupContainerReregistration

## Áttekintés
Visszaregisztrálja a kiszolgálót, hogy egy biztonságimásolat-tárolóhoz csatlakozzon.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Az **enable-AzureRmBackupContainerReregistration** parancsmag újra regisztrálja a kiszolgálót az Azure Backup-tárolóhoz való csatlakozáshoz, és folytatja a biztonsági másolat helyreállítási pontjának a folytatását.

Ha elpusztít egy szervert, az összes Felhőbeli biztonságimásolat-pontja a biztonsági másolatban marad.
Ha helyettesítő kiszolgálót hoz létre, és ugyanazt a teljesen minősített tartománynevet rendeli hozzá, a kiszolgálót visszakapcsolhatja ugyanahhoz a boltozathoz.
Ez a parancsmag lehetővé teszi biztonsági másolatok készítését és új biztonsági pontok hozzáadását a meglévő halmazhoz.
Az új kiszolgáló továbbra is a biztonsági mentési láncban marad.

## Példák

## PARAMÉTEREK

### -Container
Azt a tárolót adja meg, amelyre a parancsmag újra regisztrálja.
Ha **AzureRmBackupContainer** szeretne beolvasni, használja az Get-AzureRmBackupContainer parancsmagot.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### AzureBackupContainer

## KIMENETEK

### Nincs

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Register-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)


