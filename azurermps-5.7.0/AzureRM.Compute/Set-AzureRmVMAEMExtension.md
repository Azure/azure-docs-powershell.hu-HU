---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: edc91b756b90684299d84228c04862a0ce6c2e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492357"
---
# Set-AzureRmVMAEMExtension

## Áttekintés
Engedélyezi a SAP-rendszerek figyelését.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [<CommonParameters>]
```

## Leírás
A **set-AzureRmVMAEMExtension** parancsmag frissíti a virtuális gép konfigurációját, hogy engedélyezze vagy frissítse a virtuális GÉPRE telepített SAP-rendszerek figyelésének támogatását.
A parancsmag telepíti az Azure Enhanced monitoring (AEM) bővítményt, amely összegyűjti a teljesítménnyel kapcsolatos adatokat, így az SAP rendszer számára elérhetővé válik.

## Példák

### 1. példa: az AEM-bővítmény használata
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

Ez a parancs a contoso-Server nevű virtuális gépet az AEM-bővítmény használatára állítja be.
A parancs a stdstorage nevű tárterület-fiókot adja meg.

## PARAMÉTEREK

### -DisableWAD
Jelzi, hogy ez a parancsmag nem engedélyezi az Azure Diagnostics használatát a virtuális gépen.

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

### -EnableWAD
Ha ez a paraméter meg van határozva, akkor a parancsmagot engedélyezi a Windows Azure Diagnostics for this Virtual Machine használatát.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
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
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Annak a virtuális gépnek az erőforráscsoport-csoportjának a nevét adja meg, amelyre a parancsmag módosított.

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

### -SkipStorage
Jelzi, hogy ez a parancsmag kihagyja a tárterület konfigurációját.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
A virtuális gép nevét adja meg.
Ez a parancsmag hozzáadja a virtuális gép AEM bővítményét, amelyet ez a paraméter határoz meg.

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

### -WADStorageAccountName
Annak a tároló fióknak a nevét adja meg, amelyet a parancsmag a LinuxDiagnostics vagy a IaaSDiagnostics bővítmény konfigurálásához használ.
Ha a virtuális gép nem szabványos tárolási fiókot használ, meg kell adnia a paraméter értékét.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzureRmVMAEMExtension](./Get-AzureRmVMAEMExtension.md)

[Remove-AzureRmVMAEMExtension](./Remove-AzureRmVMAEMExtension.md)

[Teszt-AzureRmVMAEMExtension](./Test-AzureRmVMAEMExtension.md)


