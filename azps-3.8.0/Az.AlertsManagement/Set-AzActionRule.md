---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/set-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Set-AzActionRule.md
ms.openlocfilehash: f2f8d4d17f9cce30f5101a5ae5a90c20c50e3f98
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011193"
---
# <span data-ttu-id="da74c-101">Set-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="da74c-101">Set-AzActionRule</span></span>

## <span data-ttu-id="da74c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="da74c-102">SYNOPSIS</span></span>
<span data-ttu-id="da74c-103">Műveleti szabály létrehozása vagy módosítása.</span><span class="sxs-lookup"><span data-stu-id="da74c-103">Create or update an action rule.</span></span>

## <span data-ttu-id="da74c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="da74c-104">SYNTAX</span></span>

### <span data-ttu-id="da74c-105">BySimplifiedFormatDiagnosticsActionRule (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="da74c-105">BySimplifiedFormatDiagnosticsActionRule (Default)</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da74c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="da74c-106">ByInputObject</span></span>
```
Set-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da74c-107">BySimplifiedFormatActionGroupActionRule</span><span class="sxs-lookup"><span data-stu-id="da74c-107">BySimplifiedFormatActionGroupActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ActionGroupId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da74c-108">BySimplifiedFormatSuppressionActionRule</span><span class="sxs-lookup"><span data-stu-id="da74c-108">BySimplifiedFormatSuppressionActionRule</span></span>
```
Set-AzActionRule -ResourceGroupName <String> -Name <String> [-Description <String>] -Status <String>
 -Scope <System.Collections.Generic.List`1[System.String]> [-SeverityCondition <String>]
 [-MonitorServiceCondition <String>] [-MonitorCondition <String>] [-TargetResourceTypeCondition <String>]
 [-AlertRuleIdCondition <String>] [-DescriptionCondition <String>] [-AlertContextCondition <String>]
 -ActionRuleType <String> -ReccurenceType <String> [-SuppressionStartTime <String>]
 [-SuppressionEndTime <String>] [-ReccurentValue <Int32[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da74c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="da74c-109">DESCRIPTION</span></span>
<span data-ttu-id="da74c-110">**Set-AzActionRule** létrehoz vagy frissít egy műveleti szabályt.</span><span class="sxs-lookup"><span data-stu-id="da74c-110">**Set-AzActionRule** creates or updates an action rule.</span></span>

## <span data-ttu-id="da74c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="da74c-111">EXAMPLES</span></span>

### <span data-ttu-id="da74c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="da74c-112">Example 1</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Suppression" -ReccurenceType "Weekly" -SuppressionStartTime "06/26/2018 06:00:00" -SuppressionEndTime "07/27/2018 06:00:00" -ReccurentValue 1,4,6
```

<span data-ttu-id="da74c-113">Ez a parancsmag műveleti szabályt hoz létre a lemondás számára.</span><span class="sxs-lookup"><span data-stu-id="da74c-113">This cmdlet creates an action rule for supression.</span></span>

