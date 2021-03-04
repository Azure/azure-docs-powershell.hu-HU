---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelAlertRule.md
ms.openlocfilehash: 86b6067e13a7b4d1d90e8fcb3d308af797dab354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927554"
---
# <span data-ttu-id="15a76-101">Update-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="15a76-101">Update-AzSentinelAlertRule</span></span>

## <span data-ttu-id="15a76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15a76-102">SYNOPSIS</span></span>
<span data-ttu-id="15a76-103">Analytic (riasztási szabály) létrehozása</span><span class="sxs-lookup"><span data-stu-id="15a76-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="15a76-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="15a76-104">SYNTAX</span></span>

### <span data-ttu-id="15a76-105">AlertRuleId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="15a76-105">AlertRuleId (Default)</span></span>
```
Update-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled] [-DisplayName <String>]
 [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15a76-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="15a76-106">InputObject</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -InputObject <PSSentinelAlertRule>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15a76-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="15a76-107">ResourceId</span></span>
```
Update-AzSentinelAlertRule [-AlertRuleTemplateName <String>] [-Enabled] [-Disabled]
 [-DisplayName <String>] [-ProductFilter <String>] [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>] [-SuppressionDuration <TimeSpan>]
 [-SuppressionEnabled] [-SuppressionDisabled] [-Query <String>] [-QueryFrequency <TimeSpan>]
 [-QueryPeriod <TimeSpan>] [-Severity <String>] [-Tactics <System.Collections.Generic.IList`1[System.String]>]
 [-TriggerOperator <TriggerOperator>] [-TriggerThreshold <Int32>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15a76-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="15a76-108">DESCRIPTION</span></span>
<span data-ttu-id="15a76-109">Az **Update-AzSentinelAlertRule parancsmag** frissíti az Analytic (Riasztási szabály) parancsmagot a megadott munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="15a76-109">The **Update-AzSentinelAlertRule** cmdlet updates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="15a76-110">Használhat -InputObject vagy -ResourceId vagy -AlertId értékeket.</span><span class="sxs-lookup"><span data-stu-id="15a76-110">You can use an -InputObject or -ResourceId or -AlertId.</span></span>  <span data-ttu-id="15a76-111">Frissíthet 1 vagy több proprtery parmaterst.</span><span class="sxs-lookup"><span data-stu-id="15a76-111">You can update 1 or more proprtery parmaters.</span></span>
<span data-ttu-id="15a76-112">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="15a76-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>


## <span data-ttu-id="15a76-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="15a76-113">EXAMPLES</span></span>

### <span data-ttu-id="15a76-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="15a76-114">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -Disabled -DisplayName "Disabled-AlertRuleDisplayName"
```

<span data-ttu-id="15a76-115">Ebben a példában egy **AlertRule-beállítást** letiltottra, és átnevezünk  *Disabled-AlertRuleDisplayName névre.*</span><span class="sxs-lookup"><span data-stu-id="15a76-115">This example updates an **AlertRule** setting it to *Disabled* and renames to *Disabled-AlertRuleDisplayName*.</span></span>  <span data-ttu-id="15a76-116">Minden más tulajdonság változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="15a76-116">All other properties will remain the same.</span></span>

### <span data-ttu-id="15a76-117">2. példa</span><span class="sxs-lookup"><span data-stu-id="15a76-117">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
PS C:\> Update-AzSentinelAlertRule -InputObject $AlertRule -Disabled
```

<span data-ttu-id="15a76-118">Ebben a példában egy **AlertRule-t** letiltott InputObject beállítással *frissül.*</span><span class="sxs-lookup"><span data-stu-id="15a76-118">This example updates an **AlertRule** using an InputObject setting it to *Disabled*.</span></span>  <span data-ttu-id="15a76-119">Minden más tulajdonság változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="15a76-119">All other properties will remain the same.</span></span>


## <span data-ttu-id="15a76-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15a76-120">PARAMETERS</span></span>

### <span data-ttu-id="15a76-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="15a76-121">-AlertRuleId</span></span>
<span data-ttu-id="15a76-122">Riasztási szabály azonosítója.</span><span class="sxs-lookup"><span data-stu-id="15a76-122">Alert Rule Id.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="15a76-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="15a76-124">Értesítési szabálysablon.</span><span class="sxs-lookup"><span data-stu-id="15a76-124">Alert Rule Template.</span></span>

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

### <span data-ttu-id="15a76-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a76-125">-DefaultProfile</span></span>
<span data-ttu-id="15a76-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15a76-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a76-127">-Leírás</span><span class="sxs-lookup"><span data-stu-id="15a76-127">-Description</span></span>
<span data-ttu-id="15a76-128">Leírás.</span><span class="sxs-lookup"><span data-stu-id="15a76-128">Description.</span></span>

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

### <span data-ttu-id="15a76-129">-Disabled</span><span class="sxs-lookup"><span data-stu-id="15a76-129">-Disabled</span></span>
<span data-ttu-id="15a76-130">Értesítési szabály letiltva.</span><span class="sxs-lookup"><span data-stu-id="15a76-130">Alert Rule Disabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="15a76-131">-DisplayName</span></span>
<span data-ttu-id="15a76-132">Értesítési szabály megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="15a76-132">Alert Rule Display Name.</span></span>

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

### <span data-ttu-id="15a76-133">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="15a76-133">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="15a76-134">Alert Rule Display Names Exclude Filter.</span><span class="sxs-lookup"><span data-stu-id="15a76-134">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-135">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="15a76-135">-DisplayNamesFilter</span></span>
<span data-ttu-id="15a76-136">Riasztási szabály megjelenítendő nevek szűrője.</span><span class="sxs-lookup"><span data-stu-id="15a76-136">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-137">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="15a76-137">-Enabled</span></span>
<span data-ttu-id="15a76-138">Értesítési szabály engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="15a76-138">Alert Rule Enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15a76-139">-InputObject</span></span>
<span data-ttu-id="15a76-140">InputObject.</span><span class="sxs-lookup"><span data-stu-id="15a76-140">InputObject.</span></span>

```yaml
Type: PSSentinelAlertRule
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="15a76-141">-ProductFilter</span></span>
<span data-ttu-id="15a76-142">Riasztási szabály termékszűrője.</span><span class="sxs-lookup"><span data-stu-id="15a76-142">Alert Rule Product Filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-143">-Query</span><span class="sxs-lookup"><span data-stu-id="15a76-143">-Query</span></span>
<span data-ttu-id="15a76-144">Riasztási szabály lekérdezése.</span><span class="sxs-lookup"><span data-stu-id="15a76-144">Alert Rule Query.</span></span>

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

### <span data-ttu-id="15a76-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="15a76-145">-QueryFrequency</span></span>
<span data-ttu-id="15a76-146">Riasztási szabály lekérdezésének gyakorisága.</span><span class="sxs-lookup"><span data-stu-id="15a76-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="15a76-147">-QueryPeriod</span></span>
<span data-ttu-id="15a76-148">Riasztási szabály lekérdezési időszaka.</span><span class="sxs-lookup"><span data-stu-id="15a76-148">Alert Rule Query Period.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a76-149">-ResourceGroupName</span></span>
<span data-ttu-id="15a76-150">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="15a76-150">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15a76-151">-ResourceId</span></span>
<span data-ttu-id="15a76-152">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="15a76-152">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-153">-SúlyosságSzűrő</span><span class="sxs-lookup"><span data-stu-id="15a76-153">-SeveritiesFilter</span></span>
<span data-ttu-id="15a76-154">Riasztási szabály súlyossági szűrője.</span><span class="sxs-lookup"><span data-stu-id="15a76-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-155">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="15a76-155">-Severity</span></span>
<span data-ttu-id="15a76-156">Incidens súlyossága.</span><span class="sxs-lookup"><span data-stu-id="15a76-156">Incident Severity.</span></span>

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

### <span data-ttu-id="15a76-157">–KéntelvezetőDisabled</span><span class="sxs-lookup"><span data-stu-id="15a76-157">-SuppressionDisabled</span></span>
<span data-ttu-id="15a76-158">Riasztási szabály letiltva.</span><span class="sxs-lookup"><span data-stu-id="15a76-158">Alert Rule Suppression Disabled.</span></span>

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

### <span data-ttu-id="15a76-159">–ADuration</span><span class="sxs-lookup"><span data-stu-id="15a76-159">-SuppressionDuration</span></span>
<span data-ttu-id="15a76-160">Riasztási szabály időtartamára vonatkozó riasztási szabály.</span><span class="sxs-lookup"><span data-stu-id="15a76-160">Alert Rule Suppression Duration.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-161">-A1111-2010-400</span><span class="sxs-lookup"><span data-stu-id="15a76-161">-SuppressionEnabled</span></span>
<span data-ttu-id="15a76-162">Riasztási szabály engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="15a76-162">Alert Rule Suppression Enabled.</span></span>

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

### <span data-ttu-id="15a76-163">– 2010.01.</span><span class="sxs-lookup"><span data-stu-id="15a76-163">-Tactics</span></span>
<span data-ttu-id="15a76-164">Riasztási szabály figyelősök.</span><span class="sxs-lookup"><span data-stu-id="15a76-164">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-165">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="15a76-165">-TriggerOperator</span></span>
<span data-ttu-id="15a76-166">Riasztási szabály eseményindítója.</span><span class="sxs-lookup"><span data-stu-id="15a76-166">Alert Rule Trigger Operator.</span></span>

```yaml
Type: TriggerOperator
Parameter Sets: (All)
Aliases:
Accepted values: GreaterThan, LessThan, Equal, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-167">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="15a76-167">-TriggerThreshold</span></span>
<span data-ttu-id="15a76-168">Riasztási szabály eseményindító küszöbértéke.</span><span class="sxs-lookup"><span data-stu-id="15a76-168">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-169">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="15a76-169">-WorkspaceName</span></span>
<span data-ttu-id="15a76-170">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="15a76-170">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a76-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15a76-171">-Confirm</span></span>
<span data-ttu-id="15a76-172">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="15a76-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15a76-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a76-173">-WhatIf</span></span>
<span data-ttu-id="15a76-174">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="15a76-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15a76-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15a76-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15a76-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a76-176">CommonParameters</span></span>
<span data-ttu-id="15a76-177">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a76-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a76-178">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15a76-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a76-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15a76-179">INPUTS</span></span>

### <span data-ttu-id="15a76-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="15a76-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

### <span data-ttu-id="15a76-181">System.String</span><span class="sxs-lookup"><span data-stu-id="15a76-181">System.String</span></span>

## <span data-ttu-id="15a76-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15a76-182">OUTPUTS</span></span>

### <span data-ttu-id="15a76-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="15a76-183">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>

## <span data-ttu-id="15a76-184">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="15a76-184">NOTES</span></span>

## <span data-ttu-id="15a76-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15a76-185">RELATED LINKS</span></span>
