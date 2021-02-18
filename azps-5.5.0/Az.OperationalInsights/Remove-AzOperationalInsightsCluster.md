---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202334"
---
# <span data-ttu-id="982de-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="982de-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="982de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="982de-102">SYNOPSIS</span></span>
<span data-ttu-id="982de-103">Fürt törlése</span><span class="sxs-lookup"><span data-stu-id="982de-103">Delete cluster</span></span>

## <span data-ttu-id="982de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="982de-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="982de-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="982de-105">DESCRIPTION</span></span>
<span data-ttu-id="982de-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span><span class="sxs-lookup"><span data-stu-id="982de-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="982de-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="982de-107">EXAMPLES</span></span>

### <span data-ttu-id="982de-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="982de-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="982de-109">Fürt törlése</span><span class="sxs-lookup"><span data-stu-id="982de-109">Delete cluster</span></span>

## <span data-ttu-id="982de-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="982de-110">PARAMETERS</span></span>

### <span data-ttu-id="982de-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="982de-111">-AsJob</span></span>
<span data-ttu-id="982de-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="982de-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="982de-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="982de-113">-ClusterName</span></span>
<span data-ttu-id="982de-114">A fürt neve.</span><span class="sxs-lookup"><span data-stu-id="982de-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="982de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="982de-115">-DefaultProfile</span></span>
<span data-ttu-id="982de-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="982de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="982de-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="982de-117">-ResourceGroupName</span></span>
<span data-ttu-id="982de-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="982de-118">The resource group name.</span></span>

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

### <span data-ttu-id="982de-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="982de-119">-Confirm</span></span>
<span data-ttu-id="982de-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="982de-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="982de-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="982de-121">-WhatIf</span></span>
<span data-ttu-id="982de-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="982de-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="982de-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="982de-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="982de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="982de-124">CommonParameters</span></span>
<span data-ttu-id="982de-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="982de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="982de-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="982de-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="982de-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="982de-127">INPUTS</span></span>

### <span data-ttu-id="982de-128">System.String</span><span class="sxs-lookup"><span data-stu-id="982de-128">System.String</span></span>

## <span data-ttu-id="982de-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="982de-129">OUTPUTS</span></span>

### <span data-ttu-id="982de-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="982de-130">System.Boolean</span></span>

## <span data-ttu-id="982de-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="982de-131">NOTES</span></span>

## <span data-ttu-id="982de-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="982de-132">RELATED LINKS</span></span>
