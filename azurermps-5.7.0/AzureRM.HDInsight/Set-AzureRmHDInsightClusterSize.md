---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/set-azurermhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Set-AzureRmHDInsightClusterSize.md
ms.openlocfilehash: eda9032cde317f418132e28917f7543d60ea0bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93678989"
---
# <span data-ttu-id="af193-101">Set-AzureRmHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="af193-101">Set-AzureRmHDInsightClusterSize</span></span>

## <span data-ttu-id="af193-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af193-102">SYNOPSIS</span></span>
<span data-ttu-id="af193-103">A megadott szektorcsoportban lévő munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="af193-103">Sets the number of Worker nodes in a specified cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af193-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af193-104">SYNTAX</span></span>

```
Set-AzureRmHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af193-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af193-105">DESCRIPTION</span></span>
<span data-ttu-id="af193-106">A **set-AzureRmHDInsightClusterSize** parancsmag a megadott Azure HDInsight-fürtökben lévő munkaállomások számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="af193-106">The **Set-AzureRmHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="af193-107">Példák</span><span class="sxs-lookup"><span data-stu-id="af193-107">EXAMPLES</span></span>

### <span data-ttu-id="af193-108">1. példa: megadott szektorcsoport méretének beállítása</span><span class="sxs-lookup"><span data-stu-id="af193-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzureRmHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="af193-109">Ez a parancs beállítja a-Hadoop-001 nevű fürt méretét.</span><span class="sxs-lookup"><span data-stu-id="af193-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="af193-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af193-110">PARAMETERS</span></span>

### <span data-ttu-id="af193-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="af193-111">-ClusterName</span></span>
<span data-ttu-id="af193-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af193-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="af193-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af193-113">-DefaultProfile</span></span>
<span data-ttu-id="af193-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="af193-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af193-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af193-115">-ResourceGroupName</span></span>
<span data-ttu-id="af193-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="af193-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="af193-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="af193-117">-TargetInstanceCount</span></span>
<span data-ttu-id="af193-118">A fürtben a munkavégző csomópontok kívánt számát adja meg.</span><span class="sxs-lookup"><span data-stu-id="af193-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af193-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af193-119">CommonParameters</span></span>
<span data-ttu-id="af193-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af193-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af193-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af193-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af193-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af193-122">INPUTS</span></span>

### <span data-ttu-id="af193-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="af193-123">None</span></span>
<span data-ttu-id="af193-124">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="af193-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="af193-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af193-125">OUTPUTS</span></span>

### <span data-ttu-id="af193-126">Microsoft. Azure. Management. HDInsight. models. cluster</span><span class="sxs-lookup"><span data-stu-id="af193-126">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="af193-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af193-127">NOTES</span></span>

## <span data-ttu-id="af193-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af193-128">RELATED LINKS</span></span>

