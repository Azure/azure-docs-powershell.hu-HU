---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Remove-AzureRmHDInsightCluster.md
ms.openlocfilehash: a09da5122403d971d8b5d1abde79c8a9a95c3ecd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504160"
---
# <span data-ttu-id="67009-101">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="67009-101">Remove-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="67009-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="67009-102">SYNOPSIS</span></span>
<span data-ttu-id="67009-103">Eltávolítja a megadott HDInsight-fürtöt az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="67009-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67009-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="67009-104">SYNTAX</span></span>

```
Remove-AzureRmHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67009-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="67009-105">DESCRIPTION</span></span>
<span data-ttu-id="67009-106">A **Remove-AzureRmHDInsightCluster** parancsmag az előfizetésből eltávolítja a megadott HDInsight-fürtszolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="67009-106">The **Remove-AzureRmHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="67009-107">Ezzel a művelettel a Hadoop elosztott fájlrendszerében (HDFS) tárolt adatok is törlődnek.</span><span class="sxs-lookup"><span data-stu-id="67009-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="67009-108">A rendszer nem törli a kapcsolódó Azure-tárterületi fiókban tárolt adatait.</span><span class="sxs-lookup"><span data-stu-id="67009-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="67009-109">A külső metastores tárolt adatot nem törli a program.</span><span class="sxs-lookup"><span data-stu-id="67009-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="67009-110">Példák</span><span class="sxs-lookup"><span data-stu-id="67009-110">EXAMPLES</span></span>

### <span data-ttu-id="67009-111">Példa 1: Azure HDInsight-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="67009-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzureRmHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="67009-112">Ez a parancs eltávolítja a-Hadoop-001 nevű fürtöt.</span><span class="sxs-lookup"><span data-stu-id="67009-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="67009-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="67009-113">PARAMETERS</span></span>

### <span data-ttu-id="67009-114">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="67009-114">-ClusterName</span></span>
<span data-ttu-id="67009-115">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="67009-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="67009-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67009-116">-ResourceGroupName</span></span>
<span data-ttu-id="67009-117">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="67009-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="67009-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67009-118">-DefaultProfile</span></span>
<span data-ttu-id="67009-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="67009-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67009-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67009-120">CommonParameters</span></span>
<span data-ttu-id="67009-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="67009-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67009-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67009-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67009-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="67009-123">INPUTS</span></span>

## <span data-ttu-id="67009-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="67009-124">OUTPUTS</span></span>

### <span data-ttu-id="67009-125">Microsoft. Azure. Management. HDInsight. models. ClusterGetResponse</span><span class="sxs-lookup"><span data-stu-id="67009-125">Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse</span></span>

## <span data-ttu-id="67009-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="67009-126">NOTES</span></span>

## <span data-ttu-id="67009-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="67009-127">RELATED LINKS</span></span>

[<span data-ttu-id="67009-128">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="67009-128">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="67009-129">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="67009-129">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


