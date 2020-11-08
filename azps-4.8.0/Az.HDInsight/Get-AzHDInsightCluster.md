---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: 289f7b4bf397384b1420af02a5517e57bf51675d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018094"
---
# <span data-ttu-id="fe8b1-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fe8b1-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="fe8b1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe8b1-102">SYNOPSIS</span></span>
<span data-ttu-id="fe8b1-103">A jelenlegi előfizetéshez vagy egy meghatározott erőforráscsoporthoz tartozó összes Azure HDInsight-szektorcsoport beszerzése és listázása, vagy egy adott fürt beolvasása.</span><span class="sxs-lookup"><span data-stu-id="fe8b1-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="fe8b1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe8b1-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe8b1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe8b1-105">DESCRIPTION</span></span>
<span data-ttu-id="fe8b1-106">A **Get-AzHDInsightCluster** parancsmag az Azure HDInsight-szolgáltatási fürtök listáját tartalmazza az aktuális előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="fe8b1-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="fe8b1-107">Az *fürtnév* paraméterrel részletes információkat kaphat egy adott fürtről.</span><span class="sxs-lookup"><span data-stu-id="fe8b1-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="fe8b1-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fe8b1-108">EXAMPLES</span></span>

### <span data-ttu-id="fe8b1-109">Példa 1: az Azure HDInsight-fürtök listázása</span><span class="sxs-lookup"><span data-stu-id="fe8b1-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="fe8b1-110">Ez a parancs felsorolja az összes Azure HDInsight-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="fe8b1-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="fe8b1-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe8b1-111">PARAMETERS</span></span>

### <span data-ttu-id="fe8b1-112">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="fe8b1-112">-ClusterName</span></span>
<span data-ttu-id="fe8b1-113">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe8b1-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe8b1-114">-DefaultProfile</span></span>
<span data-ttu-id="fe8b1-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fe8b1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe8b1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe8b1-116">-ResourceGroupName</span></span>
<span data-ttu-id="fe8b1-117">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe8b1-117">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe8b1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe8b1-118">CommonParameters</span></span>
<span data-ttu-id="fe8b1-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe8b1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe8b1-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fe8b1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe8b1-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe8b1-121">INPUTS</span></span>

### <span data-ttu-id="fe8b1-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="fe8b1-122">None</span></span>

## <span data-ttu-id="fe8b1-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe8b1-123">OUTPUTS</span></span>

### <span data-ttu-id="fe8b1-124">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fe8b1-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="fe8b1-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe8b1-125">NOTES</span></span>

## <span data-ttu-id="fe8b1-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe8b1-126">RELATED LINKS</span></span>

[<span data-ttu-id="fe8b1-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fe8b1-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="fe8b1-128">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="fe8b1-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


