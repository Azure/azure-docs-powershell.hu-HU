---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 94dac11a3c26adaac93b4e36c2dda3df513d4076
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465889"
---
# Publish-AzVMDscConfiguration

## SYNOPSIS
Egy DSC-parancsfájlt tölt fel azure blobtárolóba.

## SZINTAXIS

### UploadArchive (alapértelmezett)
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateArchive
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **Publish-AzVMDscConfiguration** parancsmag feltölti a kívánt államkonfigurációs (DSC) parancsfájlt az Azure blobtárba, amelyet később a Set-AzVMDscExtension parancsmagot használva lehet azure-Set-AzVMDscExtension alkalmazni.

## PÉLDÁK

### 1. példa: .zip csomag létrehozása egy azure-tárhelyre való feltöltéshez
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

Ez a parancs létrehoz egy .zip csomagot az adott parancsfájlhoz és a függő erőforrásmodulhoz, és feltölti azt az Azure-tárhelyre.

### 2. példa: .zip-csomag létrehozása és tárolása helyi fájlban
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

Ez a parancs .zip csomagot hoz létre az adott parancsprogramhoz és a függő erőforrásmodulhoz, és azt a helyi fájlban tárolja, .\MyConfiguration.ps1.zip.

### 3. példa: Konfiguráció hozzáadása az archívumhoz, majd feltöltése tárhelyre
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

Ez a parancs hozzáadja a Sample.ps1 nevű konfigurációt a konfigurációs archívumhoz az Azure-tárhelyre való feltöltéshez, és kihagyja a függő erőforrásmodulokat.

### 4. példa: Konfigurációs adatok hozzáadása az archívumhoz, majd feltöltése tárhelyre
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

Ez a parancs hozzáadja a Sample.ps1 1-es nevű konfigurációs adatokat és SampleData.psda konfigurációs archívumhoz, és feltölti az Azure-tárhelyre.

### 5. példa: Konfiguráció, konfigurációs adatok és további tartalmak hozzáadása az archívumhoz, majd feltöltése tárhelyre
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

Ez a parancs hozzáadja a Sample.ps1 nevű konfigurációt, az 1-es SampleData.psdkonfigurációs adatokat és további tartalmakat a konfigurációs archívumhoz az Azure-tárhelyre való feltöltéshez.

## PARAMETERS

### -AdditionalPath
A konfigurációs archívumba foglalni kívánt fájl vagy címtár elérési útját adja meg.
A rendszer letölti a virtuális gépre a konfigurációval együtt.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Egy .psd1 fájl elérési útját adja meg, amely a konfiguráció adatait adja meg.
Ez bekerül a konfigurációs archívumba, majd átkerül a konfigurációs függvénynek.
A parancsmagon keresztül biztosított konfigurációs adatút felülírja azt Set-AzVMDscExtension parancsmagon keresztül

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

### -ConfigurationPath
Egy vagy több konfigurációt tartalmazó fájl elérési útját adja meg.
A fájl lehet Windows PowerShell-parancsfájl (.ps1) vagy Windows PowerShell-modulfájl (.psm1).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContainerName
Annak az Azure-tárolónak a neve, amelybe a konfiguráció feltöltődik.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
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

### -OutputArchivePath
Annak a helyi .zip fájlnak az elérési útját adja meg, amelybe a konfigurációs archívumot meg kell írni.
Ha ezt a paramétert használja, a konfigurációs parancsfájl nem lesz feltöltve az Azure blobtárba.

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A tárfiókot tartalmazó erőforráscsoport nevét adja meg.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipDependencyDetection
Azt jelzi, hogy ez a parancsmag kizárja a DSC-erőforrásfüggőségeket a konfigurációs archívumból.

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

### -StorageAccountName
A konfigurációs parancsfájlnak a ContainerName paraméterben megadott tárolóba való feltöltéshez használt *Azure-tárfiók* nevét adja meg.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
A tárolási végpont utótagját határozza meg.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
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

### System.String[]

## KIMENETEK

### System.String

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


