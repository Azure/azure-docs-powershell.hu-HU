---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169546"
---
# <span data-ttu-id="96f6b-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="96f6b-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="96f6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="96f6b-103">Törölt munkaterület visszaállítása</span><span class="sxs-lookup"><span data-stu-id="96f6b-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="96f6b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="96f6b-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96f6b-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="96f6b-105">DESCRIPTION</span></span>
<span data-ttu-id="96f6b-106">Törölt munkaterület visszaállítása</span><span class="sxs-lookup"><span data-stu-id="96f6b-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="96f6b-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="96f6b-107">EXAMPLES</span></span>

### <span data-ttu-id="96f6b-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="96f6b-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="96f6b-109">Törölt munkaterület visszaállítása</span><span class="sxs-lookup"><span data-stu-id="96f6b-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="96f6b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96f6b-110">PARAMETERS</span></span>

### <span data-ttu-id="96f6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96f6b-111">-DefaultProfile</span></span>
<span data-ttu-id="96f6b-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="96f6b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96f6b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="96f6b-113">-Force</span></span>
<span data-ttu-id="96f6b-114">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="96f6b-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="96f6b-115">-Location</span><span class="sxs-lookup"><span data-stu-id="96f6b-115">-Location</span></span>
<span data-ttu-id="96f6b-116">Az a földrajzi terület, ahol a munkaterület létrejön.</span><span class="sxs-lookup"><span data-stu-id="96f6b-116">The geographic region that the workspace will be created in.</span></span>

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

### <span data-ttu-id="96f6b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="96f6b-117">-Name</span></span>
<span data-ttu-id="96f6b-118">A munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="96f6b-118">The workspace name.</span></span>

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

### <span data-ttu-id="96f6b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96f6b-119">-ResourceGroupName</span></span>
<span data-ttu-id="96f6b-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="96f6b-120">The resource group name.</span></span>

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

### <span data-ttu-id="96f6b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96f6b-121">-Confirm</span></span>
<span data-ttu-id="96f6b-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="96f6b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96f6b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96f6b-123">-WhatIf</span></span>
<span data-ttu-id="96f6b-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="96f6b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96f6b-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="96f6b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96f6b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f6b-126">CommonParameters</span></span>
<span data-ttu-id="96f6b-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96f6b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f6b-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96f6b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f6b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96f6b-129">INPUTS</span></span>

### <span data-ttu-id="96f6b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="96f6b-130">System.String</span></span>

## <span data-ttu-id="96f6b-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96f6b-131">OUTPUTS</span></span>

### <span data-ttu-id="96f6b-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="96f6b-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="96f6b-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="96f6b-133">NOTES</span></span>

## <span data-ttu-id="96f6b-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96f6b-134">RELATED LINKS</span></span>
