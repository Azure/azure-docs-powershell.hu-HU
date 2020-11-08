---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: BB01591D-4E1A-4C89-8B2A-5A242C29B125
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8904c5e228d181a3090b3a0d62d74d84005bd2b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016248"
---
# Invoke-AzureHDInsightHiveJob

## Áttekintés
A kaptár-lekérdezéseket egy HDInsight-fürtbe küldi, a lekérdezés végrehajtásának előrehaladását jeleníti meg, és a lekérdezés eredményét egy műveletben kapja.

## SZINTAXISA

```
Invoke-AzureHDInsightHiveJob [-Arguments <String[]>] [-Defines <Hashtable>] [-File <String>]
 [-Files <String[]>] [-JobName <String>] [-Query <String>] [-RunAsFileJob] [-StatusFolder <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Leírás
Az Azure PowerShell HDInsight ez a verziója elavult.
A következő parancsmagok törlődnek január 1, 2017.
Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.

Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

A **meghívó-AzureHDInsightHiveJob** parancsmag HDInsight-fürtökhöz küldi a kaptár-lekérdezéseket, a lekérdezés végrehajtásának előrehaladását jeleníti meg, és a lekérdezés eredményét egy műveletben kapja.
Ahhoz, hogy a HDInsight-fürtöt be szeretné állítani, a **AzureHDInsightHiveJob** futtatása előtt futtatnia kell az Use-AzureHDInsightCluster parancsmagot.

## Példák

### 1. példa: a kaptár-lekérdezés elterjesztése
```
PS C:\>Use-AzureHDInsightCluster "Cluster01" -Subscription (Get-AzureSubscription -Current).SubscriptionId 
PS C:\> Invoke-AzureHDInsightHiveJob "select * from hivesampletable limit 10"
```

Az első parancs a **use-AzureHDInsightCluster** parancsmaggal megadhatja a kaptár-lekérdezéshez használni kívánt fürtöt a jelenlegi előfizetésben.

A második parancs a **meghívott AzureHDInsightHiveJob** parancsmagot használja a kaptár lekérdezés elküldéséhez.

## PARAMÉTEREK

### -Argumentumok
Argumentumokat ad meg egy Hadoop-feladathoz.
Az argumentumokat parancssori argumentumként kell átadni az egyes tevékenységekhez.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Határozza meg
Itt adhatja meg a Hadoop konfigurációs értékeit a feladatok futásakor.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Params

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Fájl
A Windows Azure Storage blob (WASB) elérési útját adja meg a futtatandó lekérdezést tartalmazó Azure Blob-tárolóban lévő fájlhoz.
Ezt a paramétert a *query* paraméter helyett használhatja.

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Files
A kaptár-feladathoz szükséges fájlok gyűjteményét adja meg.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Feladatnév
A kaptár-feladat nevét adja meg.
Ha nem adja meg ezt a paramétert, ez a parancsmag az alapértelmezett értéket használja: "kaptár: \<first 100 characters of Query\> ".

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.
Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Query
A kaptár-lekérdezést adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueryText

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunAsFileJob
Jelzi, hogy ez a parancsmag létrehoz egy fájlt az alapértelmezett Azure Storage-fiókban, amelyben a lekérdezés tárolható.
Ez a parancsmag elküldi azt a feladatot, amely parancsfájlként hivatkozik erre a fájlra.

Ezt a funkciót speciális karakterek (például százalék (%)) kezelésére használhatja. Ez a Templeton-on keresztül sikertelen volt, mert a Templeton URL-ként értelmezi a százalékos jellel ellátni kívánt lekérdezést.

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

### -StatusFolder
Annak a mappának a helyét adja meg, amely az adott projekthez tartozó normál kimeneteket és hibák kimenetét tartalmazza, valamint a kilépési kódot és a tevékenység naplóit.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

## KIMENETEK

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureHDInsightHiveJobDefinition](./New-AzureHDInsightHiveJobDefinition.md)

[Use-AzureHDInsightCluster](./Use-AzureHDInsightCluster.md)


