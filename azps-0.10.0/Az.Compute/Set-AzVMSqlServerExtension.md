---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 1795216cbc18da2d503a1e0056d614337cd12785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398240"
---
# Set-AzVMSqlServerExtension

## SYNOPSIS
Beállítja az Azure SQL Server-bővítményt egy virtuális gépen.

## SZINTAXIS

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzVMSqlServerExtension** parancsmag beállítja az AzureSQL Server-bővítményt egy virtuális gépen.

## PÉLDÁK

### 1. példa: Automatikus javítási beállítások megadása virtuális gépen
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

Az első parancs a **New-AzureVMSqlServerAutoPatchingConfig** parancsmag használatával hoz létre konfigurációs objektumot.
A parancs a konfigurációt a $AutoPatchingConfig tárolja.

A második parancs a VirtualMachine11 nevű virtuális gépet kapja meg a Service02 nevű szolgáltatásban a Get-AzVM parancsmag használatával.
A parancs a folyamat műveleti operátorával átadja az objektumot az aktuális parancsmagnak.

Az aktuális parancsmag beállítja az automatikus javítási beállításokat $AutoPatchingConfig virtuális gépre.
A parancs átadja a virtuális gépet a Update-AzVM parancsmagnak.

### 2. példa: Automatikus biztonsági mentési beállítások megadása virtuális gépen
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

Az első parancs a **New-AzureVMSqlServerAutoBackupConfig** parancsmag használatával hoz létre konfigurációs objektumot.
A parancs a konfigurációt a $AutoBackupConfig tárolja.

A második parancs lekérte a VirtualMachine11 nevű virtuális gépet a Service02 nevű szolgáltatásban, majd átadja az aktuális parancsmagnak.

Az aktuális parancsmag beállítja az automatikus biztonsági mentési beállításokat $AutoBackupConfig virtuális gépre.
A parancs átadja a virtuális gépet a Update-AzVM parancsmagnak.

### 3. példa: SQL Server-bővítmény letiltása virtuális gépen
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

Ez a parancs egy VirtualMachine08 nevű virtuális gépet kap a Service03 szolgáltatásban, majd átadja az aktuális parancsmagnak.
A parancs letiltja az SQL Server virtuális gép bővítményét a virtuális gépen.

### 4. példa: SQL Server-bővítmény eltávolítása egy adott virtuális gépen
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

Ez a parancs egy VirtualMachine08 nevű virtuális gépet kap a Service03 szolgáltatásban, majd átadja az aktuális parancsmagnak.
A parancs eltávolítja az SQL Server virtuális gép bővítményét a virtuális gépen.

## PARAMETERS

### -AutoBackupSettings
Az SQL Server automatikus biztonsági mentési beállításait adja meg.
Az **AutoBackupSettings objektum** létrehozásához használja a New-AzureVMSqlServerAutoBackupConfig parancsmagot.

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
Az SQL Server automatikus javítási beállításait adja meg.
**AutoPatchingSettings objektum** létrehozásához használja a New-AzureVMSqlServerAutoPatchingConfig parancsmagot.

```yaml
Type: AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -KeyVaultCredentialSettings
```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
A virtuális gép helyét határozza meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Az SQL Server bővítmény nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A virtuális gép erőforráscsoportját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Az SQL Server-bővítmény verzióját határozza meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Annak a virtuális gépnek a nevét adja meg, amelyen ez a parancsmag beállítja az SQL Server-bővítményt.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nincs
Ez a parancsmag semmilyen bemenetet nem fogad el.

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[New-AzureVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[New-AzureVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Remove-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AzVM](./Update-AzVM.md)


