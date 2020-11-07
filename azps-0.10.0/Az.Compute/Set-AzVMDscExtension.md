---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: ccad3d793ec5763a4c7db44d2b5ff3583b35402b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844209"
---
# Set-AzVMDscExtension

## Áttekintés
A DSC bővítmény beállítása virtuális gépen.

## SZINTAXISA

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Leírás
A **set-AzVMDscExtension** parancsmag egy erőforráscsoport virtuális gépén a Windows PowerShell által kért állapot-konfigurációs (DSC) kiterjesztést adja meg.

## Példák

### 1. példa: DSC-bővítmény beállítása
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

Ez a parancs beállítja a VM07 nevű virtuális gép DSC bővítményét, hogy letöltse Sample.ps1.zip a STG nevű tároló fiókból és az alapértelmezett tárolóból.
A parancs a ConfigName nevű konfigurációt hívja meg.
A Sample.ps1.zip-fájlt korábban a **Közzététel-AzVMDscConfiguration-** ban töltötték fel.

### 2. példa: DSC-bővítmény beállítása konfigurációs adatokkal
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

Ez a parancs beállítja a VM13 nevű virtuális gép kiterjesztését Sample.ps1.zip letöltéséhez a STG nevű tárterület-fiókból és a WindowsPowerShellDSC nevű tárolóból.
A parancs a ConfigName nevű konfigurációt adja meg, és a konfigurációs adatokat és argumentumokat adja meg.
A Sample.ps1.zip-fájlt korábban a **Közzététel-AzVMDscConfiguration-** ban töltötték fel.

### 3. példa: DSC-bővítmény beállítása az automatikus frissítést tartalmazó konfigurációs adatokkal
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

Ez a parancs beállítja a VM22 nevű virtuális gép kiterjesztését Sample.ps1.zip letöltéséhez a STG nevű tárterület-fiókból és a WindowsPowerShellDSC nevű tárolóból.
A parancs a ConfigName nevű konfigurációt hívja meg, és a konfigurációs adatokat és argumentumokat adja meg.
Ez a parancs azt is lehetővé teszi, hogy a kiterjesztés-kezelő automatikusan frissítse a legújabb verzióra.
A Sample.ps1.zip korábban a **Közzététel-AzVMDscConfiguration-** ban töltötték fel.

## PARAMÉTEREK

### -ArchiveBlobName
A Publish-AzVMDscConfiguration parancsmag által korábban feltöltött konfigurációs fájl nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveContainerName
Annak az Azure-tárolónak a megnevezése, amelyben a konfigurációs Archívum található.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveResourceGroupName
Annak a csoportnak a neve, amely a konfigurációs archívumot tartalmazó tárolási fiókot tartalmazza.
Ez a paraméter nem kötelező, ha a tárolási fiók és a virtuális gép egyaránt ugyanabban az erőforráscsoport-csoportban található.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveStorageAccountName
Megadja a ArchiveBlobName letöltéséhez használt Azure Storage Account nevet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ArchiveStorageEndpointSuffix
A tárolási végpont utótagját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoUpdate
A *verzió* paraméter által megadott kiterjesztés-kezelő verziót adja meg.
Alapértelmezés szerint az Extension Handler nem frissíti az automatikus frissítést.
Használja az *AutoUpdate* paramétert, amellyel engedélyezheti a bővítmények automatikus frissítését a legújabb verzióra, és elérhetővé válik.

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

### -ConfigurationArgument
A konfigurációs függvény argumentumait tartalmazó kivonatoló táblát adja meg.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationData
Annak a. psd1 fájlnak az elérési útvonalát adja meg, amely a konfigurációhoz szükséges adatokat adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationName
Annak a konfigurációnak a nevét adja meg, amelyre a DSC bővítmény hivatkozik.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataCollection
Az adatgyűjtési típust adja meg.
A paraméter elfogadható értékei a következők: engedélyezés és letiltás.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Force
Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.

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

### -Hely
Az erőforrás-kiterjesztés elérési útját adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (név)
A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.
Az alapértelmezett érték a Microsoft. PowerShell. DSC.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A virtuális gép erőforráscsoport-csoportjának nevét adja meg.

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

### -Verzió
Annak a DSC-bővítménynek a verziószámát adja meg, amely a Set-AzVMDscExtension alkalmazza a beállításokat.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Annak a virtuális gépnek a neve, ahol a DSC Extension Handler telepítve van.

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

### -WmfVersion
A WMF-verziót adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.

A parancsmag nem fut.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### Nincs
Ez a parancsmag nem fogadja el a bevitelt.

## KIMENETEK

### Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Közzététel – AzVMDscConfiguration](./Publish-AzVMDscConfiguration.md)


