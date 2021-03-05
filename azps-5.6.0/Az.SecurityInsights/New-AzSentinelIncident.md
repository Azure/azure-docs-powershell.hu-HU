---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
ms.openlocfilehash: 6cb65832484c7038f5740c481836d8fe889ebc94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005653"
---
# <span data-ttu-id="793e9-101">New-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="793e9-101">New-AzSentinelIncident</span></span>

## <span data-ttu-id="793e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="793e9-102">SYNOPSIS</span></span>
<span data-ttu-id="793e9-103">Incidens létrehozása.</span><span class="sxs-lookup"><span data-stu-id="793e9-103">Create an Incident.</span></span>

## <span data-ttu-id="793e9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="793e9-104">SYNTAX</span></span>

```
New-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-Classificaton <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="793e9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="793e9-105">DESCRIPTION</span></span>
<span data-ttu-id="793e9-106">A **New-AzSentinelIncident** parancsmag létrehoz egy incidenst a megadott munkaterületről.</span><span class="sxs-lookup"><span data-stu-id="793e9-106">The **New-AzSentinelIncident** cmdlet creates a Incident from the specified workspace.</span></span>
<span data-ttu-id="793e9-107">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="793e9-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="793e9-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="793e9-108">EXAMPLES</span></span>

### <span data-ttu-id="793e9-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="793e9-109">Example 1</span></span>
```powershell
PS C:\> $Incident = New-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Title "NewIncident" -Severity Low -Status New
```

<span data-ttu-id="793e9-110">Ez a példa létrehoz egy **incidenst** a megadott munkaterületen, majd azt a $Incident tárolja.</span><span class="sxs-lookup"><span data-stu-id="793e9-110">This example creates an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="793e9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="793e9-111">PARAMETERS</span></span>

### <span data-ttu-id="793e9-112">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="793e9-112">-ClassificationComment</span></span>
<span data-ttu-id="793e9-113">Incident Classificaiton Comment.</span><span class="sxs-lookup"><span data-stu-id="793e9-113">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="793e9-114">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="793e9-114">-ClassificationReason</span></span>
<span data-ttu-id="793e9-115">Incident Classificaiton Reason.</span><span class="sxs-lookup"><span data-stu-id="793e9-115">Incident Classificaiton Reason.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="793e9-116">-Classificaton</span><span class="sxs-lookup"><span data-stu-id="793e9-116">-Classificaton</span></span>
<span data-ttu-id="793e9-117">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="793e9-117">Incident Classificaiton.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="793e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="793e9-118">-DefaultProfile</span></span>
<span data-ttu-id="793e9-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="793e9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="793e9-120">-Leírás</span><span class="sxs-lookup"><span data-stu-id="793e9-120">-Description</span></span>
<span data-ttu-id="793e9-121">Leírás.</span><span class="sxs-lookup"><span data-stu-id="793e9-121">Description.</span></span>

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

### <span data-ttu-id="793e9-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="793e9-122">-IncidentId</span></span>
<span data-ttu-id="793e9-123">Incidens azonosítója.</span><span class="sxs-lookup"><span data-stu-id="793e9-123">Incident Id.</span></span>

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

### <span data-ttu-id="793e9-124">-Label</span><span class="sxs-lookup"><span data-stu-id="793e9-124">-Label</span></span>
<span data-ttu-id="793e9-125">Incidenscímkék.</span><span class="sxs-lookup"><span data-stu-id="793e9-125">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="793e9-126">-Tulajdonos</span><span class="sxs-lookup"><span data-stu-id="793e9-126">-Owner</span></span>
<span data-ttu-id="793e9-127">Incidens tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="793e9-127">Incident Owner.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="793e9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="793e9-128">-ResourceGroupName</span></span>
<span data-ttu-id="793e9-129">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="793e9-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="793e9-130">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="793e9-130">-Severity</span></span>
<span data-ttu-id="793e9-131">Incidens súlyossága.</span><span class="sxs-lookup"><span data-stu-id="793e9-131">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="793e9-132">-Állapot</span><span class="sxs-lookup"><span data-stu-id="793e9-132">-Status</span></span>
<span data-ttu-id="793e9-133">Incidens állapota.</span><span class="sxs-lookup"><span data-stu-id="793e9-133">Incident Status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="793e9-134">-Title</span><span class="sxs-lookup"><span data-stu-id="793e9-134">-Title</span></span>
<span data-ttu-id="793e9-135">Incidens címe.</span><span class="sxs-lookup"><span data-stu-id="793e9-135">Incident Title.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="793e9-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="793e9-136">-WorkspaceName</span></span>
<span data-ttu-id="793e9-137">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="793e9-137">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="793e9-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="793e9-138">-Confirm</span></span>
<span data-ttu-id="793e9-139">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="793e9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="793e9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="793e9-140">-WhatIf</span></span>
<span data-ttu-id="793e9-141">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="793e9-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="793e9-142">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="793e9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="793e9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="793e9-143">CommonParameters</span></span>
<span data-ttu-id="793e9-144">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="793e9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="793e9-145">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="793e9-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="793e9-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="793e9-146">INPUTS</span></span>

### <span data-ttu-id="793e9-147">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="793e9-147">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
### <span data-ttu-id="793e9-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="793e9-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>
## <span data-ttu-id="793e9-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="793e9-149">OUTPUTS</span></span>

### <span data-ttu-id="793e9-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="793e9-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="793e9-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="793e9-151">NOTES</span></span>

## <span data-ttu-id="793e9-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="793e9-152">RELATED LINKS</span></span>
