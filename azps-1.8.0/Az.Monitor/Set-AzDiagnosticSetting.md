---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: 6f78e11fc6a5ef5cca2148258db9effd044b8c25
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402813"
---
# <span data-ttu-id="77250-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="77250-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="77250-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77250-102">SYNOPSIS</span></span>
<span data-ttu-id="77250-103">Beállítja az erőforrás napló- és metrikákra vonatkozó beállításait.</span><span class="sxs-lookup"><span data-stu-id="77250-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="77250-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="77250-104">SYNTAX</span></span>

### <span data-ttu-id="77250-105">OldSetDiagnosticSetting (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="77250-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77250-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="77250-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77250-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="77250-107">DESCRIPTION</span></span>
<span data-ttu-id="77250-108">A **Set-AzDiagnosticSetting** parancsmag engedélyezi vagy letiltja az adott erőforrás minden egyes szemcsés és naplókategóriáját.</span><span class="sxs-lookup"><span data-stu-id="77250-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="77250-109">A naplókat és a metrikákat a megadott tárfiók tárolja.</span><span class="sxs-lookup"><span data-stu-id="77250-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="77250-110">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen létrehozza, módosítja vagy eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="77250-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="77250-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="77250-111">EXAMPLES</span></span>

### <span data-ttu-id="77250-112">1. példa: Az erőforráshoz szükséges összes mérőszám és napló engedélyezése</span><span class="sxs-lookup"><span data-stu-id="77250-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="77250-113">Ez a parancs engedélyezi az Összes elérhető metrikát és naplót az Resource01-hez.</span><span class="sxs-lookup"><span data-stu-id="77250-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="77250-114">2. példa: Az összes mérőszám és napló letiltása</span><span class="sxs-lookup"><span data-stu-id="77250-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="77250-115">Ez a parancs letiltja az erőforrás Erőforrás01 erőforrás összes rendelkezésre álló mérőszámát és naplóját.</span><span class="sxs-lookup"><span data-stu-id="77250-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="77250-116">3. példa: Több metrikakategória engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="77250-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
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

<span data-ttu-id="77250-117">Ez a parancs letiltja a Kategória1 és a Kategória2 nevű metrikakategóriákat.</span><span class="sxs-lookup"><span data-stu-id="77250-117">This command disables the metrics cateories called Category1 and Category2.</span></span>
<span data-ttu-id="77250-118">Az összes többi kategória változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="77250-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="77250-119">4. példa: Több naplókategória engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="77250-119">Example 4: Enable/disable multiple log categories</span></span>
```
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

<span data-ttu-id="77250-120">Ez a parancs engedélyezi a Kategória1 és a Kategória2 kategóriát.</span><span class="sxs-lookup"><span data-stu-id="77250-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="77250-121">Az összes többi metrika és naplókategória változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="77250-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="77250-122">4. példa: Időszemét és több kategória engedélyezése</span><span class="sxs-lookup"><span data-stu-id="77250-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="77250-123">Ez a parancs csak Kategória1, Kategória2 és idő grain PT1M-et tesz lehetővé.</span><span class="sxs-lookup"><span data-stu-id="77250-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="77250-124">Minden más idő és kategória változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="77250-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="77250-125">5. példa: Folyamat használata</span><span class="sxs-lookup"><span data-stu-id="77250-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting
```

<span data-ttu-id="77250-126">Ez a parancs a PowerShell-folyamat segítségével beállít egy diagnosztikai beállítást (nem módosítja).</span><span class="sxs-lookup"><span data-stu-id="77250-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="77250-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77250-127">PARAMETERS</span></span>

### <span data-ttu-id="77250-128">-Category</span><span class="sxs-lookup"><span data-stu-id="77250-128">-Category</span></span>
<span data-ttu-id="77250-129">Az engedélyezett vagy letiltható naplókategóriák listája az Engedélyezett *értéknek megfelelően.*</span><span class="sxs-lookup"><span data-stu-id="77250-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="77250-130">Ha nincs megadva kategória, ez a parancs az összes támogatott kategórián működik.</span><span class="sxs-lookup"><span data-stu-id="77250-130">If no category is specified, this command operates on all supported categories.</span></span>

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

### <span data-ttu-id="77250-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77250-131">-DefaultProfile</span></span>
<span data-ttu-id="77250-132">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="77250-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77250-133">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="77250-133">-Enabled</span></span>
<span data-ttu-id="77250-134">Azt jelzi, hogy engedélyezni kell-e a diagnosztika funkcióját.</span><span class="sxs-lookup"><span data-stu-id="77250-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="77250-135">Adja $True a diagnosztika engedélyezéséhez szükséges beállításokat, $False a diagnosztika letiltásához szükséges beállításokat.</span><span class="sxs-lookup"><span data-stu-id="77250-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="77250-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="77250-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="77250-137">Az eseményközpont engedélyezési szabályazonosítója</span><span class="sxs-lookup"><span data-stu-id="77250-137">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="77250-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="77250-138">-EventHubName</span></span>
<span data-ttu-id="77250-139">Az eseményközpont neve</span><span class="sxs-lookup"><span data-stu-id="77250-139">The event hub name</span></span>

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

