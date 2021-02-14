---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: ab97162fb2651bce8e242ca0cef7b497ffcf1bef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167442"
---
# <span data-ttu-id="b56f6-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b56f6-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="b56f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b56f6-102">SYNOPSIS</span></span>
<span data-ttu-id="b56f6-103">A megadott HDInsight-fürt eltávolítása az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="b56f6-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="b56f6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b56f6-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b56f6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b56f6-105">DESCRIPTION</span></span>
<span data-ttu-id="b56f6-106">A **Remove-AzHDInsightCluster** parancsmag eltávolítja a megadott HDInsight-szolgáltatáscsoportot egy előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="b56f6-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="b56f6-107">Ez a művelet a Hadoop Distributed File System (HDFS) rendszerben a fürtön tárolt összes adatot is törli.</span><span class="sxs-lookup"><span data-stu-id="b56f6-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="b56f6-108">A társított Azure Storage-fiókban tárolt adatok nem törlődnek.</span><span class="sxs-lookup"><span data-stu-id="b56f6-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="b56f6-109">A külső metastore-okban tárolt adatok nem törlődnek.</span><span class="sxs-lookup"><span data-stu-id="b56f6-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="b56f6-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b56f6-110">EXAMPLES</span></span>

### <span data-ttu-id="b56f6-111">1. példa: Azure HDInsight-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="b56f6-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="b56f6-112">Ez a parancs eltávolítja a -hadoop-001 nevű fürtöt.</span><span class="sxs-lookup"><span data-stu-id="b56f6-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b56f6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b56f6-113">PARAMETERS</span></span>

### <span data-ttu-id="b56f6-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b56f6-114">-ClusterName</span></span>
<span data-ttu-id="b56f6-115">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b56f6-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b56f6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b56f6-116">-DefaultProfile</span></span>
<span data-ttu-id="b56f6-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b56f6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b56f6-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b56f6-118">-PassThru</span></span>
<span data-ttu-id="b56f6-119">Ha a PassThru jelen van, kimenetként adja meg az eredményt</span><span class="sxs-lookup"><span data-stu-id="b56f6-119">If PassThru is present, output the result</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56f6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b56f6-120">-ResourceGroupName</span></span>
<span data-ttu-id="b56f6-121">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b56f6-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b56f6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b56f6-122">CommonParameters</span></span>
<span data-ttu-id="b56f6-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b56f6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b56f6-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b56f6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b56f6-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b56f6-125">INPUTS</span></span>

### <span data-ttu-id="b56f6-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="b56f6-126">None</span></span>
## <span data-ttu-id="b56f6-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b56f6-127">OUTPUTS</span></span>

### <span data-ttu-id="b56f6-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b56f6-128">System.Boolean</span></span>
## <span data-ttu-id="b56f6-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b56f6-129">NOTES</span></span>

## <span data-ttu-id="b56f6-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b56f6-130">RELATED LINKS</span></span>

[<span data-ttu-id="b56f6-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b56f6-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="b56f6-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b56f6-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


