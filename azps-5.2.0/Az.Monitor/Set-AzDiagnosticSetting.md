---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: eeadf64c83f62a8d245a7ace8f750b34ddc230ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361981"
---
# <span data-ttu-id="8ec6c-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8ec6c-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="8ec6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ec6c-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec6c-103">Beállítja az erőforrás naplói és metrikák beállításait.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="8ec6c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8ec6c-104">SYNTAX</span></span>

### <span data-ttu-id="8ec6c-105">OldSetDiagnosticSetting (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8ec6c-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-ExportToResourceSpecific] [-EnableLog <Boolean>]
 [-EnableMetrics <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ec6c-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="8ec6c-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ec6c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8ec6c-107">DESCRIPTION</span></span>
<span data-ttu-id="8ec6c-108">A **Set-AzDiagnosticSetting** parancsmag engedélyezi vagy letiltja az adott erőforrás minden egyes szemcsés és naplókategóriáját.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="8ec6c-109">A naplókat és a metrikákat a megadott tárfiók tárolja.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="8ec6c-110">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen létrehozza, módosítja vagy eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="8ec6c-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8ec6c-111">EXAMPLES</span></span>

### <span data-ttu-id="8ec6c-112">1. példa: Az erőforráshoz szükséges összes mérőszám és napló engedélyezése</span><span class="sxs-lookup"><span data-stu-id="8ec6c-112">Example 1: Enable all metrics and logs for a resource</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="8ec6c-113">Ez a parancs engedélyezi az Összes elérhető metrikát és naplót az Resource01-hez.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="8ec6c-114">2. példa: Az összes mérőszám és napló letiltása</span><span class="sxs-lookup"><span data-stu-id="8ec6c-114">Example 2: Disable all metrics and logs</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="8ec6c-115">Ez a parancs letiltja az erőforrás Erőforrás01 erőforrás összes rendelkezésre álló mérőszámát és naplóját.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="8ec6c-116">3. példa: Több metrikakategória engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="8ec6c-116">Example 3: Enable/disable multiple metrics categories</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="8ec6c-117">Ez a parancs letiltja a Kategória1 és a Kategória2 nevű metrikák kategóriáit.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="8ec6c-118">Az összes többi kategória változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="8ec6c-119">4. példa: Több naplókategória engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="8ec6c-119">Example 4: Enable/disable multiple log categories</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="8ec6c-120">Ez a parancs engedélyezi a Kategória1 és a Kategória2 kategóriát.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="8ec6c-121">Az összes többi metrika és naplókategória változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="8ec6c-122">5. példa: Időszemét és több kategória engedélyezése</span><span class="sxs-lookup"><span data-stu-id="8ec6c-122">Example 5: Enable a time grain and multiple categories</span></span>
```powershell
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="8ec6c-123">Ez a parancs csak Kategória1, Kategória2 és idő grain PT1M-et tesz lehetővé.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="8ec6c-124">Minden más idő és kategória változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="8ec6c-125">6. példa: Folyamat használata</span><span class="sxs-lookup"><span data-stu-id="8ec6c-125">Example 6: Using pipeline</span></span>
```powershell
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting -Enabled $True -Category Category1,Category2
```

<span data-ttu-id="8ec6c-126">Ez a parancs a PowerShell-folyamat segítségével beállít egy diagnosztikai beállítást (módosítás nélkül).</span><span class="sxs-lookup"><span data-stu-id="8ec6c-126">This command uses the PowerShell pipeline to set (no change made) a diagnostic setting.</span></span>

## <span data-ttu-id="8ec6c-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ec6c-127">PARAMETERS</span></span>

### <span data-ttu-id="8ec6c-128">-Category</span><span class="sxs-lookup"><span data-stu-id="8ec6c-128">-Category</span></span>
<span data-ttu-id="8ec6c-129">Az engedélyezett vagy letiltható naplókategóriák listája az Engedélyezett *értéknek megfelelően.*</span><span class="sxs-lookup"><span data-stu-id="8ec6c-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="8ec6c-130">Ha nincs megadva kategória, ez a parancs az összes támogatott kategórián működik.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-130">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec6c-131">-DefaultProfile</span></span>
<span data-ttu-id="8ec6c-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8ec6c-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ec6c-133">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="8ec6c-133">-Enabled</span></span>
<span data-ttu-id="8ec6c-134">Azt jelzi, hogy engedélyezni kell-e a diagnosztika funkcióját.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="8ec6c-135">Adja $True a diagnosztika engedélyezéséhez szükséges beállításokat, $False a diagnosztika letiltásához szükséges beállításokat.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-136">-EnableLog</span><span class="sxs-lookup"><span data-stu-id="8ec6c-136">-EnableLog</span></span>
<span data-ttu-id="8ec6c-137">Az az érték, amely azt jelzi, hogy a diagnosztikai naplókat engedélyezni vagy letiltani kell-e</span><span class="sxs-lookup"><span data-stu-id="8ec6c-137">The value indicating whether the diagnostic logs should be enabled or disabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-138">-EnableMetrics</span><span class="sxs-lookup"><span data-stu-id="8ec6c-138">-EnableMetrics</span></span>
<span data-ttu-id="8ec6c-139">Az az érték, amely azt jelzi, hogy a diagnosztikai metrikákat engedélyezni vagy letiltani kell-e</span><span class="sxs-lookup"><span data-stu-id="8ec6c-139">The value indicating whether the diagnostic metrics should be enabled or disabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-140">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="8ec6c-140">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="8ec6c-141">Az eseményközpont engedélyezési szabályazonosítója</span><span class="sxs-lookup"><span data-stu-id="8ec6c-141">The event hub authorization rule id</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-142">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="8ec6c-142">-EventHubName</span></span>
<span data-ttu-id="8ec6c-143">Az eseményközpont neve</span><span class="sxs-lookup"><span data-stu-id="8ec6c-143">The event hub name</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-144">-ExportToResourceSpecific</span><span class="sxs-lookup"><span data-stu-id="8ec6c-144">-ExportToResourceSpecific</span></span>
<span data-ttu-id="8ec6c-145">Flag indicating that the export to LA must be done to a resource specific table, a.k.a.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-145">Flag indicating that the export to LA must be done to a resource specific table, a.k.a.</span></span> <span data-ttu-id="8ec6c-146">dedikált vagy rögzített sématáblát,  szemben az **AzureDiagnostics** nevű alapértelmezett dinamikus sématáblával.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-146">dedicated or fixed schema table, as opposed to the **default** dynamic schema table called **AzureDiagnostics**.</span></span>

<span data-ttu-id="8ec6c-147">Ez az argumentum csak akkor hatékony, ha az **argumentum -workspaceId** is meg van adva.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-147">This argument is effective only when the argument **-workspaceId** is also given.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ec6c-148">-InputObject</span></span>
<span data-ttu-id="8ec6c-149">A bemeneti objektum (a folyamatból lehetséges).) A név és az erőforrásazonosító ki lesz bontva ebből az objektumból.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-149">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings
Parameter Sets: NewSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-150">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="8ec6c-150">-MetricCategory</span></span>
<span data-ttu-id="8ec6c-151">A metrikus kategóriák listája.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-151">The list of metric categories.</span></span> <span data-ttu-id="8ec6c-152">Ha nincs megadva kategória, ez a parancs az összes támogatott kategórián működik.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-152">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-153">-Name</span><span class="sxs-lookup"><span data-stu-id="8ec6c-153">-Name</span></span>
<span data-ttu-id="8ec6c-154">A diagnosztikai beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-154">The name of the diagnostic setting.</span></span> <span data-ttu-id="8ec6c-155">Az alapértelmezett érték a **szolgáltatás.**</span><span class="sxs-lookup"><span data-stu-id="8ec6c-155">The default value is **service**.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-156">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ec6c-156">-ResourceId</span></span>
<span data-ttu-id="8ec6c-157">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-157">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-158">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="8ec6c-158">-RetentionEnabled</span></span>
<span data-ttu-id="8ec6c-159">Azt jelzi, hogy engedélyezve van-e a diagnosztikai adatok megőrzése.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-159">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-160">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8ec6c-160">-RetentionInDays</span></span>
<span data-ttu-id="8ec6c-161">Az adatmegőrzési házirendet napokban adja meg.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-161">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-162">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="8ec6c-162">-ServiceBusRuleId</span></span>
<span data-ttu-id="8ec6c-163">A szolgáltatásbusz szabályazonosítója.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-163">The Service Bus Rule id.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-164">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8ec6c-164">-StorageAccountId</span></span>
<span data-ttu-id="8ec6c-165">Annak a tárfióknak az azonosítója, amelybe menteni kell az adatokat.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-165">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-166">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="8ec6c-166">-Timegrain</span></span>
<span data-ttu-id="8ec6c-167">A metrikák engedélyezéséhez vagy letiltásához szükséges időkorrekta az *Engedélyezett értéknek megfelelően.*</span><span class="sxs-lookup"><span data-stu-id="8ec6c-167">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="8ec6c-168">Ha nem ad meg időszemetet, ez a parancs az összes rendelkezésre álló időszeméten működik.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-168">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-169">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="8ec6c-169">-WorkspaceId</span></span>
<span data-ttu-id="8ec6c-170">A Naplóelemzés munkaterület erőforrás-azonosítója, amelybe naplókat/metrikákat kell küldeni</span><span class="sxs-lookup"><span data-stu-id="8ec6c-170">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ec6c-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ec6c-171">-Confirm</span></span>
<span data-ttu-id="8ec6c-172">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ec6c-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ec6c-173">-WhatIf</span></span>
<span data-ttu-id="8ec6c-174">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ec6c-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ec6c-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec6c-176">CommonParameters</span></span>
<span data-ttu-id="8ec6c-177">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ec6c-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec6c-178">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ec6c-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec6c-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ec6c-179">INPUTS</span></span>

### <span data-ttu-id="8ec6c-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="8ec6c-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="8ec6c-181">System.String</span><span class="sxs-lookup"><span data-stu-id="8ec6c-181">System.String</span></span>

### <span data-ttu-id="8ec6c-182">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8ec6c-182">System.Boolean</span></span>

### <span data-ttu-id="8ec6c-183">System.Collections.Generic.List'1[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8ec6c-183">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8ec6c-184">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8ec6c-184">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8ec6c-185">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8ec6c-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8ec6c-186">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8ec6c-186">OUTPUTS</span></span>

### <span data-ttu-id="8ec6c-187">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="8ec6c-187">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="8ec6c-188">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8ec6c-188">NOTES</span></span>

## <span data-ttu-id="8ec6c-189">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8ec6c-189">RELATED LINKS</span></span>

<span data-ttu-id="8ec6c-190">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="8ec6c-190">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