### <span data-ttu-id="77250-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77250-140">-InputObject</span></span>
<span data-ttu-id="77250-141">A bemeneti objektum (a folyamatból lehetséges).) A név és az erőforrásazonosító ki lesz bontva ebből az objektumból.</span><span class="sxs-lookup"><span data-stu-id="77250-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="77250-142">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="77250-142">-MetricCategory</span></span>
<span data-ttu-id="77250-143">A metrikus kategóriák listája.</span><span class="sxs-lookup"><span data-stu-id="77250-143">The list of metric categories.</span></span>
<span data-ttu-id="77250-144">Ha nincs megadva kategória, ez a parancs az összes támogatott kategórián működik.</span><span class="sxs-lookup"><span data-stu-id="77250-144">If no category is specified, this command operates on all supported categories.</span></span>

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

### <span data-ttu-id="77250-145">-Name</span><span class="sxs-lookup"><span data-stu-id="77250-145">-Name</span></span>
<span data-ttu-id="77250-146">A diagnosztikai beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="77250-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="77250-147">Az alapértelmezett érték a **szolgáltatás.**</span><span class="sxs-lookup"><span data-stu-id="77250-147">The default value is **service**.</span></span>

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

### <span data-ttu-id="77250-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77250-148">-ResourceId</span></span>
<span data-ttu-id="77250-149">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="77250-149">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="77250-150">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="77250-150">-RetentionEnabled</span></span>
<span data-ttu-id="77250-151">Azt jelzi, hogy engedélyezve van-e a diagnosztikai adatok megőrzése.</span><span class="sxs-lookup"><span data-stu-id="77250-151">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="77250-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="77250-152">-RetentionInDays</span></span>
<span data-ttu-id="77250-153">Az adatmegőrzési házirendet napokban adja meg.</span><span class="sxs-lookup"><span data-stu-id="77250-153">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="77250-154">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="77250-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="77250-155">A szolgáltatásbusz szabályazonosítója.</span><span class="sxs-lookup"><span data-stu-id="77250-155">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="77250-156">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="77250-156">-StorageAccountId</span></span>
<span data-ttu-id="77250-157">Annak a tárfióknak az azonosítója, amelybe menteni kell az adatokat.</span><span class="sxs-lookup"><span data-stu-id="77250-157">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="77250-158">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="77250-158">-Timegrain</span></span>
<span data-ttu-id="77250-159">A metrikák engedélyezéséhez vagy letiltásához szükséges időkorrekta az *Engedélyezett értéknek megfelelően.*</span><span class="sxs-lookup"><span data-stu-id="77250-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="77250-160">Ha nem ad meg időszemetet, ez a parancs az összes rendelkezésre álló időszeméten működik.</span><span class="sxs-lookup"><span data-stu-id="77250-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="77250-161">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="77250-161">-WorkspaceId</span></span>
<span data-ttu-id="77250-162">A Naplóelemzés munkaterület erőforrás-azonosítója, amelybe naplókat/metrikákat kell küldeni</span><span class="sxs-lookup"><span data-stu-id="77250-162">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

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

### <span data-ttu-id="77250-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77250-163">-Confirm</span></span>
<span data-ttu-id="77250-164">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="77250-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77250-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77250-165">-WhatIf</span></span>
<span data-ttu-id="77250-166">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="77250-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77250-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="77250-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77250-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77250-168">CommonParameters</span></span>
<span data-ttu-id="77250-169">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77250-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77250-170">További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77250-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77250-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77250-171">INPUTS</span></span>

### <span data-ttu-id="77250-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="77250-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="77250-173">System.String</span><span class="sxs-lookup"><span data-stu-id="77250-173">System.String</span></span>

### <span data-ttu-id="77250-174">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="77250-174">System.Boolean</span></span>

### <span data-ttu-id="77250-175">System.Collections.Generic.List'1[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="77250-175">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="77250-176">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="77250-176">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="77250-177">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="77250-177">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="77250-178">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="77250-178">OUTPUTS</span></span>

### <span data-ttu-id="77250-179">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="77250-179">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="77250-180">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="77250-180">NOTES</span></span>

## <span data-ttu-id="77250-181">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="77250-181">RELATED LINKS</span></span>

<span data-ttu-id="77250-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="77250-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
