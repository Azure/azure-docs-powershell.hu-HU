---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: c4a3f33094e5337306e44e2b310cd7cce32e8887
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328365"
---
# <span data-ttu-id="64911-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="64911-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="64911-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64911-102">SYNOPSIS</span></span>
<span data-ttu-id="64911-103">A megadott HDInsight-fürt eltávolítása az aktuális előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="64911-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="64911-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="64911-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64911-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="64911-105">DESCRIPTION</span></span>
<span data-ttu-id="64911-106">A **Remove-AzHDInsightCluster** parancsmag eltávolítja a megadott HDInsight-szolgáltatáscsoportot az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="64911-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="64911-107">Ez a művelet a Hadoop Distributed File System (HDFS) rendszerben a fürtön tárolt összes adatot is törli.</span><span class="sxs-lookup"><span data-stu-id="64911-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="64911-108">A társított Azure Storage-fiókban tárolt adatok nem törlődnek.</span><span class="sxs-lookup"><span data-stu-id="64911-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="64911-109">A külső metastore-okban tárolt adatok nem törlődnek.</span><span class="sxs-lookup"><span data-stu-id="64911-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="64911-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="64911-110">EXAMPLES</span></span>

### <span data-ttu-id="64911-111">1. példa: Azure HDInsight-fürt törlése</span><span class="sxs-lookup"><span data-stu-id="64911-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="64911-112">Ez a parancs eltávolítja a"-hadoop-001" nevű fürtöt.</span><span class="sxs-lookup"><span data-stu-id="64911-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="64911-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64911-113">PARAMETERS</span></span>

### <span data-ttu-id="64911-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="64911-114">-ClusterName</span></span>
<span data-ttu-id="64911-115">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64911-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="64911-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64911-116">-DefaultProfile</span></span>
<span data-ttu-id="64911-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="64911-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64911-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64911-118">-ResourceGroupName</span></span>
<span data-ttu-id="64911-119">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64911-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="64911-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64911-120">-PassThru</span></span>
<span data-ttu-id="64911-121">Ha a PassThru jelen van, kimenetként adja meg az eredményt</span><span class="sxs-lookup"><span data-stu-id="64911-121">If PassThru is present, output the result</span></span>

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

### <span data-ttu-id="64911-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64911-122">CommonParameters</span></span>
<span data-ttu-id="64911-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64911-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64911-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64911-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64911-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64911-125">INPUTS</span></span>

### <span data-ttu-id="64911-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="64911-126">None</span></span>
## <span data-ttu-id="64911-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64911-127">OUTPUTS</span></span>

### <span data-ttu-id="64911-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="64911-128">System.Boolean</span></span>
## <span data-ttu-id="64911-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="64911-129">NOTES</span></span>

## <span data-ttu-id="64911-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64911-130">RELATED LINKS</span></span>

[<span data-ttu-id="64911-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="64911-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="64911-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="64911-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


