---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRule.md
ms.openlocfilehash: 97a07b515cff6cfd8521033dbe7380eb2a7bc1d1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168994"
---
# <span data-ttu-id="859b4-101">New-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="859b4-101">New-AzSentinelAlertRule</span></span>

## <span data-ttu-id="859b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="859b4-102">SYNOPSIS</span></span>
<span data-ttu-id="859b4-103">Analytic (riasztási szabály) létrehozása</span><span class="sxs-lookup"><span data-stu-id="859b4-103">Create an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="859b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="859b4-104">SYNTAX</span></span>

### <span data-ttu-id="859b4-105">ScheduledAlertRule (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="859b4-105">ScheduledAlertRule (Default)</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Scheduled]
 [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled] -DisplayName <String>
 [-Description <String>] [-SuppressionDuration <TimeSpan>] [-SuppressionEnabled] -Query <String>
 -QueryFrequency <TimeSpan> -QueryPeriod <TimeSpan> -Severity <String>
 [-Tactics <System.Collections.Generic.IList`1[System.String]>] [-TriggerOperator <TriggerOperator>]
 -TriggerThreshold <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="859b4-106">2016.01.012.0</span><span class="sxs-lookup"><span data-stu-id="859b4-106">FusionAlertRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> [-Fusion] [-AlertRuleId <String>]
 -AlertRuleTemplateName <String> [-Enabled] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="859b4-107">MicrosoftSecurityIncidentCreationRule</span><span class="sxs-lookup"><span data-stu-id="859b4-107">MicrosoftSecurityIncidentCreationRule</span></span>
```
New-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-MicrosoftSecurityIncidentCreation] [-AlertRuleId <String>] [-AlertRuleTemplateName <String>] [-Enabled]
 -DisplayName <String> -ProductFilter <String> [-Description <String>]
 [-DisplayNamesExcludeFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DisplayNamesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-SeveritiesFilter <System.Collections.Generic.IList`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="859b4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="859b4-108">DESCRIPTION</span></span>
<span data-ttu-id="859b4-109">A **New-AzSentinelAlertRule** parancsmag létrehoz egy analytic (riasztási szabály) a megadott munkaterületen.</span><span class="sxs-lookup"><span data-stu-id="859b4-109">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="859b4-110">A létrehozni kívánt riasztási szabály  fajtáját meg kell adnia a három paraméter egyikeként *(Az ütemezés,* az Ütemezett vagy a *MicrosoftSecurityIncidentCreation* paraméter).</span><span class="sxs-lookup"><span data-stu-id="859b4-110">You must specify one of the three parameters, *Fusion*, *Scheduled* or *MicrosoftSecurityIncidentCreation*, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="859b4-111">Minden egyes fajtához különböző kötelező paramétereket kell megadni.</span><span class="sxs-lookup"><span data-stu-id="859b4-111">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="859b4-112">A Confirm *paraméter* és a Windows PowerShell$ConfirmPreference változó segítségével szabályozhatja, hogy a parancsmag megerősítést kér-e.</span><span class="sxs-lookup"><span data-stu-id="859b4-112">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="859b4-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="859b4-113">EXAMPLES</span></span>

### <span data-ttu-id="859b4-114">1. példa</span><span class="sxs-lookup"><span data-stu-id="859b4-114">Example 1</span></span>
```powershell
PS C:\>$AlertRuleTemplateName = "f71aba3d-28fb-450b-b192-4e76a83015c8"
PS C:\>$AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Fusion -Enabled -AlertRuleTemplateName $AlertRuleTemplateName
```

<span data-ttu-id="859b4-115">Ebben a példában létrehoz egy **AlertRule-et** a *Figyelő* típusúról az *Advanced Multistage* támadásészleléshez használható sablon alapján, majd azt egy $AlertRule változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="859b4-115">This example creates a **AlertRule** of the *Fusion* kind based on the Template for *Advanced Multistage Attack Detection*, and then stores it in the $AlertRule variable.</span></span>

### <span data-ttu-id="859b4-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="859b4-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplateName = "a2e0eb51-1f11-461a-999b-cd0ebe5c7a72"
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftSecurityIncidentCreation -Enabled -AlertRuleTemplateName $AlertRuleTemplateName -DisplayName "Create incidents based on Azure Security Center for IoT" -ProductFilter "Azure Security Center for IoT"
```

<span data-ttu-id="859b4-117">Ebben a példában létrehoz egy **AlertRule-t** a *MicrosoftSecurityIncidentCreation* típusúról az *Azure Security Center for IoT-riasztások* alapján létrehozott incidensek létrehozása sablon alapján, majd azt a $AlertRule tárolja.</span><span class="sxs-lookup"><span data-stu-id="859b4-117">This example creates a **AlertRule** of the *MicrosoftSecurityIncidentCreation* kind based on the template for *Create incidents based on Azure Security Center for IoT alerts*, and then stores it in the $AlertRule varaible.</span></span>

### <span data-ttu-id="859b4-118">2. példa</span><span class="sxs-lookup"><span data-stu-id="859b4-118">Example 2</span></span>
```powershell
PS C:\> $AlertRule = New-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Scheduled -Enabled -DisplayName "Powershell Exection Alert (Several Times per Hour)" -Severity Low -Query "SecurityEvent | where EventId == 4688" -QueryFrequency (New-TimeSpan -Hours 1) -QueryPeriod (New-TimeSpan -Hours 1) -TriggerThreshold 10
```

<span data-ttu-id="859b4-119">Ebben a példában létrehoz  egy Ütemezett típusú **DataConnectort,** majd azt egy másik $AlertRule tárolja.</span><span class="sxs-lookup"><span data-stu-id="859b4-119">This example creates a **DataConnector** of the *Scheduled* kind, and then stores it in the $AlertRule varaible.</span></span>

## <span data-ttu-id="859b4-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="859b4-120">PARAMETERS</span></span>

### <span data-ttu-id="859b4-121">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="859b4-121">-AlertRuleId</span></span>
<span data-ttu-id="859b4-122">Riasztási szabály azonosítója.</span><span class="sxs-lookup"><span data-stu-id="859b4-122">Alert Rule Id.</span></span>

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

### <span data-ttu-id="859b4-123">-AlertRuleTemplateName</span><span class="sxs-lookup"><span data-stu-id="859b4-123">-AlertRuleTemplateName</span></span>
<span data-ttu-id="859b4-124">Értesítési szabálysablon.</span><span class="sxs-lookup"><span data-stu-id="859b4-124">Alert Rule Template.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="859b4-125">-DefaultProfile</span></span>
<span data-ttu-id="859b4-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="859b4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="859b4-127">-Leírás</span><span class="sxs-lookup"><span data-stu-id="859b4-127">-Description</span></span>
<span data-ttu-id="859b4-128">Leírás.</span><span class="sxs-lookup"><span data-stu-id="859b4-128">Description.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="859b4-129">-DisplayName</span></span>
<span data-ttu-id="859b4-130">Értesítési szabály megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="859b4-130">Alert Rule Display Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule, MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-131">-DisplayNamesExcludeFilter</span><span class="sxs-lookup"><span data-stu-id="859b4-131">-DisplayNamesExcludeFilter</span></span>
<span data-ttu-id="859b4-132">Alert Rule Display Names Exclude Filter.</span><span class="sxs-lookup"><span data-stu-id="859b4-132">Alert Rule Display Names Exclude Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-133">-DisplayNamesFilter</span><span class="sxs-lookup"><span data-stu-id="859b4-133">-DisplayNamesFilter</span></span>
<span data-ttu-id="859b4-134">Riasztási szabály megjelenítendő nevek szűrője.</span><span class="sxs-lookup"><span data-stu-id="859b4-134">Alert Rule Display Names Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-135">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="859b4-135">-Enabled</span></span>
<span data-ttu-id="859b4-136">Értesítési szabály engedélyezve.</span><span class="sxs-lookup"><span data-stu-id="859b4-136">Alert Rule Enabled.</span></span>

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

### <span data-ttu-id="859b4-137">–1.</span><span class="sxs-lookup"><span data-stu-id="859b4-137">-Fusion</span></span>
<span data-ttu-id="859b4-138">Értesítési szabály fajtája.</span><span class="sxs-lookup"><span data-stu-id="859b4-138">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FusionAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-139">-MicrosoftSecurityIncidentCreation</span><span class="sxs-lookup"><span data-stu-id="859b4-139">-MicrosoftSecurityIncidentCreation</span></span>
<span data-ttu-id="859b4-140">Értesítési szabály fajtája.</span><span class="sxs-lookup"><span data-stu-id="859b4-140">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-141">-ProductFilter</span><span class="sxs-lookup"><span data-stu-id="859b4-141">-ProductFilter</span></span>
<span data-ttu-id="859b4-142">Értesítési szabály termékszűrője.</span><span class="sxs-lookup"><span data-stu-id="859b4-142">Alert Rule Product Filter.</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:
Accepted values: Azure Active Directory Identity Protection, Azure Advanced Threat Protection, Azure Security Center, Azure Security Center for IoT, Microsoft Cloud App Security, Microsoft Defender Advanced Threat Protection, Office 365 Advanced Threat Protection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-143">-Query</span><span class="sxs-lookup"><span data-stu-id="859b4-143">-Query</span></span>
<span data-ttu-id="859b4-144">Riasztási szabály lekérdezése.</span><span class="sxs-lookup"><span data-stu-id="859b4-144">Alert Rule Query.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-145">-QueryFrequency</span><span class="sxs-lookup"><span data-stu-id="859b4-145">-QueryFrequency</span></span>
<span data-ttu-id="859b4-146">Riasztási szabály lekérdezésének gyakorisága.</span><span class="sxs-lookup"><span data-stu-id="859b4-146">Alert Rule Query Frequency.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-147">-QueryPeriod</span><span class="sxs-lookup"><span data-stu-id="859b4-147">-QueryPeriod</span></span>
<span data-ttu-id="859b4-148">Riasztási szabály lekérdezési időszaka.</span><span class="sxs-lookup"><span data-stu-id="859b4-148">Alert Rule Query Period.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="859b4-149">-ResourceGroupName</span></span>
<span data-ttu-id="859b4-150">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="859b4-150">Resource group name.</span></span>

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

### <span data-ttu-id="859b4-151">-Scheduled</span><span class="sxs-lookup"><span data-stu-id="859b4-151">-Scheduled</span></span>
<span data-ttu-id="859b4-152">Értesítési szabály fajtája.</span><span class="sxs-lookup"><span data-stu-id="859b4-152">Alert Rule Kind.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-153">-SúlyosságSzűrő</span><span class="sxs-lookup"><span data-stu-id="859b4-153">-SeveritiesFilter</span></span>
<span data-ttu-id="859b4-154">Riasztási szabály súlyossági szűrője.</span><span class="sxs-lookup"><span data-stu-id="859b4-154">Alert Rule Severities Filter.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: MicrosoftSecurityIncidentCreationRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-155">-Súlyosság</span><span class="sxs-lookup"><span data-stu-id="859b4-155">-Severity</span></span>
<span data-ttu-id="859b4-156">Incidens súlyossága.</span><span class="sxs-lookup"><span data-stu-id="859b4-156">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-157">–ADuration</span><span class="sxs-lookup"><span data-stu-id="859b4-157">-SuppressionDuration</span></span>
<span data-ttu-id="859b4-158">Riasztási szabály időtartamára vonatkozó riasztási szabály.</span><span class="sxs-lookup"><span data-stu-id="859b4-158">Alert Rule Suppression Duration.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-159">-A1111-2010-400</span><span class="sxs-lookup"><span data-stu-id="859b4-159">-SuppressionEnabled</span></span>
<span data-ttu-id="859b4-160">Riasztási szabály engedélyezése.</span><span class="sxs-lookup"><span data-stu-id="859b4-160">Alert Rule Suppression Enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-161">– 2010.01.</span><span class="sxs-lookup"><span data-stu-id="859b4-161">-Tactics</span></span>
<span data-ttu-id="859b4-162">Riasztási szabályok figyelői.</span><span class="sxs-lookup"><span data-stu-id="859b4-162">Alert Rule Tactics.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[System.String]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-163">-TriggerOperator</span><span class="sxs-lookup"><span data-stu-id="859b4-163">-TriggerOperator</span></span>
<span data-ttu-id="859b4-164">Riasztási szabály eseményindítója.</span><span class="sxs-lookup"><span data-stu-id="859b4-164">Alert Rule Trigger Operator.</span></span>

```yaml
Type: Microsoft.Azure.Management.SecurityInsights.Models.TriggerOperator
Parameter Sets: ScheduledAlertRule
Aliases:
Accepted values: Equal, GreaterThan, LessThan, NotEqual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-165">-TriggerThreshold</span><span class="sxs-lookup"><span data-stu-id="859b4-165">-TriggerThreshold</span></span>
<span data-ttu-id="859b4-166">Riasztási szabály eseményindító küszöbértéke.</span><span class="sxs-lookup"><span data-stu-id="859b4-166">Alert Rule Trigger Threshold.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ScheduledAlertRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="859b4-167">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="859b4-167">-WorkspaceName</span></span>
<span data-ttu-id="859b4-168">Munkaterület neve.</span><span class="sxs-lookup"><span data-stu-id="859b4-168">Workspace Name.</span></span>

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

### <span data-ttu-id="859b4-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="859b4-169">-Confirm</span></span>
<span data-ttu-id="859b4-170">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="859b4-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="859b4-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="859b4-171">-WhatIf</span></span>
<span data-ttu-id="859b4-172">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="859b4-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="859b4-173">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="859b4-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="859b4-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="859b4-174">CommonParameters</span></span>
<span data-ttu-id="859b4-175">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="859b4-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="859b4-176">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="859b4-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="859b4-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="859b4-177">INPUTS</span></span>

### <span data-ttu-id="859b4-178">Nincs</span><span class="sxs-lookup"><span data-stu-id="859b4-178">None</span></span>
## <span data-ttu-id="859b4-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="859b4-179">OUTPUTS</span></span>

### <span data-ttu-id="859b4-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="859b4-180">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="859b4-181">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="859b4-181">NOTES</span></span>

## <span data-ttu-id="859b4-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="859b4-182">RELATED LINKS</span></span>
