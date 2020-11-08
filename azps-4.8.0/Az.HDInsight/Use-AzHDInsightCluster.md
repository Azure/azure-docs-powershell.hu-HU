---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/use-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Use-AzHDInsightCluster.md
ms.openlocfilehash: 15d93d6dbdc7b231d47d5372864883f915e66ae9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025326"
---
# <span data-ttu-id="e16be-101">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e16be-101">Use-AzHDInsightCluster</span></span>

## <span data-ttu-id="e16be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e16be-102">SYNOPSIS</span></span>
<span data-ttu-id="e16be-103">Kijelöli az Invoke-RmAzureHDInsightHiveJob parancsmaggal használni kívánt fürtöt.</span><span class="sxs-lookup"><span data-stu-id="e16be-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

## <span data-ttu-id="e16be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e16be-104">SYNTAX</span></span>

```
Use-AzHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e16be-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e16be-105">DESCRIPTION</span></span>
<span data-ttu-id="e16be-106">A **use-AzHDInsightCluster** parancsmag azt az Azure HDInsight-fürtöt adja meg, amely a kaptár-feladatok elvégzéséhez használható Invoke-AzHDInsightHiveJob parancsmagot jelöli.</span><span class="sxs-lookup"><span data-stu-id="e16be-106">The **Use-AzHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="e16be-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e16be-107">EXAMPLES</span></span>

### <span data-ttu-id="e16be-108">1. példa: válasszon egy fürtöt a kaptár lekérdezések küldéséhez</span><span class="sxs-lookup"><span data-stu-id="e16be-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="e16be-109">Ez a parancs kiválaszt egy fürtöt a kaptár-lekérdezések küldéséhez.</span><span class="sxs-lookup"><span data-stu-id="e16be-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="e16be-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e16be-110">PARAMETERS</span></span>

### <span data-ttu-id="e16be-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="e16be-111">-ClusterName</span></span>
<span data-ttu-id="e16be-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e16be-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e16be-113">-DefaultProfile</span></span>
<span data-ttu-id="e16be-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e16be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e16be-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="e16be-115">-HttpCredential</span></span>
<span data-ttu-id="e16be-116">A cluster login (HTTP) hitelesítő adatait adja meg a fürthöz.</span><span class="sxs-lookup"><span data-stu-id="e16be-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e16be-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e16be-117">-ResourceGroupName</span></span>
<span data-ttu-id="e16be-118">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e16be-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e16be-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e16be-119">CommonParameters</span></span>
<span data-ttu-id="e16be-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e16be-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e16be-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e16be-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e16be-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e16be-122">INPUTS</span></span>

### <span data-ttu-id="e16be-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="e16be-123">None</span></span>

## <span data-ttu-id="e16be-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e16be-124">OUTPUTS</span></span>

### <span data-ttu-id="e16be-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e16be-125">System.String</span></span>

## <span data-ttu-id="e16be-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e16be-126">NOTES</span></span>

## <span data-ttu-id="e16be-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e16be-127">RELATED LINKS</span></span>

[<span data-ttu-id="e16be-128">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e16be-128">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="e16be-129">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="e16be-129">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)


