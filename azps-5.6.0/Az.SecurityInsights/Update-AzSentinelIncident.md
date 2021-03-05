---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: 03062015b1f9d14688488887ed226f1b697589ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015990"
---
# <span data-ttu-id="88042-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="88042-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="88042-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88042-102">SYNOPSIS</span></span>
<span data-ttu-id="88042-103">Incidens frissítése.</span><span class="sxs-lookup"><span data-stu-id="88042-103">Update an Incident.</span></span>

## <span data-ttu-id="88042-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="88042-104">SYNTAX</span></span>

### <span data-ttu-id="88042-105">IncidentId (default)</span><span class="sxs-lookup"><span data-stu-id="88042-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88042-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="88042-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88042-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="88042-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88042-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="88042-108">DESCRIPTION</span></span>
<span data-ttu-id="88042-109">Az **Update-AzSentinelIncident** parancsmag frissíti az incidenst a megadott munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="88042-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="88042-110">Az Incidens objektumokat paraméterként vagy a folyamat műveleti jelének használatával is átadhatja, vagy megadhatja **a** szükséges paramétereket.</span><span class="sxs-lookup"><span data-stu-id="88042-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="88042-111">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="88042-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="88042-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="88042-112">EXAMPLES</span></span>

### <span data-ttu-id="88042-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="88042-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="88042-114">A parancs beállítja az Incident by *IncidentId tulajdonságot,* *és a Súlyosság* tulajdonságot Magasra *állítja.*</span><span class="sxs-lookup"><span data-stu-id="88042-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="88042-115">Minden más tulajdonság változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="88042-115">All other properties remain the same.</span></span>

## <span data-ttu-id="88042-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88042-116">PARAMETERS</span></span>

### <span data-ttu-id="88042-117">-Classification</span><span class="sxs-lookup"><span data-stu-id="88042-117">-Classification</span></span>
<span data-ttu-id="88042-118">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="88042-118">Incident Classificaiton.</span></span>

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

### <span data-ttu-id="88042-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="88042-119">-ClassificationComment</span></span>
<span data-ttu-id="88042-120">Incident Classificaiton Comment.</span><span class="sxs-lookup"><span data-stu-id="88042-120">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="88042-121">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="88042-121">-ClassificationReason</span></span>
<span data-ttu-id="88042-122">Incident Classificaiton Reason.</span><span class="sxs-lookup"><span data-stu-id="88042-122">Incident Classificaiton Reason.</span></span>

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

### <span data-ttu-id="88042-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88042-123">-DefaultProfile</span></span>
<span data-ttu-id="88042-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="88042-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88042-125">-Leírás</span><span class="sxs-lookup"><span data-stu-id="88042-125">-Description</span></span>
<span data-ttu-id="88042-126">Leírás.</span><span class="sxs-lookup"><span data-stu-id="88042-126">Description.</span></span>

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

### <span data-ttu-id="88042-127">-IncidentID</span><span class="sxs-lookup"><span data-stu-id="88042-127">-IncidentID</span></span>
<span data-ttu-id="88042-128">Incidens azonosítója.</span><span class="sxs-lookup"><span data-stu-id="88042-128">Incident Id.</span></span>

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

### <span data-ttu-id="88042-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88042-129">-InputObject</span></span>
<span data-ttu-id="88042-130">InputObject.</span><span class="sxs-lookup"><span data-stu-id="88042-130">InputObject.</span></span>

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

### <span data-ttu-id="88042-131">-Label</span><span class="sxs-lookup"><span data-stu-id="88042-131">-Label</span></span>
<span data-ttu-id="88042-132">Incidenscímkék.</span><span class="sxs-lookup"><span data-stu-id="88042-132">Incident Labels.</span></span>

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

### <span data-ttu-id="88042-133">-Tulajdonos</span><span class="sxs-lookup"><span data-stu-id="88042-133">-Owner</span></span>
<span data-ttu-id="88042-134">Incidens tulajdonosa.</span><span class="sxs-lookup"><span data-stu-id="88042-134">Incident Owner.</span></span>

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

### <span data-ttu-id="88042-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88042-135">-ResourceGroupName</span></span>
<span data-ttu-id="88042-136">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="88042-136">Resource group name.</span></span>

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

### <span data-ttu-id="88042-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88042-137">-ResourceId</span></span>
<span data-ttu-id="88042-138">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="88042-138">Resource Id.</span></span>

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

### <span data-ttu-id="88042-139">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="88042-139">-Severity</span></span>
<span data-ttu-id="88042-140">Incidens súlyossága.</span><span class="sxs-lookup"><span data-stu-id="88042-140">Incident Severity.</span></span>

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

### <span data-ttu-id="88042-141">-Állapot</span><span class="sxs-lookup"><span data-stu-id="88042-141">-Status</span></span>
<span data-ttu-id="88042-142">Incidens állapota.</span><span class="sxs-lookup"><span data-stu-id="88042-142">Incident Status.</span></span>

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

### <span data-ttu-id="88042-143">-Title</span><span class="sxs-lookup"><span data-stu-id="88042-143">-Title</span></span>
<span data-ttu-id="88042-144">Incidens címe.</span><span class="sxs-lookup"><span data-stu-id="88042-144">Incident Title.</span></span>

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

### <span data-ttu-id="88042-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="88042-145">-WorkspaceName</span></span>
<span data-ttu-id="88042-146">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="88042-146">Workspace Name.</span></span>

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

### <span data-ttu-id="88042-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88042-147">-Confirm</span></span>
<span data-ttu-id="88042-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="88042-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88042-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88042-149">-WhatIf</span></span>
<span data-ttu-id="88042-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="88042-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88042-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="88042-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88042-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88042-152">CommonParameters</span></span>
<span data-ttu-id="88042-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88042-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88042-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88042-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88042-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88042-155">INPUTS</span></span>

### <span data-ttu-id="88042-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="88042-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="88042-157">System.String</span><span class="sxs-lookup"><span data-stu-id="88042-157">System.String</span></span>

### <span data-ttu-id="88042-158">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="88042-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="88042-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="88042-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="88042-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="88042-160">OUTPUTS</span></span>

### <span data-ttu-id="88042-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="88042-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="88042-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="88042-162">NOTES</span></span>

## <span data-ttu-id="88042-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="88042-163">RELATED LINKS</span></span>
