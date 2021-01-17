---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481044"
---
# <span data-ttu-id="73d06-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="73d06-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="73d06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73d06-102">SYNOPSIS</span></span>
<span data-ttu-id="73d06-103">Munkaterület leválasztása szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="73d06-103">Unlink service for workspace</span></span>

## <span data-ttu-id="73d06-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="73d06-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="73d06-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="73d06-105">DESCRIPTION</span></span>
<span data-ttu-id="73d06-106">Munkaterület leválasztása szolgáltatás</span><span class="sxs-lookup"><span data-stu-id="73d06-106">Unlink service for workspace</span></span>

## <span data-ttu-id="73d06-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="73d06-107">EXAMPLES</span></span>

### <span data-ttu-id="73d06-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="73d06-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="73d06-109">Munkaterület csatolt szolgáltatásának leválasztása</span><span class="sxs-lookup"><span data-stu-id="73d06-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="73d06-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73d06-110">PARAMETERS</span></span>

### <span data-ttu-id="73d06-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73d06-111">-AsJob</span></span>
<span data-ttu-id="73d06-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="73d06-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73d06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73d06-113">-DefaultProfile</span></span>
<span data-ttu-id="73d06-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73d06-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73d06-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="73d06-115">-LinkedServiceName</span></span>
<span data-ttu-id="73d06-116">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="73d06-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d06-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73d06-117">-ResourceGroupName</span></span>
<span data-ttu-id="73d06-118">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="73d06-118">The resource group name.</span></span>

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

### <span data-ttu-id="73d06-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="73d06-119">-WorkspaceName</span></span>
<span data-ttu-id="73d06-120">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="73d06-120">The Workspace name.</span></span>

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

### <span data-ttu-id="73d06-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73d06-121">-Confirm</span></span>
<span data-ttu-id="73d06-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="73d06-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73d06-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73d06-123">-WhatIf</span></span>
<span data-ttu-id="73d06-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="73d06-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73d06-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73d06-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73d06-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73d06-126">CommonParameters</span></span>
<span data-ttu-id="73d06-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73d06-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73d06-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73d06-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73d06-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73d06-129">INPUTS</span></span>

### <span data-ttu-id="73d06-130">System.String</span><span class="sxs-lookup"><span data-stu-id="73d06-130">System.String</span></span>

## <span data-ttu-id="73d06-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73d06-131">OUTPUTS</span></span>

### <span data-ttu-id="73d06-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="73d06-132">System.Boolean</span></span>

## <span data-ttu-id="73d06-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="73d06-133">NOTES</span></span>

## <span data-ttu-id="73d06-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73d06-134">RELATED LINKS</span></span>
