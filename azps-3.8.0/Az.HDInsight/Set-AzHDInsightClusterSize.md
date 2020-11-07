---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 8f34e9233da61bb2381c99c33922fa4332b588fd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846062"
---
# <span data-ttu-id="b00a6-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="b00a6-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="b00a6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b00a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b00a6-103">A megadott szektorcsoportban lévő munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b00a6-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="b00a6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b00a6-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b00a6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b00a6-105">DESCRIPTION</span></span>
<span data-ttu-id="b00a6-106">A **set-AzHDInsightClusterSize** parancsmag a megadott Azure HDInsight-fürtökben lévő munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b00a6-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b00a6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b00a6-107">EXAMPLES</span></span>

### <span data-ttu-id="b00a6-108">1. példa: megadott szektorcsoport méretének beállítása</span><span class="sxs-lookup"><span data-stu-id="b00a6-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="b00a6-109">Ez a parancs beállítja a-Hadoop-001 nevű fürt méretét.</span><span class="sxs-lookup"><span data-stu-id="b00a6-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b00a6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b00a6-110">PARAMETERS</span></span>

### <span data-ttu-id="b00a6-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="b00a6-111">-ClusterName</span></span>
<span data-ttu-id="b00a6-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b00a6-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b00a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00a6-113">-DefaultProfile</span></span>
<span data-ttu-id="b00a6-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b00a6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b00a6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b00a6-115">-ResourceGroupName</span></span>
<span data-ttu-id="b00a6-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b00a6-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b00a6-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="b00a6-117">-TargetInstanceCount</span></span>
<span data-ttu-id="b00a6-118">A fürtben a munkavégző csomópontok kívánt számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b00a6-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b00a6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00a6-119">CommonParameters</span></span>
<span data-ttu-id="b00a6-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b00a6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00a6-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b00a6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00a6-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b00a6-122">INPUTS</span></span>

### <span data-ttu-id="b00a6-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="b00a6-123">None</span></span>

## <span data-ttu-id="b00a6-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b00a6-124">OUTPUTS</span></span>

### <span data-ttu-id="b00a6-125">Microsoft. Azure. Management. HDInsight. models. cluster</span><span class="sxs-lookup"><span data-stu-id="b00a6-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="b00a6-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b00a6-126">NOTES</span></span>

## <span data-ttu-id="b00a6-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b00a6-127">RELATED LINKS</span></span>
