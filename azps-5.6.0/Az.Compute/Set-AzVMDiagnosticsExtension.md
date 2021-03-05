---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 9e33f3e956f7d1fee0d93eebf5e14fa0df460303
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013686"
---
# Set-AzVMDiagnosticsExtension

## SYNOPSIS
Konfigurálja az Azure diagnosztikai bővítményt egy virtuális gépen.

## SZINTAXIS

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzVMDiagnosticsExtension** parancsmag konfigurálja az Azure diagnosztikai bővítményt egy virtuális gépen.

## PÉLDÁK

### 1. példa: Diagnosztikai konfigurációban megadott tárfiók használatával való diagnosztika engedélyezése
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

Ez a parancs diagnosztikai konfigurációs fájlt használ a diagnosztika engedélyezéséhez.
A diagnostics_publicconfig.xml a diagnosztikai bővítmény nyilvános XML-konfigurációját tartalmazza, beleértve annak a tárfióknak a nevét, amelyre a diagnosztikai adatokat küldeni fogja.
A diagnosztikai tárfióknak ugyanabban az előfizetésben kell lennie, mint a virtuális gépnek.

### 2. példa: Diagnosztikai adatok engedélyezése tárfiók nevével
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

Ez a parancs a tárfiók nevét használja a diagnosztika engedélyezéséhez.
Ha a diagnosztikai konfiguráció nem ad meg tárfióknevet, vagy felül szeretné bírálni a konfigurációs fájlban megadott diagnosztikai tárfiók nevét, használja a *StorageAccountName* paramétert.
A diagnosztikai tárfióknak ugyanabban az előfizetésben kell lennie, mint a virtuális gépnek.

### 3. példa: A diagnosztika engedélyezése a tárfiók nevével és kulcsával
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

Ez a parancs a tárfiók nevét és kulcsát használja a diagnosztika engedélyezéséhez.
Ha a diagnosztikai tárfiók másik előfizetésben van, mint a virtuális gép, engedélyezze a diagnosztikai adatok küldését a tárfiókba a név és a kulcs explicit megadásával.

## PARAMETERS

### -AutoUpgradeMinorVersion
Azt jelzi, hogy ez a parancsmag lehetővé teszi-e az Azure vendégügynöknek, hogy automatikusan frissítse a bővítményt egy újabb alverzióra.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
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

### -DiagnosticsConfigurationPath
A konfigurációs fájl elérési útját adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
A virtuális gép helyét határozza meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Egy bővítmény nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
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

### -StorageAccountEndpoint
A tárfiók végpontját határozza meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountKey
A tárfiók kulcsát adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
A tárfiók nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
Az Azure-tárterület környezetét határozza meg.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
A bővítménynek a virtuális géphez használt verzióját adja meg.
A verzió beszerzéséhez futtassa a Get-AzVMExtensionImage parancsmagot a *PublisherName* paraméterhez a Microsoft.Compute értékkel, a Típus paraméterhez pedig a VMAccessAgent *parancsmagot.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Annak a virtuális gépnek a nevét adja meg, amelyen a parancsmag működik.

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

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext

### System.Boolean

## KIMENETEK

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVMDiagnosticsExtension](./Get-AzVMDiagnosticsExtension.md)

[Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md)

[Remove-AzVMDiagnosticsExtension](./Remove-AzVMDiagnosticsExtension.md)


