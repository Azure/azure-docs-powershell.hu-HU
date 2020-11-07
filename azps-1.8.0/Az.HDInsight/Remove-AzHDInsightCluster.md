---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: e52d838f0aa7ce901b8099710b38f570d4285a4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835990"
---
# <span data-ttu-id="32850-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="32850-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="32850-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="32850-102">SYNOPSIS</span></span>
<span data-ttu-id="32850-103">Eltávolítja a megadott HDInsight-fürtöt az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="32850-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="32850-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="32850-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32850-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="32850-105">DESCRIPTION</span></span>
<span data-ttu-id="32850-106">A **Remove-AzHDInsightCluster** parancsmag az előfizetésből eltávolítja a megadott HDInsight-fürtszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="32850-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="32850-107">Ezzel a művelettel a Hadoop elosztott fájlrendszerében (HDFS) tárolt adatok is törlődnek.</span><span class="sxs-lookup"><span data-stu-id="32850-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="32850-108">A rendszer nem törli a kapcsolódó Azure-tárterületi fiókban tárolt adatait.</span><span class="sxs-lookup"><span data-stu-id="32850-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="32850-109">A külső metastores tárolt adatot nem törli a program.</span><span class="sxs-lookup"><span data-stu-id="32850-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="32850-110">Példák</span><span class="sxs-lookup"><span data-stu-id="32850-110">EXAMPLES</span></span>

### <span data-ttu-id="32850-111">Példa 1: Azure HDInsight-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="32850-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="32850-112">Ez a parancs eltávolítja a-Hadoop-001 nevű fürtöt.</span><span class="sxs-lookup"><span data-stu-id="32850-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="32850-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="32850-113">PARAMETERS</span></span>

### <span data-ttu-id="32850-114">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="32850-114">-ClusterName</span></span>
<span data-ttu-id="32850-115">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32850-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="32850-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32850-116">-DefaultProfile</span></span>
<span data-ttu-id="32850-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="32850-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32850-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32850-118">-ResourceGroupName</span></span>
<span data-ttu-id="32850-119">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32850-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="32850-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32850-120">CommonParameters</span></span>
<span data-ttu-id="32850-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="32850-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32850-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32850-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32850-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="32850-123">INPUTS</span></span>

### <span data-ttu-id="32850-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="32850-124">None</span></span>

## <span data-ttu-id="32850-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32850-125">OUTPUTS</span></span>

### <span data-ttu-id="32850-126">Microsoft. Azure. Management. HDInsight. models. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="32850-126">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="32850-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="32850-127">NOTES</span></span>

## <span data-ttu-id="32850-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32850-128">RELATED LINKS</span></span>

[<span data-ttu-id="32850-129">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="32850-129">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="32850-130">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="32850-130">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


