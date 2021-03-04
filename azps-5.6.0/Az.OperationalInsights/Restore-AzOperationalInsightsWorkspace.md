---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1035d918870a15000be066fd59cc72913d8d8cf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937874"
---
# <span data-ttu-id="884e1-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="884e1-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="884e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="884e1-102">SYNOPSIS</span></span>
<span data-ttu-id="884e1-103">Törölt munkaterület visszaállítása</span><span class="sxs-lookup"><span data-stu-id="884e1-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="884e1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="884e1-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="884e1-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="884e1-105">DESCRIPTION</span></span>
<span data-ttu-id="884e1-106">Törölt munkaterület visszaállítása</span><span class="sxs-lookup"><span data-stu-id="884e1-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="884e1-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="884e1-107">EXAMPLES</span></span>

### <span data-ttu-id="884e1-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="884e1-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="884e1-109">Törölt munkaterület visszaállítása</span><span class="sxs-lookup"><span data-stu-id="884e1-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="884e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="884e1-110">PARAMETERS</span></span>

### <span data-ttu-id="884e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="884e1-111">-DefaultProfile</span></span>
<span data-ttu-id="884e1-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="884e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="884e1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="884e1-113">-Force</span></span>
<span data-ttu-id="884e1-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="884e1-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="884e1-115">-Location</span><span class="sxs-lookup"><span data-stu-id="884e1-115">-Location</span></span>
<span data-ttu-id="884e1-116">Az a földrajzi terület, ahol a munkaterület létrejön.</span><span class="sxs-lookup"><span data-stu-id="884e1-116">The geographic region that the workspace will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="884e1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="884e1-117">-Name</span></span>
<span data-ttu-id="884e1-118">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="884e1-118">The workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="884e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="884e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="884e1-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="884e1-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="884e1-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="884e1-121">-Confirm</span></span>
<span data-ttu-id="884e1-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="884e1-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884e1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="884e1-123">-WhatIf</span></span>
<span data-ttu-id="884e1-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="884e1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="884e1-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="884e1-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="884e1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="884e1-126">CommonParameters</span></span>
<span data-ttu-id="884e1-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="884e1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="884e1-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="884e1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="884e1-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="884e1-129">INPUTS</span></span>

### <span data-ttu-id="884e1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="884e1-130">System.String</span></span>

## <span data-ttu-id="884e1-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="884e1-131">OUTPUTS</span></span>

### <span data-ttu-id="884e1-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="884e1-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="884e1-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="884e1-133">NOTES</span></span>

## <span data-ttu-id="884e1-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="884e1-134">RELATED LINKS</span></span>
