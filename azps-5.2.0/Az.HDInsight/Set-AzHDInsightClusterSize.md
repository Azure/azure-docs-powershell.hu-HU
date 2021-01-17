---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: A9A8C4B9-6346-4186-9D73-3A56437BFB2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightclustersize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightClusterSize.md
ms.openlocfilehash: 8f34e9233da61bb2381c99c33922fa4332b588fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328310"
---
# <span data-ttu-id="481c6-101">Set-AzHDInsightClusterSize</span><span class="sxs-lookup"><span data-stu-id="481c6-101">Set-AzHDInsightClusterSize</span></span>

## <span data-ttu-id="481c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="481c6-102">SYNOPSIS</span></span>
<span data-ttu-id="481c6-103">Beállítja egy adott fürt dolgozói csomópontjainak számát.</span><span class="sxs-lookup"><span data-stu-id="481c6-103">Sets the number of Worker nodes in a specified cluster.</span></span>

## <span data-ttu-id="481c6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="481c6-104">SYNTAX</span></span>

```
Set-AzHDInsightClusterSize [-ClusterName] <String> [-TargetInstanceCount] <Int32> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="481c6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="481c6-105">DESCRIPTION</span></span>
<span data-ttu-id="481c6-106">A **Set-AzHDInsightClusterSize** parancsmag beállítja egy adott Azure HDInsight-fürt dolgozói csomópontjainak számát.</span><span class="sxs-lookup"><span data-stu-id="481c6-106">The **Set-AzHDInsightClusterSize** cmdlet sets the number of Worker nodes in a specified Azure HDInsight cluster.</span></span>

## <span data-ttu-id="481c6-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="481c6-107">EXAMPLES</span></span>

### <span data-ttu-id="481c6-108">1. példa: Adott fürt méretének beállítása</span><span class="sxs-lookup"><span data-stu-id="481c6-108">Example 1: Set the size of a specified cluster</span></span>
```
PS C:\>Set-AzHDInsightClusterSize -ClusterName "your-hadoop-001" -TargetInstanceCount 6
```

<span data-ttu-id="481c6-109">Ez a parancs beállítja a -hadoop-001 nevű fürt méretét.</span><span class="sxs-lookup"><span data-stu-id="481c6-109">This command sets the size of the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="481c6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="481c6-110">PARAMETERS</span></span>

### <span data-ttu-id="481c6-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="481c6-111">-ClusterName</span></span>
<span data-ttu-id="481c6-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="481c6-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="481c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="481c6-113">-DefaultProfile</span></span>
<span data-ttu-id="481c6-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="481c6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="481c6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="481c6-115">-ResourceGroupName</span></span>
<span data-ttu-id="481c6-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="481c6-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="481c6-117">-TargetInstanceCount</span><span class="sxs-lookup"><span data-stu-id="481c6-117">-TargetInstanceCount</span></span>
<span data-ttu-id="481c6-118">Megadja a fürtben a munkavégző csomópontok kívánt számát.</span><span class="sxs-lookup"><span data-stu-id="481c6-118">Specifies the desired number of Worker nodes in the cluster.</span></span>

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

### <span data-ttu-id="481c6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="481c6-119">CommonParameters</span></span>
<span data-ttu-id="481c6-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="481c6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="481c6-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="481c6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="481c6-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="481c6-122">INPUTS</span></span>

### <span data-ttu-id="481c6-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="481c6-123">None</span></span>

## <span data-ttu-id="481c6-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="481c6-124">OUTPUTS</span></span>

### <span data-ttu-id="481c6-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span><span class="sxs-lookup"><span data-stu-id="481c6-125">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="481c6-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="481c6-126">NOTES</span></span>

## <span data-ttu-id="481c6-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="481c6-127">RELATED LINKS</span></span>
