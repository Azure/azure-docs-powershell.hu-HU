---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 5efda3a73cc94d2e196b5817d5b3c1e507192da0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844637"
---
# Get-AzVMAEMExtension

## Áttekintés
Információt kap az agrár-és az agrár-mellékről.

## SZINTAXISA

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A **Get-AzVMAEMExtension** parancsmag információkat kap az Azure Enhanced monitoring (AEM) bővítményről.

## Példák

### 1. példa: az AEM-bővítmény beszerzése
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

Ez a parancs a contoso-Server nevű virtuális gép AEM-bővítményének információit kapja meg.

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
A virtuális gép nevét adja meg.
Ez a parancsmag információt ad az agrár-és a virtuális gép AEM-bővítményére vonatkozóan.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OSType
Megadja az operációs rendszer lemezének típusát.
Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.
A paraméter elfogadható értékei a következők: Windows és Linux.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
A virtuális gép erőforráscsoport nevét adja meg.
Ez a parancsmag a virtuális gép AEM-bővítményére vonatkozó információkat kap.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Állapot
Jelzi, hogy ez a parancsmag csak az AEM bővítmény példány nézetét kapja meg.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
A virtuális gép nevét adja meg.
Ez a parancsmag információt ad az agrár-és a virtuális gép AEM-bővítményéről, amelyet ez a paraméter határoz meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineExtension

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Remove-AzVMAEMExtension](./Remove-AzVMAEMExtension.md)

[Set-AzVMAEMExtension](./Set-AzVMAEMExtension.md)

[Teszt-AzVMAEMExtension](./Test-AzVMAEMExtension.md)


