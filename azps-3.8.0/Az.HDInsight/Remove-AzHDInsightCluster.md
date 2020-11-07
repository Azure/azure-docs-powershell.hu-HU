---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: c4a3f33094e5337306e44e2b310cd7cce32e8887
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847526"
---
# <span data-ttu-id="9a50b-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9a50b-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="9a50b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a50b-102">SYNOPSIS</span></span>
<span data-ttu-id="9a50b-103">Eltávolítja a megadott HDInsight-fürtöt az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="9a50b-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="9a50b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a50b-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a50b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a50b-105">DESCRIPTION</span></span>
<span data-ttu-id="9a50b-106">A **Remove-AzHDInsightCluster** parancsmag az előfizetésből eltávolítja a megadott HDInsight-fürtszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="9a50b-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="9a50b-107">Ezzel a művelettel a Hadoop elosztott fájlrendszerében (HDFS) tárolt adatok is törlődnek.</span><span class="sxs-lookup"><span data-stu-id="9a50b-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="9a50b-108">A rendszer nem törli a kapcsolódó Azure-tárterületi fiókban tárolt adatait.</span><span class="sxs-lookup"><span data-stu-id="9a50b-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="9a50b-109">A külső metastores tárolt adatot nem törli a program.</span><span class="sxs-lookup"><span data-stu-id="9a50b-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="9a50b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9a50b-110">EXAMPLES</span></span>

### <span data-ttu-id="9a50b-111">Példa 1: Azure HDInsight-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="9a50b-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="9a50b-112">Ez a parancs eltávolítja a-Hadoop-001 nevű fürtöt.</span><span class="sxs-lookup"><span data-stu-id="9a50b-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="9a50b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a50b-113">PARAMETERS</span></span>

### <span data-ttu-id="9a50b-114">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="9a50b-114">-ClusterName</span></span>
<span data-ttu-id="9a50b-115">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a50b-115">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a50b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a50b-116">-DefaultProfile</span></span>
<span data-ttu-id="9a50b-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9a50b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a50b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a50b-118">-ResourceGroupName</span></span>
<span data-ttu-id="9a50b-119">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9a50b-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9a50b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a50b-120">-PassThru</span></span>
<span data-ttu-id="9a50b-121">Ha a PassThru létezik, az eredmény kitermelése</span><span class="sxs-lookup"><span data-stu-id="9a50b-121">If PassThru is present, output the result</span></span>

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

### <span data-ttu-id="9a50b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a50b-122">CommonParameters</span></span>
<span data-ttu-id="9a50b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a50b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a50b-124">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9a50b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a50b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a50b-125">INPUTS</span></span>

### <span data-ttu-id="9a50b-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="9a50b-126">None</span></span>
## <span data-ttu-id="9a50b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a50b-127">OUTPUTS</span></span>

### <span data-ttu-id="9a50b-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a50b-128">System.Boolean</span></span>
## <span data-ttu-id="9a50b-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a50b-129">NOTES</span></span>

## <span data-ttu-id="9a50b-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a50b-130">RELATED LINKS</span></span>

[<span data-ttu-id="9a50b-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9a50b-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="9a50b-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9a50b-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)

