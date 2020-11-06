---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: 76cf830e79c2374d81c57a1341ae99636333e273
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498960"
---
# <span data-ttu-id="136de-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="136de-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="136de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="136de-102">SYNOPSIS</span></span>
<span data-ttu-id="136de-103">A jelenlegi előfizetéshez vagy egy meghatározott erőforráscsoporthoz tartozó összes Azure HDInsight-szektorcsoport beszerzése és listázása, vagy egy adott fürt beolvasása.</span><span class="sxs-lookup"><span data-stu-id="136de-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="136de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="136de-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="136de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="136de-105">DESCRIPTION</span></span>
<span data-ttu-id="136de-106">A **Get-AzureRmHDInsightCluster** parancsmag az Azure HDInsight-szolgáltatási fürtök listáját tartalmazza az aktuális előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="136de-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="136de-107">Az *fürtnév* paraméterrel részletes információkat kaphat egy adott fürtről.</span><span class="sxs-lookup"><span data-stu-id="136de-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="136de-108">Példák</span><span class="sxs-lookup"><span data-stu-id="136de-108">EXAMPLES</span></span>

### <span data-ttu-id="136de-109">Példa 1: az Azure HDInsight-fürtök listázása</span><span class="sxs-lookup"><span data-stu-id="136de-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="136de-110">Ez a parancs felsorolja az összes Azure HDInsight-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="136de-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="136de-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="136de-111">PARAMETERS</span></span>

### <span data-ttu-id="136de-112">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="136de-112">-ClusterName</span></span>
<span data-ttu-id="136de-113">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="136de-113">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="136de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="136de-114">-DefaultProfile</span></span>
<span data-ttu-id="136de-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="136de-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="136de-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="136de-116">-ResourceGroupName</span></span>
<span data-ttu-id="136de-117">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="136de-117">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="136de-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="136de-118">CommonParameters</span></span>
<span data-ttu-id="136de-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="136de-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="136de-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="136de-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="136de-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="136de-121">INPUTS</span></span>

### <span data-ttu-id="136de-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="136de-122">None</span></span>
<span data-ttu-id="136de-123">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="136de-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="136de-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="136de-124">OUTPUTS</span></span>

### <span data-ttu-id="136de-125">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. HDInsight. models. AzureHDInsightCluster]</span><span class="sxs-lookup"><span data-stu-id="136de-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster]</span></span>

## <span data-ttu-id="136de-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="136de-126">NOTES</span></span>

## <span data-ttu-id="136de-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="136de-127">RELATED LINKS</span></span>

[<span data-ttu-id="136de-128">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="136de-128">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="136de-129">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="136de-129">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


