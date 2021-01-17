---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupStatus.md
ms.openlocfilehash: 9e1ba332efbaf3c7e314f4daf7ebfb9bb96b22b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346146"
---
# Get-AzRecoveryServicesBackupStatus

## SYNOPSIS
Annak ellenőrzése, hogy az ARM-erőforrásról van-e biztonságimentve.

## SZINTAXIS

### Név (alapértelmezett)
```
Get-AzRecoveryServicesBackupStatus -Name <String> -ResourceGroupName <String> -Type <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdWorkload
```
Get-AzRecoveryServicesBackupStatus -Type <String> -ResourceId <String> -ProtectableObjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Azonosító
```
Get-AzRecoveryServicesBackupStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## LEÍRÁS
A parancs null/üres értéket ad vissza, ha a megadott erőforrás nem védett az előfizetés egyik helyreállítási szolgáltatás-tárolója alatt sem. Ha a tároló védett, a megfelelő tárolóadatokat fogja visszaadni.

## PÉLDÁK

### 1. példa

Annak ellenőrzése, hogy az ARM-erőforrásról van-e biztonságimentve. (automatikusan generált)

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupStatus -Name 'myAzureVM' -ResourceGroupName 'myAzureVMRG' -Type AzureVM
```

## PARAMETERS

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Annak az Azure-erőforrásnak a neve, amelynek a képviselőjét ellenőrizni kell, ha azt már védi az előfizetésben egy helyreállítási szolgáltatás tárolója.

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectableObjectName
Annak az Azure-erőforrásnak a neve, amelynek a képviselőjét ellenőrizni kell, ha azt már védi az előfizetésben egy helyreállítási szolgáltatás tárolója.

```yaml
Type: System.String
Parameter Sets: IdWorkload
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Annak az Azure-erőforrásnak az erőforráscsoportja, amelynek az elemét ellenőrizni kell, ha az előfizetésben már rendelkezik egy RecoveryServices-tárolóval.

```yaml
Type: System.String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Annak az Azure-erőforrásnak az azonosítója, amelynek a reprezentatív elemét ellenőrizni kell, ha azt már védi az előfizetésben néhány RecoveryServices-tároló.

```yaml
Type: System.String
Parameter Sets: IdWorkload, Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Type
Annak az Azure-erőforrásnak a típusa, amelynek a képviselő elemét ellenőrizni kell, ha azt már védi az előfizetésben egy helyreállítási szolgáltatás tárolója.

```yaml
Type: System.String
Parameter Sets: Name, IdWorkload
Aliases:
Accepted values: AzureVM, AzureFiles

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ResourceBackupStatus

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
