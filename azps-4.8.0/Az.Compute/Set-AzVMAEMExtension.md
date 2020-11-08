---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: b476254d5b9236aa95a30832499aca65a8a110c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183086"
---
# Set-AzVMAEMExtension

## Áttekintés
Engedélyezi a SAP-rendszerek figyelését.

## SZINTAXISA

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Leírás
A **set-AzVMAEMExtension** parancsmag frissíti a virtuális gép konfigurációját, hogy engedélyezze vagy frissítse a virtuális GÉPRE telepített SAP-rendszerek figyelésének támogatását.
A parancsmag telepíti az Azure Enhanced monitoring (AEM) bővítményt, amely összegyűjti a teljesítménnyel kapcsolatos adatokat, így az SAP rendszer számára elérhetővé válik.

## Példák

### 1. példa: az AEM-bővítmény használata
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

Ez a parancs a contoso-Server nevű virtuális gépet az AEM-bővítmény használatára állítja be.
A parancs a stdstorage nevű tárterület-fiókot adja meg.

## PARAMÉTEREK

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -EnableWAD
Ha ez a paraméter meg van határozva, akkor a parancsmagot engedélyezi a Windows Azure Diagnostics for this Virtual Machine használatát.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallNewExtension
Telepítse az új VM-bővítményt az SAP-hoz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Várva
Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet. Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.

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

### -OSType
Megadja az operációs rendszer lemezének típusát.
Ha az operációs rendszer lemeze nem tartalmaz típust, akkor ezt a paramétert kell megadnia.
A paraméter elfogadható értékei a következők: Windows és Linux.

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SetAccessToIndividualResources
A VM-identitás elérését az egyes erőforrásokhoz, például adatlemezekhez állítja be, a teljes erőforráscsoport helyett.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipStorage
Jelzi, hogy ez a parancsmag kihagyja a tárterület konfigurációját.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### System. String

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVMAEMExtension](./Get-AzVMAEMExtension.md)

[Remove-AzVMAEMExtension](./Remove-AzVMAEMExtension.md)

[Teszt-AzVMAEMExtension](./Test-AzVMAEMExtension.md)


