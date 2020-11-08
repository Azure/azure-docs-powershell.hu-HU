---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015720"
---
# Add-AzureHDInsightScriptAction

## Áttekintés
Egy HDInsight parancsfájl-művelet hozzáadása

## SZINTAXISA

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Leírás
Az Azure PowerShell HDInsight ez a verziója elavult.
A következő parancsmagok törlődnek január 1, 2017.
Kérjük, használja az Azure PowerShell HDInsight újabb verzióját.

Ha többet szeretne tudni arról, hogy miként hozhat létre fürtöket az új HDInsight, olvassa el a [Linux-alapú fürtök létrehozása az Azure PowerShell-HDInsight használatával](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) című témakört https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Ha többet szeretne tudni arról, hogy miként küldhet munkahelyeket az Azure PowerShell és más megközelítések segítségével, olvassa el a [Hadoop-feladatok elküldése az HDInsight-](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) on https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/)
Az Azure PowerShell HDInsight további információt az [Azure HDInsight parancsmagok](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (című témakörben találhat https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

A **Add-AzureHDInsightScriptAction** parancsmag Azure HDInsight funkciókat biztosít, amelyek a további szoftverek telepítéséhez vagy a Hadoop-fürtökön futó alkalmazások konfigurációjának módosításához használhatók a Windows PowerShell-parancsfájlok használatával.

Parancsfájl-műveletek akkor futnak a fürtcsomópontok során, ha a HDInsight-fürtöket telepítik, és a fürt a fürtök teljes HDInsight-konfigurációját követően futnak.
A parancsfájl-műveletek a rendszeradminisztrátori fiók jogosultságai csoportban futnak, és teljes hozzáférési jogosultságokat biztosítanak a fürtcsomópontok számára.
Az egyes fürtöket megadhatja az adott sorrendben futtatandó parancsfájl-műveletek listájával.

## Példák

### 1. példa: parancsfájl-művelet hozzáadása fürthöz
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

Az első parancs a **New-AzureHDInsightClusterConfig** parancsmagot használja az HDInsight-beli fürtkonfiguráció létrehozásához, majd a $config változóban tárolja.

A második parancs az **Add-AzureHDInsightScriptAction** parancsmagot használja a TestScriptAction nevű parancsfájl-műveletek hozzáadásához a $config.

A végleges parancs a **New-AzureHDInsightCluster** parancsmagot használja az $config-ban tárolt parancsfájlokat futtató új HDInsight-fürtök létrehozásához.

### 2. példa: több parancsfájl-művelet hozzáadása a fürthöz
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

Az első parancs a **New-AzureHDInsightClusterConfig** parancsmagot használja az HDInsight-beli fürtkonfiguráció létrehozásához, majd a $config változóban tárolja.

A második parancs az **Add-AzureHDInsightScriptAction** parancsmaggal adja hozzá a megadott parancsfájl-műveletet az $Confighez, és a pipeline operátor segítségével másodszor is felveszi a $Configt, ha második parancsfájl **-** műveletet szeretne hozzáadni a $Confighoz.

A végleges parancs a **New-AzureHDInsightCluster** parancsmagot használja az $config parancsfájl-műveleteket futtató fürtök létrehozásához.

## PARAMÉTEREK

### -ClusterRoleCollection
Azokat a csomópontokat adja meg, amelyekhez parancsfájlt kell futtatni.
A paraméter elfogadható értékei a következők: HeadNode vagy DataNode.

Adhat meg egy értéket vagy mindkét értéket.

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Config
Konfigurációs objektumot ad meg.
Ez a parancsmag parancsfájl-műveleti információkat ad az objektumhoz, amelyhez ez a paraméter van meghatározva.

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A parancsfájl-műveletek nevét adja meg.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Paraméterek
A parancsfájl-műveletek által megkövetelt paramétereket adja meg.

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

### -URI
A futtatandó parancsfájl URI-helyét adja meg.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
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

[Új – AzureHDInsightCluster](./New-AzureHDInsightCluster.md)

[Új – AzureHDInsightClusterConfig](./New-AzureHDInsightClusterConfig.md)


