---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: 737ccdbd742b3c4cc12518262423e846678cf599
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155579"
---
# Invoke-AzHDInsightHiveJob

## SYNOPSIS
Hive-lekérdezést küld egy HDInsight-fürtnek, és egy művelettel beolvassa a lekérdezés eredményét.

## SZINTAXIS

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
Az **Invoke-AzHDInsightHiveCm** parancsmag egy Hive-lekérdezést küld egy Azure HDInsight-fürtnek, és egy művelettel beolvassa a lekérdezés eredményét.
Mielőtt meghívja Use-AzHDInsightCluster **Invoke-AzHDInsightHiveFeladatot,** adja meg a lekérdezéshez használni kívánt fürtöt.

## PÉLDÁK

### 1. példa: Hive-lekérdezés elküldése Azure HDInsight-fürtbe
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

Ez a parancs elküldi a TÁBLA MEGJELENÍTÉSE lekérdezést a "Your-hadoop-001" nevű fürtnek.

## PARAMETERS

### -Argumentumok
Egy tömböt ad meg a feladat argumentumaiból.
Az argumentumokat a függvény parancssori argumentumként minden tevékenységnek átveszi.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultContainer
A HDInsight-fürt alapértelmezett Azure Storage-fiókjában található alapértelmezett tároló nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

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

### -DefaultStorageAccountKey
A HDInsight-fürt által használt alapértelmezett tárfiók fiókkulcsát adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultStorageAccountName
A HDInsight-fürt által használt alapértelmezett tárfiók neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Definiál
Megadja a hadoop konfigurációs értékeit, amelyek a feladat futtatásakor adhatók meg.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -File
A futtatni kívánt lekérdezést tartalmazó fájl elérési útját adja meg az Azure Storage-ban.
Ezt a paramétert használhatja a *Lekérdezés paraméter* helyett.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Files
A Hive-feladathoz szükséges fájlok gyűjteményét adja meg.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
A Hive-feladat nevét adja meg.
Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett értéket használja: "Hive: \<first 100 characters of Query\> ".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Query
A Hive lekérdezést adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunAsFileFile
Azt jelzi, hogy ez a parancsmag létrehoz egy fájlt az alapértelmezett Azure-tárfiókban, amelyben a lekérdezést tárolni lehet.
Ez a parancsmag parancsprogramként elküldi a fájlra hivatkozó feladatot.
Ez a funkció speciális karakterek, például százalékjel (%) kezeléséhez használható. hiba lépne fel a Templetonon keresztüli munkabeküldésekkor, mert a Templeton a százalékjelet beküldött lekérdezéseket URL-paraméterként értelmezi.

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

### -StatusFolder
Megadja annak a mappának a helyét, amely a feladat normál kimenetét és hibakimenetét tartalmazza.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### System.String

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Use-AzHDInsightCluster](./Use-AzHDInsightCluster.md)


