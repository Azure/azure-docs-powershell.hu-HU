---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 1aad073ebd1f1a5e14abfd728ba6e6266a2d6fb8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364179"
---
# Disable-AzVMDiskEncryption

## SYNOPSIS
Letiltja a titkosítást az IaaS virtuális gépeken.

## SZINTAXIS

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Disable-AzVMDiskEncryption** parancsmag letiltja a titkosítást az infrastruktúra szolgáltatásként (IaaS) virtuális gépén.
Ez a parancsmag csak Windows-virtuális gépeken támogatott, Linux virtuális gépeken nem.
Ez a parancsmag egy bővítményt telepít a virtuális gépre a titkosítás letiltásához.
Ha a *Name paraméter* nincs megadva, létrejön egy "AzureDiskEncryption for Windows VMs" nevű bővítmény.
Figyelem: Ez a parancsmag újraindítja a virtuális gépet.

## PÉLDÁK

### 1. példa: A windowsos virtuális gép összes kötetének titkosításának letiltása
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

Ez a parancs letiltja a titkosítást az összes típusú, VM002 nevű virtuális gépre, amely a Group0001 nevű erőforráscsoporthoz tartozik.
Mivel a *VolumeType* paraméter nincs megadva, a parancsmag az Összes értékre állítja az értéket.

### 2. példa: Adatkötetek titkosításának letiltása Windows virtuális gépen
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

Ez a parancs letiltja a titkosítást a VM004 nevű virtuális gép típusadatokat mennyisége számára, amely a Group002 nevű erőforráscsoporthoz tartozik.

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

### -DisableAutoUpgradeMinorVersion
Azt jelzi, hogy ez a parancsmag letiltja a bővítmény alverziója automatikus frissítését.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExtensionPublisherName
A bővítmény közzétevőjának neve. Ezt a paramétert csak a "Microsoft.Azure.Security" alapértelmezett értékének felülbírálása érdekében adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExtensionType
A bővítmény típusa. Ezt a paramétert megadva felülbírálhatja a Windows-VMs -hez használt "AzureDiskEncryption" és a Linux-alapú "AzureDiskEncryptionForLinux" alapértelmezett értékét.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.

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

### -Name
A bővítményt képviselő Azure Resource Manager (ARM) nevét adja meg.
Ha nincs megadva ez a paraméter, ez a parancsmag alapértelmezés szerint "AzureDiskEncryption windowsos VMs esetén" lesz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A virtuális gép erőforráscsoportnevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
A titkosítási bővítmény verzióját határozza meg.
Ha nem ad meg értéket ehhez a paraméterhez, a bővítmény legújabb verzióját használja a program.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Annak a virtuális gépnek a nevét adja meg, amelyn ez a parancsmag letiltja a titkosítást.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VolumeType
A titkosítási művelet végrehajtásához szükséges virtuális gépkötet típusát határozza meg.
Windows-virtuális gépek esetén érvényes értékek: 
- Mind
- Operációs rendszer
- Adatok.
Ha nem ad meg értéket ehhez a paraméterhez, az alapértelmezett érték a Mind érték.
Linux esetén jelenleg nem támogatott a titkosítás letiltása.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

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
A parancsmag futtatásakor a program megjeleníti, hogy mi történik.
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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Management.Automation.SwitchParameter

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVMDiskEncryptionStatus](./Get-AzVMDiskEncryptionStatus.md)

[Remove-AzVMDiskEncryptionExtension](./Remove-AzVMDiskEncryptionExtension.md)

[Set-AzVMDiskEncryptionExtension](./Set-AzVMDiskEncryptionExtension.md)