### <span data-ttu-id="da74c-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="da74c-114">Example 2</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "ActionGroup" -ActionGroupId "/subscriptions/1e3ff1c0-771a-4119-a03b-be82a51e232d/resourceGroups/alertscorrelationrg/providers/Microsoft.insights/actiongroups/testAG"
```

<span data-ttu-id="da74c-115">Ez a parancsmag műveleti szabályt hoz létre a műveletek csoport számára.</span><span class="sxs-lookup"><span data-stu-id="da74c-115">This cmdlet creates an action rule for action group.</span></span>

### <span data-ttu-id="da74c-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="da74c-116">Example 3</span></span>
```powershell
PS C:\> Set-AzActionRule -ResourceGroupName "test-rg" -Name "Test-AR" -Scope "/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/alertslab","/subscriptions/dd91de05-d791-4ceb-b6dc-988682dc7d72/resourceGroups/Test-VMs" -SeverityCondition "Equals:Sev0,Sev1" -MonitorCondition "NotEquals:Resolved" -Description "Test description" -Status "Enabled" -ActionRuleType "Diagnostics"
```

<span data-ttu-id="da74c-117">Ez a parancsmag műveleti szabályt hoz létre a diagnosztika beállításaihoz.</span><span class="sxs-lookup"><span data-stu-id="da74c-117">This cmdlet creates an action rule for diagnostics settings.</span></span>

## <span data-ttu-id="da74c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="da74c-118">PARAMETERS</span></span>

### <span data-ttu-id="da74c-119">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="da74c-119">-ActionGroupId</span></span>
<span data-ttu-id="da74c-120">A műveleti csoport azonosítóját, amelyet értesíteni kell.</span><span class="sxs-lookup"><span data-stu-id="da74c-120">Action Group Id which is to be notified.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatActionGroupActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-121">-ActionRuleType</span><span class="sxs-lookup"><span data-stu-id="da74c-121">-ActionRuleType</span></span>
<span data-ttu-id="da74c-122">Műveleti szabály JSON formátum</span><span class="sxs-lookup"><span data-stu-id="da74c-122">Action rule Json format</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-123">-AlertContextCondition</span><span class="sxs-lookup"><span data-stu-id="da74c-123">-AlertContextCondition</span></span>
<span data-ttu-id="da74c-124">Várható formátum – { \< művelet \> : \< pontosvesszővel elválasztott lista, például értékek \> }.</span><span class="sxs-lookup"><span data-stu-id="da74c-124">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="da74c-125">Tartalma: smartgroups</span><span class="sxs-lookup"><span data-stu-id="da74c-125">Contains:smartgroups</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-126">-AlertRuleIdCondition</span><span class="sxs-lookup"><span data-stu-id="da74c-126">-AlertRuleIdCondition</span></span>
<span data-ttu-id="da74c-127">Várható formátum – { \< művelet \> : \< pontosvesszővel elválasztott lista, például értékek \> }.</span><span class="sxs-lookup"><span data-stu-id="da74c-127">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="da74c-128">Eredménye:/előfizetések/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/Providers/Microsoft. ininsights/metricAlerts/teszt-mrmc-VM-abvarma</span><span class="sxs-lookup"><span data-stu-id="da74c-128">Equals:/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourceGroups/abvarma/providers/microsoft.insights/metricAlerts/test-mrmc-vm-abvarma</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da74c-129">-DefaultProfile</span></span>
<span data-ttu-id="da74c-130">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="da74c-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da74c-131">-Leírás</span><span class="sxs-lookup"><span data-stu-id="da74c-131">-Description</span></span>
<span data-ttu-id="da74c-132">A műveleti szabály leírása</span><span class="sxs-lookup"><span data-stu-id="da74c-132">Description of Action Rule</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-133">-DescriptionCondition</span><span class="sxs-lookup"><span data-stu-id="da74c-133">-DescriptionCondition</span></span>
<span data-ttu-id="da74c-134">Várható formátum – { \< művelet \> : \< pontosvesszővel elválasztott lista, például értékek \> }.</span><span class="sxs-lookup"><span data-stu-id="da74c-134">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="da74c-135">Tartalma: teszt riasztás</span><span class="sxs-lookup"><span data-stu-id="da74c-135">Contains:Test Alert</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da74c-136">-InputObject</span></span>
<span data-ttu-id="da74c-137">A műveleti szabály erőforrás</span><span class="sxs-lookup"><span data-stu-id="da74c-137">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-138">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="da74c-138">-MonitorCondition</span></span>
<span data-ttu-id="da74c-139">Várható formátum – { \< művelet \> : \< pontosvesszővel elválasztott lista, például értékek \> }.</span><span class="sxs-lookup"><span data-stu-id="da74c-139">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="da74c-140">NotEquals: megoldva</span><span class="sxs-lookup"><span data-stu-id="da74c-140">NotEquals:Resolved</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-141">-MonitorServiceCondition</span><span class="sxs-lookup"><span data-stu-id="da74c-141">-MonitorServiceCondition</span></span>
<span data-ttu-id="da74c-142">Várható formátum – { \< művelet \> : \< pontosvesszővel elválasztott lista, például értékek \> }.</span><span class="sxs-lookup"><span data-stu-id="da74c-142">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="da74c-143">Egyenlő: platform, log Analytics</span><span class="sxs-lookup"><span data-stu-id="da74c-143">Equals:Platform,Log Analytics</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-144">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="da74c-144">-Name</span></span>
<span data-ttu-id="da74c-145">Műveleti szabály neve</span><span class="sxs-lookup"><span data-stu-id="da74c-145">Action rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-146">-ReccurenceType</span><span class="sxs-lookup"><span data-stu-id="da74c-146">-ReccurenceType</span></span>
<span data-ttu-id="da74c-147">Adja meg, hogy mennyi ideig legyen érvényes a Letiltás.</span><span class="sxs-lookup"><span data-stu-id="da74c-147">Specifies the duration when the suppression should be applied.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-148">-ReccurentValue</span><span class="sxs-lookup"><span data-stu-id="da74c-148">-ReccurentValue</span></span>
<span data-ttu-id="da74c-149">Reccurent-értékek (ha szükséges) Heti- \[ 1, 2, \] havonta- \[ 1, 3, 5, 30 esetén\]</span><span class="sxs-lookup"><span data-stu-id="da74c-149">Reccurent values, if applicable.In case of Weekly - \[1,2\] In case of Monthly - \[1,3,5,30\]</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da74c-150">-ResourceGroupName</span></span>
<span data-ttu-id="da74c-151">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="da74c-151">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-152">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="da74c-152">-Scope</span></span>
<span data-ttu-id="da74c-153">Vesszővel elválasztott értékek listája</span><span class="sxs-lookup"><span data-stu-id="da74c-153">Comma separated list of values</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-154">-SeverityCondition</span><span class="sxs-lookup"><span data-stu-id="da74c-154">-SeverityCondition</span></span>
<span data-ttu-id="da74c-155">Várható formátum – { \< művelet \> : \< pontosvesszővel elválasztott lista, például értékek \> }.</span><span class="sxs-lookup"><span data-stu-id="da74c-155">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="da74c-156">Egyenlő: Sev0, Sev1</span><span class="sxs-lookup"><span data-stu-id="da74c-156">Equals:Sev0,Sev1</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-157">-Állapot</span><span class="sxs-lookup"><span data-stu-id="da74c-157">-Status</span></span>
<span data-ttu-id="da74c-158">A műveleti szabály állapota</span><span class="sxs-lookup"><span data-stu-id="da74c-158">Status of Action Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-159">-SuppressionEndTime</span><span class="sxs-lookup"><span data-stu-id="da74c-159">-SuppressionEndTime</span></span>
<span data-ttu-id="da74c-160">Letiltási befejezési idő</span><span class="sxs-lookup"><span data-stu-id="da74c-160">Suppression End Time.</span></span>
<span data-ttu-id="da74c-161">A 12/09/2018 06:00:00 + formátumot csak egyszer, naponta, hetente vagy havonta kell megemlíteni a Reccurent elfogadási ütemezésekor.</span><span class="sxs-lookup"><span data-stu-id="da74c-161">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-162">-SuppressionStartTime</span><span class="sxs-lookup"><span data-stu-id="da74c-162">-SuppressionStartTime</span></span>
<span data-ttu-id="da74c-163">Elfojtás kezdési időpontja.</span><span class="sxs-lookup"><span data-stu-id="da74c-163">Suppression Start Time.</span></span>
<span data-ttu-id="da74c-164">A 12/09/2018 06:00:00 + formátumot csak egyszer, naponta, hetente vagy havonta kell megemlíteni a Reccurent elfogadási ütemezésekor.</span><span class="sxs-lookup"><span data-stu-id="da74c-164">Format 12/09/2018 06:00:00 +Should be mentioned in case of Reccurent Supression Schedule - Once, Daily, Weekly or Monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-165">-TargetResourceTypeCondition</span><span class="sxs-lookup"><span data-stu-id="da74c-165">-TargetResourceTypeCondition</span></span>
<span data-ttu-id="da74c-166">Várható formátum – { \< művelet \> : \< pontosvesszővel elválasztott lista, például értékek \> }.</span><span class="sxs-lookup"><span data-stu-id="da74c-166">Expected format - {\<operation\>:\<comma separated list of values\>} For eg.</span></span>
<span data-ttu-id="da74c-167">Tartalma: virtuális gépek, tárolási fiók</span><span class="sxs-lookup"><span data-stu-id="da74c-167">Contains:Virtual Machines,Storage Account</span></span>

```yaml
Type: System.String
Parameter Sets: BySimplifiedFormatDiagnosticsActionRule, BySimplifiedFormatActionGroupActionRule, BySimplifiedFormatSuppressionActionRule
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da74c-168">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="da74c-168">-Confirm</span></span>
<span data-ttu-id="da74c-169">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="da74c-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da74c-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da74c-170">-WhatIf</span></span>
<span data-ttu-id="da74c-171">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="da74c-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da74c-172">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="da74c-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da74c-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da74c-173">CommonParameters</span></span>
<span data-ttu-id="da74c-174">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="da74c-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da74c-175">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="da74c-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da74c-176">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="da74c-176">INPUTS</span></span>

### <span data-ttu-id="da74c-177">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="da74c-177">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="da74c-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="da74c-178">OUTPUTS</span></span>

### <span data-ttu-id="da74c-179">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="da74c-179">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="da74c-180">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="da74c-180">NOTES</span></span>

## <span data-ttu-id="da74c-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="da74c-181">RELATED LINKS</span></span>
