---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Add-AzureRmHDInsightScriptAction.md
ms.openlocfilehash: 51bfee17e33afcb93b90c36198e9352c3fca5fc9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672222"
---
# Add-AzureRmHDInsightScriptAction

## Áttekintés
Parancsfájl-műveleteket ad egy fürtkonfiguráció-objektumhoz.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SZINTAXISA

```
Add-AzureRmHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
Az **Add-AzureRmHDInsightScriptAction** parancsmag parancsfájl-műveleteket ad az New-AzureRmHDInsightClusterConfig parancsmag által létrehozott HDInsight-konfigurációs objektumhoz.

A parancsfájl-műveletek funkciókat nyújtanak a további szoftverek telepítéséhez, illetve a Hadoop-fürtökön futó alkalmazások konfigurációjának módosításához Windows PowerShell-vagy bash-parancsfájlok (Windows-vagy Linux-fürtök esetén) segítségével.

Parancsfájl-műveletek akkor futnak a fürtcsomópontok során, ha a HDInsight-fürtöket telepítik, és a fürt a fürtök teljes HDInsight-konfigurációját követően futnak.
A parancsfájl-műveletek a rendszeradminisztrátori fiók jogosultságai csoportban futnak, és teljes hozzáférési jogosultságokat biztosítanak a fürtcsomópontok számára.
Az egyes fürtöket megadhatja az adott sorrendben futtatandó parancsfájl-műveletek listájával.

## Példák

### 1. példa: parancsfájl-művelet hozzáadása a fürtkonfigurációs objektumhoz
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig  `
            | Add-AzureRmHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzureRmHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
            | New-AzureRmHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

A parancs hozzáadja az Ön-Hadoop-001-fürthöz tartozó, a fürtök létrehozásakor futtatandó parancsfájl-műveleteket.

## PARAMÉTEREK

### -Config
Azt a HDInsight-objektumot adja meg, amelyet a parancsmag módosított.
Ezt az objektumot a **New-AzureRmHDInsightClusterConfig** parancsmag hozza létre.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name (név)
A parancsfájl-műveletek nevét adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeType
Annak a csomópontnak a típusa, amelyen a parancsfájl-műveletek futtathatók.
A paraméter elfogadható értékei a következők:

- HeadNode
- WorkerNode
- ZookeeperNode

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Paraméterek
A parancsfájl-műveletek paramétereit adja meg.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -URI
A parancsfájl-műveletek (PowerShell-vagy bash-parancsfájlok) nyilvános URI-jét adja meg.

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## BEMENETEK

### AzureHDInsightConfig
A "config" paraméter elfogadja a "AzureHDInsightConfig" típusú értéket a csővezetékről

## KIMENETEK

### Microsoft. Azure. Command. HDInsight. models. AzureHDInsightConfig

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Új – AzureRmHDInsightClusterConfig](./New-AzureRmHDInsightClusterConfig.md)


