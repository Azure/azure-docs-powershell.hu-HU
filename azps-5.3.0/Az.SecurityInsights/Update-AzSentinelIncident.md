---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: c98270b4e69d80e18ba721de0a6379d40d21fc75
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479689"
---
# <span data-ttu-id="da986-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="da986-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="da986-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da986-102">SYNOPSIS</span></span>
<span data-ttu-id="da986-103">Incidens frissítése.</span><span class="sxs-lookup"><span data-stu-id="da986-103">Update an Incident.</span></span>

## <span data-ttu-id="da986-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="da986-104">SYNTAX</span></span>

### <span data-ttu-id="da986-105">IncidentId (default)</span><span class="sxs-lookup"><span data-stu-id="da986-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da986-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="da986-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da986-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="da986-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da986-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="da986-108">DESCRIPTION</span></span>
<span data-ttu-id="da986-109">Az **Update-AzSentinelIncident** parancsmag frissíti az incidenst a megadott munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="da986-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="da986-110">Az Incidens  objektumokat paraméterként vagy a folyamat műveleti jelének használatával is átadhatja, vagy megadhatja a szükséges paramétereket.</span><span class="sxs-lookup"><span data-stu-id="da986-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="da986-111">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="da986-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="da986-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="da986-112">EXAMPLES</span></span>

### <span data-ttu-id="da986-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="da986-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="da986-114">A parancs beállítja az Incident by *IncidentId tulajdonságot,* *és a Súlyosság* tulajdonságot Magasra *állítja.*</span><span class="sxs-lookup"><span data-stu-id="da986-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="da986-115">Minden más tulajdonság változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="da986-115">All other properties remain the same.</span></span>

## <span data-ttu-id="da986-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da986-116">PARAMETERS</span></span>

### <span data-ttu-id="da986-117">-Classification</span><span class="sxs-lookup"><span data-stu-id="da986-117">-Classification</span></span>
<span data-ttu-id="da986-118">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="da986-118">Incident Classificaiton.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da986-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="da986-119">-ClassificationComment</span></span>
<span data-ttu-id="da986-120">Incident Classificaiton Comment.</span><span class="sxs-lookup"><span data-stu-id="da986-120">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="da986-121">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="da986-121">-ClassificationReason</span></span>
<span data-ttu-id="da986-122">Incident Classificaiton Reason.</span><span class="sxs-lookup"><span data-stu-id="da986-122">Incident Classificaiton Reason.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da986-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da986-123">-DefaultProfile</span></span>
<span data-ttu-id="da986-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da986-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da986-125">-Leírás</span><span class="sxs-lookup"><span data-stu-id="da986-125">-Description</span></span>
<span data-ttu-id="da986-126">Leírás.</span><span class="sxs-lookup"><span data-stu-id="da986-126">Description.</span></span>

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

### <span data-ttu-id="da986-127">-IncidentID</span><span class="sxs-lookup"><span data-stu-id="da986-127">-IncidentID</span></span>
<span data-ttu-id="da986-128">Incidens azonosítója.</span><span class="sxs-lookup"><span data-stu-id="da986-128">Incident Id.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId, ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da986-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da986-129">-InputObject</span></span>
<span data-ttu-id="da986-130">InputObject.</span><span class="sxs-lookup"><span data-stu-id="da986-130">InputObject.</span></span>

```yaml
Type: PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da986-131">-Label</span><span class="sxs-lookup"><span data-stu-id="da986-131">-Label</span></span>
<span data-ttu-id="da986-132">Incidenscímkék.</span><span class="sxs-lookup"><span data-stu-id="da986-132">Incident Labels.</span></span>

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

### <span data-ttu-id="da986-133">-Tulajdonos</span><span class="sxs-lookup"><span data-stu-id="da986-133">-Owner</span></span>
<span data-ttu-id="da986-134">Incidens tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="da986-134">Incident Owner.</span></span>

```yaml
Type: PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da986-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da986-135">-ResourceGroupName</span></span>
<span data-ttu-id="da986-136">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="da986-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da986-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da986-137">-ResourceId</span></span>
<span data-ttu-id="da986-138">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="da986-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da986-139">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="da986-139">-Severity</span></span>
<span data-ttu-id="da986-140">Incidens súlyossága.</span><span class="sxs-lookup"><span data-stu-id="da986-140">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da986-141">-Állapot</span><span class="sxs-lookup"><span data-stu-id="da986-141">-Status</span></span>
<span data-ttu-id="da986-142">Incidens állapota.</span><span class="sxs-lookup"><span data-stu-id="da986-142">Incident Status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da986-143">-Title</span><span class="sxs-lookup"><span data-stu-id="da986-143">-Title</span></span>
<span data-ttu-id="da986-144">Incidens címe.</span><span class="sxs-lookup"><span data-stu-id="da986-144">Incident Title.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da986-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="da986-145">-WorkspaceName</span></span>
<span data-ttu-id="da986-146">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="da986-146">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da986-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da986-147">-Confirm</span></span>
<span data-ttu-id="da986-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="da986-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da986-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da986-149">-WhatIf</span></span>
<span data-ttu-id="da986-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="da986-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da986-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da986-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da986-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da986-152">CommonParameters</span></span>
<span data-ttu-id="da986-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da986-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da986-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da986-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da986-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da986-155">INPUTS</span></span>

### <span data-ttu-id="da986-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="da986-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="da986-157">System.String</span><span class="sxs-lookup"><span data-stu-id="da986-157">System.String</span></span>

### <span data-ttu-id="da986-158">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="da986-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="da986-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="da986-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="da986-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da986-160">OUTPUTS</span></span>

### <span data-ttu-id="da986-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="da986-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="da986-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="da986-162">NOTES</span></span>

## <span data-ttu-id="da986-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da986-163">RELATED LINKS</span></span>
