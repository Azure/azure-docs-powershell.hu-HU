---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 9e19d8e205010ce55886761d2cbb7fd904d5277d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672076"
---
# Restore-AzureRmApiManagement

## Áttekintés
Egy API-kezelési szolgáltatás visszaállítása a megadott Azure Storage blob-ról

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **Restore-AzureRmApiManagement** PARANCSMAG egy API-kezelési szolgáltatást ad vissza a megadott biztonsági másolatból egy Azurestorage blobban.

## Példák

### Példa 1: API-kezelési szolgáltatás visszaállítása
```
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

A parancs visszaállítja az API-kezelési szolgáltatást az Azure Storage blob szolgáltatásból.

## PARAMÉTEREK

### -Name (név)
A biztonsági másolattal visszaállított API-kezelési példány nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.
Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.

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

### -ResourceGroupName
Annak az erőforráscsoport-csoportnak a nevét adja meg, amely alatt az API-kezelés létezik.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceBlobName
Itt adhatja meg az Azure-tárterület biztonságimásolat-forrás blobjának a nevét.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceContainerName
Az Azure Storage Backup Source tároló nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
A tárterület-kapcsolat kontextusát adja meg.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

## KIMENETEK

### Microsoft. Azure. Command. ApiManagement. models. PsApiManagement

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Backup-AzureRmApiManagement](./Backup-AzureRmApiManagement.md)

[Get-AzureRmApiManagement](./Get-AzureRmApiManagement.md)

[Új – AzureRmApiManagement](./New-AzureRmApiManagement.md)

[Remove-AzureRmApiManagement](./Remove-AzureRmApiManagement.md)


