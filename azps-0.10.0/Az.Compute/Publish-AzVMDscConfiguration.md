---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: d099feea5efe52d8bcc6a0067550a7c4ae9bbc3a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844429"
---
# Publish-AzVMDscConfiguration

## Áttekintés
DSC-parancsfájl feltöltése Azure Blob-tárhelyre

## SZINTAXISA

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

## Leírás
A **Közzététel-AzVMDscConfiguration** parancsmag az Azure Blob-tárhelyre feltölthet egy kívánt állami konfigurációs (DSC) parancsfájlt, amelyet később a Set-AzVMDscExtension parancsmagot használó Azure virtuális gépekre alkalmazhat.

## Példák

### Példa 1:. zip csomag létrehozása a feltöltés az Azure Storage szolgáltatásba
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

Ez a parancs létrehoz egy. zip csomagot a megadott parancsfájlhoz és bármely függő erőforrás-modulhoz, és feltölti azt az Azure Storage szolgáltatásba.

### 2. példa: zip-csomag létrehozása és tárolása egy helyi fájlon
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

Ez a parancs létrehoz egy. zip csomagot a megadott parancsfájlhoz és bármely függő erőforrás-modulhoz, és a .\MyConfiguration.ps1.zip nevű helyi fájlban tárolja azt.

### 3. példa: konfiguráció felvétele az archívumba, majd feltöltés a tárterületre
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

Ez a parancs felveszi a konfigurációs archívumba Sample.ps1 nevű konfigurációt az Azure tárhelyre való feltöltéshez, és kihagyja a függő erőforrás-modulokat.

### Példa 4: konfigurációs és konfigurációs adatokat vehet fel az archívumba, majd feltöltheti azt a tárterületre
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

Ez a parancs az Azure-tárterületre való feltöltéshez felveszi a SampleData.psd1 nevű Sample.ps1 és konfigurációs adatokat a konfigurációs archívumba.

### Példa 5: konfiguráció, konfigurációs adatok és további tartalmak hozzáadása az archívumhoz, majd feltöltés a tárterületre
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

Ez a parancs felveszi a Sample.ps1, a Configuration Data SampleData.psd1 nevű konfigurációt, és további tartalmakat ad a konfigurációs archívumhoz az Azure-tárterületre való feltöltéshez.

## PARAMÉTEREK

### -AdditionalPath
A konfigurációs archívumba felvenni kívánt fájl vagy könyvtár elérési útvonalát adja meg.
A rendszer a konfigurációval együtt letölti a virtuális gépre.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Annak a. psd1 fájlnak az elérési útvonalát adja meg, amely a konfigurációhoz szükséges adatokat adja meg.
Ez hozzáadódik a konfigurációs archívumhoz, majd átment a konfigurációs függvényhez.
A Set-AzVMDscExtension parancsmagon keresztül megadott konfigurációs adatelérési út felülírja.

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

### -ConfigurationPath
Egy vagy több konfigurációt tartalmazó fájl elérési útvonalát adja meg.
A fájl lehet Windows PowerShell-parancsfájl (. ps1) vagy Windows PowerShell-modul (. psm1).

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContainerName
Annak az Azure-tárolónak a nevét adja meg, amelyre a rendszer a konfigurációt feltöltötte.

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: 4
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

### -OutputArchivePath
Annak a helyi. zip fájlnak az elérési útját adja meg, amelybe a konfigurációs archívumot írni kívánja.
Ha ezt a paramétert használja, a konfigurációs parancsfájl nem töltődik fel az Azure Blob-tárolóba.

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
A tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipDependencyDetection
Azt jelzi, hogy ez a parancsmag kizárja a DSC erőforrás-függőségeket a konfigurációs archívumból.

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

### -StorageAccountName
Annak az Azure-tárterületnek a nevét adja meg, amely a konfigurációs parancsfájlnak a *ContainerName* paraméterben megadott tárolóra való feltöltéséhez használatos.

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
A tárterület végpontjának utótagját adja meg.

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

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

### Karakterlánc
A ' ConfigurationPath ' paraméter a "string" típusú értéket fogadja el a csővezetékről

## KIMENETEK

### System. String

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


