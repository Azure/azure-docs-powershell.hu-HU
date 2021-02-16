---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: 667a8214fc7df27ce46dc28ddbdeabd1b00dce5b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162219"
---
# Set-AzVMAccessExtension

## SYNOPSIS
Hozzáadja a VMAccess bővítményt egy virtuális géphez.

## SZINTAXIS

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzVMAccessExtension** parancsmag hozzáadja a Virtuálisgép-elérés (VMAccess) virtuális gép VMAccess bővítményét egy virtuális géphez. A VMAccess bővítmény ideiglenes jelszó beállítására használható, és ezt a gépbe való bejelentkezés után azonnal módosítania kell. Ez windowsos tartományvezérlők esetén nem támogatott.

## PÉLDÁK

### 1. példa: VMAccess-bővítmény hozzáadása
```powershell
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.4" -UserName "PFuller" -Password "Password"
```

Ez a parancs hozzáad egy VMAccess bővítményt a VirtualMachine07 nevű virtuális géphez az ResourceGroup11-ben.
A parancs megadja a VMAccess név és típuskezelő verzióját.

### 2. példa

Hozzáadja a VMAccess bővítményt egy virtuális géphez. (automatikusan generált)

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMAccessExtension -Credential <PSCredential> -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -TypeHandlerVersion '2.4' -VMName 'VirtualMachine07'
```

## PARAMETERS

### -Hitelesítő adatok
A virtuális gép felhasználónevét és jelszavát adja meg **PSCredential objektumként.**
Ha a vmen a helyi rendszergazdai fióktól eltérő nevet ad meg, a VMAccess bővítmény hozzáad egy ilyen nevű helyi rendszergazdai fiókot, és hozzárendeli a megadott jelszót a fiókhoz. Ha a virtuális gép helyi rendszergazdai fiókja létezik, alaphelyzetbe állítja a jelszót, és ha a fiók le van tiltva, a VMAccess bővítmény engedélyezi azt.
Hitelesítő adatok beszerzéséhez használja a Get-Credential parancsmagot.
További információért írja be a `Get-Help Get-Credential` .

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -ForceRerun
Azt jelzi, hogy ez a parancsmag a bővítmény eltávolítása és újratelepítése nélkül újrafuttatja ugyanazt a bővítménykonfigurációt a virtuális gépen.
Az érték bármilyen karakterlánc lehet, amely nem az aktuális érték.
Ha a forceUpdateTag nem változik, a nyilvános vagy védett beállítások frissítéseit továbbra is alkalmazza a kezelő.

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

### -Location
A virtuális gép helyét határozza meg.

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

### -Name
Megadja annak a kiterjesztésnek a nevét, amelybe a parancsmag hozzáadja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NoWait
Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér. Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.

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
A virtuális gép erőforráscsoportját adja meg.

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
A virtuális géphez használni használt bővítmény verziója.
A verzió beszerzéséhez futtassa a Get-AzVMExtensionImage parancsmagot a *PublisherName* paraméterhez a Microsoft.Compute értékkel, a Type paraméterhez pedig a VMAccessAgent *parancsmagot.* A typeHandlerVersionnek legalább 2.0-nak kell lennie, mivel az 1-es verzió elavult.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Egy virtuális gép nevét adja meg.
Ez a parancsmag hozzáadja a VMAccess-et a paraméter által megadott virtuális géphez.

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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.Management.Automation.PSCredential

### System.String

### System.Management.Automation.SwitchParameter

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVMAccessExtension](./Get-AzVMAccessExtension.md)

[Remove-AzVMAccessExtension](./Remove-AzVMAccessExtension.md)

[Set-AzVMExtension](./Set-AzVMExtension.md)

[Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md)


