---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: f232d1df7bef3800fc54b2469a51f3f69c8d4fa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496148"
---
# <span data-ttu-id="a3387-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a3387-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="a3387-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3387-102">SYNOPSIS</span></span>
<span data-ttu-id="a3387-103">A jelenlegi előfizetéshez vagy egy meghatározott erőforráscsoporthoz tartozó összes Azure HDInsight-szektorcsoport beszerzése és listázása, vagy egy adott fürt beolvasása.</span><span class="sxs-lookup"><span data-stu-id="a3387-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3387-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3387-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3387-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3387-105">DESCRIPTION</span></span>
<span data-ttu-id="a3387-106">A **Get-AzureRmHDInsightCluster** parancsmag az Azure HDInsight-szolgáltatási fürtök listáját tartalmazza az aktuális előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="a3387-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="a3387-107">Az *fürtnév* paraméterrel részletes információkat kaphat egy adott fürtről.</span><span class="sxs-lookup"><span data-stu-id="a3387-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="a3387-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a3387-108">EXAMPLES</span></span>

### <span data-ttu-id="a3387-109">Példa 1: az Azure HDInsight-fürtök listázása</span><span class="sxs-lookup"><span data-stu-id="a3387-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="a3387-110">Ez a parancs felsorolja az összes Azure HDInsight-fürtöt.</span><span class="sxs-lookup"><span data-stu-id="a3387-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="a3387-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3387-111">PARAMETERS</span></span>

### <span data-ttu-id="a3387-112">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="a3387-112">-ClusterName</span></span>
<span data-ttu-id="a3387-113">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3387-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a3387-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3387-114">-DefaultProfile</span></span>
<span data-ttu-id="a3387-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a3387-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3387-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3387-116">-ResourceGroupName</span></span>
<span data-ttu-id="a3387-117">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a3387-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a3387-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3387-118">CommonParameters</span></span>
<span data-ttu-id="a3387-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3387-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3387-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3387-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3387-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3387-121">INPUTS</span></span>

### <span data-ttu-id="a3387-122">Nincs</span><span class="sxs-lookup"><span data-stu-id="a3387-122">None</span></span>

## <span data-ttu-id="a3387-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3387-123">OUTPUTS</span></span>

### <span data-ttu-id="a3387-124">Microsoft. Azure. Command. HDInsight. models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a3387-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="a3387-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3387-125">NOTES</span></span>

## <span data-ttu-id="a3387-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3387-126">RELATED LINKS</span></span>

[<span data-ttu-id="a3387-127">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a3387-127">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="a3387-128">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="a3387-128">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


