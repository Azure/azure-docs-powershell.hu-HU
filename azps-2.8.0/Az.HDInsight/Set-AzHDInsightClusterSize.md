---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 1616714879a260dea3611809b5f7028b4a203d34
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666328"
---
# <span data-ttu-id="0ec74-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="0ec74-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="0ec74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ec74-102">SYNOPSIS</span></span>
<span data-ttu-id="0ec74-103">A megadott szektorcsoportban lévő munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ec74-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="0ec74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ec74-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ec74-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ec74-105">DESCRIPTION</span></span>
<span data-ttu-id="0ec74-106">A **set-AzHDInsightClusterSize** parancsmag a megadott Azure HDInsight-fürtökben lévő munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ec74-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="0ec74-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0ec74-107">EXAMPLES</span></span>

### <span data-ttu-id="0ec74-108">1. példa: megadott szektorcsoport méretének beállítása</span><span class="sxs-lookup"><span data-stu-id="0ec74-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="0ec74-109">Ez a parancs beállítja a-Hadoop-001 nevű fürt méretét.</span><span class="sxs-lookup"><span data-stu-id="0ec74-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0ec74-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ec74-110">PARAMETERS</span></span>

### <span data-ttu-id="0ec74-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="0ec74-111">-ClusterName</span></span>
<span data-ttu-id="0ec74-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ec74-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0ec74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ec74-113">-DefaultProfile</span></span>
<span data-ttu-id="0ec74-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0ec74-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ec74-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ec74-115">-ResourceGroupName</span></span>
<span data-ttu-id="0ec74-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ec74-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0ec74-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="0ec74-117">-TargetInstanceCount</span></span>
<span data-ttu-id="0ec74-118">A fürtben a munkavégző csomópontok kívánt számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="0ec74-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="0ec74-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ec74-119">CommonParameters</span></span>
<span data-ttu-id="0ec74-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ec74-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ec74-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ec74-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ec74-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ec74-122">INPUTS</span></span>

### <span data-ttu-id="0ec74-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="0ec74-123">None</span></span>

## <span data-ttu-id="0ec74-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ec74-124">OUTPUTS</span></span>

### <span data-ttu-id="0ec74-125">Microsoft. Azure. Management. HDInsight. models. cluster</span><span class="sxs-lookup"><span data-stu-id="0ec74-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="0ec74-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ec74-126">NOTES</span></span>

## <span data-ttu-id="0ec74-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ec74-127">RELATED LINKS</span></span>
