---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: e3e03083e831f38143423e69c84a67bfbc0440db
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844242"
---
# Set-AzVMBootDiagnostic

## Áttekintés
A virtuális gép rendszerindítási diagnosztikai tulajdonságait módosítja.

## SZINTAXISA

### EnableBootDiagnostics
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DisableBootDiagnostics
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **set-AzVMBootDiagnostic** parancsmag a virtuális gép rendszerindítási diagnosztikai tulajdonságait módosítja.

## Példák

### 1. példa: a boot Diagnostics engedélyezése
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

Az első parancs a **Get-AzVM** segítségével a ContosoVM07 nevű virtuális gépet kapja.
A parancs a $VM változóban tárolja.

A második parancs engedélyezi a rendszerindítási diagnosztikát a virtuális gép számára a $VMban.
A diagnosztikai adatait a rendszer a megadott fiókban tárolja.

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

### -Letiltása
Jelzi, hogy ez a parancsmag letiltja a virtuális gép rendszerindítási diagnosztikát.

```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Engedélyezés
Jelzi, hogy ez a parancsmag engedélyezi a virtuális gép rendszerindítási diagnosztikát.

```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A virtuális gép erőforráscsoport-csoportjának nevét adja meg.

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Annak a tárolási fióknak a nevét adja meg, amelybe menteni szeretné a rendszerindítási diagnosztikai adatait.

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Azt a virtuális gépet adja meg, amelyhez ez a parancsmag a rendszerindítási diagnosztikát módosítja.
A virtuálisgép-objektum beolvasásához használja az Get-AzVM parancsmagot.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### PSVirtualMachine
A ' VM ' paraméter elfogadja a "PSVirtualMachine" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachine

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMBootDiagnosticsData](./Get-AzVMBootDiagnosticsData.md)


