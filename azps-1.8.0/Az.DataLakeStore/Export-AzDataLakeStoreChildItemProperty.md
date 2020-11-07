---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: f7c347be55b2d0cde83013454e8396b9eb8f20f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836330"
---
# Export-AzDataLakeStoreChildItemProperty

## Áttekintés
A tulajdonságok (lemezhasználat és ACL) exportálása a teljes fához a megadott elérési úttal egy kimeneti elérési útra

## SZINTAXISA

### GetDiskUsage
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### GetAllProperties
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### GetAclDump
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Leírás
Az **AzDataLakeStoreChildItemProperty** az adott könyvtár ADLS és/vagy ACL-használati módjának jelentésére szolgál, valamint az alkönyvtárakra és a fájlokra.

## Példák

### Példa 1: a lemezhasználat és az ACL használatának beszerzése az összes alkönyvtár és fájl esetében
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

A lemezhasználat és az ACL használatának beszerzése az összes alkönyvtárra és-fájlra a/a. csoportban A IncludeFile biztosítja, hogy a használat a fájlok számára is elérhető legyen

### 2. példa: az összes alkönyvtár és fájl ACL-használati felületének beszerzése a konzisztens ACL-fájlokkal
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

Az ACL-használat beszerzése az összes alkönyvtárhoz és fájlhoz a/a. csoportban A IncludeFile biztosítja, hogy a használat a fájlok számára is jelenteni legyen. Ebben az esetben a HideconsistentAcl az/a-as ACL-t jeleníti meg, nem pedig a gyerekeket, mivel az összes gyermeknek ugyanaz a hozzáférése, mint az/a. Ez a jelző kihagyja a részfa ACL kimeneti, ha az összes hozzáférés-vezérlési lista megegyezik a legfelső szintű beállítással.

## PARAMÉTEREK

### -Fiók
Az adattó áruházbeli fiókja a FileSystem művelet végrehajtásához

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Párhuzamosság
A párhuzamosan feldolgozott fájlok/könyvtárak számát jelzi.
Az alapértelmezett beállítás a rendszerspecifikáción alapuló legjobb munkamennyiségként fog kiszámításra.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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

### -GetAcl
Az ACL kikeresése a gyökér elérési útjától kezdve

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GetDiskUsage
A lemezhasználat kikeresése a gyökér elérési útjától kezdve

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HideConsistentAcl
Ne jelenjen meg a címtár-részfa, ha az ACL-elemek ugyanazok a teljes részfa alatt. Ez megkönnyíti csak azokat az elérési utakat látni, amelyek a hozzáférés-vezérlési listáktól függnek. Ha például a/a/b csoport minden fájlja és mappája megegyezik, ne jelenítse meg a subtreeunder/a/b, és a konzisztens ACL-columnCannot csak a "true" értéket tartalmazó kimeneti/a/b adja meg, ha a IncludeFiles nincs beállítva, mert a konzisztens ACL nem határozható meg a fájlok hozzáférési listáinak beolvasása nélkül.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFile
Statisztika megjelenítése a fájl szinten (alapértelmezés szerint csak a címtár szintű adatok jelenjenek meg)

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

### -MaximumDepth
Maximális színmélység a gyökérkönyvtárból, amíg a lemezhasználat vagy a hozzáférés-vezérlés megjelenik

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputPath
A kimeneti fájl elérési útja. Lehet helyi elérési út vagy ADL elérési útja. Alapértelmezés szerint helyi. Ha a SaveToAdl jelszavát határozza meg, akkor ez egy ADL-útvonal ugyanazon fiókban

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
A törlési művelet eredményét jelző logikai választ adja eredményül.

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

### -Path (elérési út)
A megadott adattó-fiók útvonala, amelyet le kell olvasnia.
A "/Folder/file.txt" formátumban lehet fájl vagy mappa, ahol az első "/" a DNS a fájlrendszer gyökerét jelzi.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SaveToAdl
Ha a továbbítás után menti a memóriaképfájl-fájlt az ADL-ra.
A DumpFile wil egy ADL-útvonal, abban az esetben

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

### – Megerősítés
A parancsmag futtatása előtt kéri a megerősítést.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Annak megjelenítése, hogy mi történik, ha a parancsmag fut.
A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### System. String

### Microsoft. Azure. Command. DataLakeStore. models. DataLakeStorePathInstance

### System. Management. Automation. SwitchParameter

### System. Int32

## KIMENETEK

### System. Boolean

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
