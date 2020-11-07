---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: ee7d753ac81a55bf563742f87de7e195c89fb644
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680668"
---
# <span data-ttu-id="f23b7-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="f23b7-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="f23b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f23b7-102">SYNOPSIS</span></span>
<span data-ttu-id="f23b7-103">Az erőforrás naplók és metrikák beállításainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="f23b7-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f23b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f23b7-104">SYNTAX</span></span>

### <span data-ttu-id="f23b7-105">OldSetDiagnosticSetting (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f23b7-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f23b7-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="f23b7-106">NewSetDiagnosticSetting</span></span>
```
Set-AzureRmDiagnosticSetting -InputObject <PSServiceDiagnosticSettings>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f23b7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f23b7-107">DESCRIPTION</span></span>
<span data-ttu-id="f23b7-108">A **set-AzureRmDiagnosticSetting** parancsmag engedélyezi vagy letiltja az adott erőforráshoz tartozó minden gabona-és naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="f23b7-108">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="f23b7-109">A naplókat és a metrikákat a program a megadott tárterület-fiókban tárolja.</span><span class="sxs-lookup"><span data-stu-id="f23b7-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="f23b7-110">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="f23b7-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f23b7-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f23b7-111">EXAMPLES</span></span>

### <span data-ttu-id="f23b7-112">1. példa: egy erőforrás összes metrikájának és naplójának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="f23b7-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="f23b7-113">Ez a parancs a Resource01 minden elérhető metrikáját és naplóját engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="f23b7-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="f23b7-114">2. példa: az összes metrikák és naplók letiltása</span><span class="sxs-lookup"><span data-stu-id="f23b7-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="f23b7-115">Ez a parancs letiltja az erőforrás-Resource01 elérhető összes metrikát és naplót.</span><span class="sxs-lookup"><span data-stu-id="f23b7-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="f23b7-116">3. példa: több metrikák kategória engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="f23b7-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
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

<span data-ttu-id="f23b7-117">Ez a parancs engedélyezi a Category1 és a Category2 nevű metrikák cateories.</span><span class="sxs-lookup"><span data-stu-id="f23b7-117">This command enables the metrics cateories called Category1 and Category2.</span></span>
<span data-ttu-id="f23b7-118">A többi kategória változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="f23b7-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="f23b7-119">Példa 4: több naplózási kategória engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="f23b7-119">Example 4: Enable/disable multiple log categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
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

<span data-ttu-id="f23b7-120">Ez a parancs lehetővé teszi a Category1 és a Category2.</span><span class="sxs-lookup"><span data-stu-id="f23b7-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="f23b7-121">A többi mérőszám és naplók kategória változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="f23b7-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="f23b7-122">4. példa: időgabona és több kategória engedélyezése</span><span class="sxs-lookup"><span data-stu-id="f23b7-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="f23b7-123">Ez a parancs csak a Category1, az Category2 és a Time Grain PT1M teszi lehetővé.</span><span class="sxs-lookup"><span data-stu-id="f23b7-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="f23b7-124">Minden más időgabona és kategória sem változik.</span><span class="sxs-lookup"><span data-stu-id="f23b7-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="f23b7-125">Példa 5: csővezeték használata</span><span class="sxs-lookup"><span data-stu-id="f23b7-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "Resource01" | Set-AzureRmDiagnosticSetting
```

<span data-ttu-id="f23b7-126">Ez a parancs a PowerShell-futószalagot használja a diagnosztikai beállítások megadásához (ez nem változik).</span><span class="sxs-lookup"><span data-stu-id="f23b7-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="f23b7-127">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f23b7-127">PARAMETERS</span></span>

### <span data-ttu-id="f23b7-128">-Kategóriák</span><span class="sxs-lookup"><span data-stu-id="f23b7-128">-Categories</span></span>
<span data-ttu-id="f23b7-129">Az engedélyezni vagy letiltani kívánt naplózási kategóriák listáját adja meg az *engedélyezett* érték szerint.</span><span class="sxs-lookup"><span data-stu-id="f23b7-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="f23b7-130">Ha nincs megadva kategória, ez a parancs minden támogatott kategórián működik.</span><span class="sxs-lookup"><span data-stu-id="f23b7-130">If no category is specified, this command operates on all supported categories.</span></span> 

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases: Category

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f23b7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f23b7-131">-DefaultProfile</span></span>
<span data-ttu-id="f23b7-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f23b7-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f23b7-133">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="f23b7-133">-Enabled</span></span>
<span data-ttu-id="f23b7-134">Azt jelzi, hogy engedélyezi-e a diagnosztika használatát.</span><span class="sxs-lookup"><span data-stu-id="f23b7-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="f23b7-135">Adja meg $True a diagnosztika engedélyezéséhez, vagy $False a diagnosztika letiltásához.</span><span class="sxs-lookup"><span data-stu-id="f23b7-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="f23b7-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="f23b7-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="f23b7-137">Az esemény központi engedélyezési szabály azonosítója</span><span class="sxs-lookup"><span data-stu-id="f23b7-137">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="f23b7-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="f23b7-138">-EventHubName</span></span>
<span data-ttu-id="f23b7-139">Az esemény központi neve</span><span class="sxs-lookup"><span data-stu-id="f23b7-139">The event hub name</span></span>

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

### <span data-ttu-id="f23b7-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f23b7-140">-InputObject</span></span>
<span data-ttu-id="f23b7-141">A bemeneti objektum (a csővezetékről lehetséges) Ekkor a program Kinyeri a nevet és a resourceId az objektumból.</span><span class="sxs-lookup"><span data-stu-id="f23b7-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="f23b7-142">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="f23b7-142">-MetricCategory</span></span>
<span data-ttu-id="f23b7-143">A metrikus kategóriák listája.</span><span class="sxs-lookup"><span data-stu-id="f23b7-143">The list of metric categories.</span></span> <span data-ttu-id="f23b7-144">Ha nincs megadva kategória, ez a parancs minden támogatott kategórián működik.</span><span class="sxs-lookup"><span data-stu-id="f23b7-144">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="f23b7-145">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f23b7-145">-Name</span></span>
<span data-ttu-id="f23b7-146">A diagnosztikai beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="f23b7-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="f23b7-147">Az alapértelmezett érték a **szolgáltatás**.</span><span class="sxs-lookup"><span data-stu-id="f23b7-147">The default value is **service**.</span></span>

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

### <span data-ttu-id="f23b7-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f23b7-148">-ResourceId</span></span>
<span data-ttu-id="f23b7-149">Az erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f23b7-149">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="f23b7-150">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="f23b7-150">-RetentionEnabled</span></span>
<span data-ttu-id="f23b7-151">Azt jelzi, hogy engedélyezve van-e a diagnosztikai adatok megőrzése.</span><span class="sxs-lookup"><span data-stu-id="f23b7-151">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="f23b7-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f23b7-152">-RetentionInDays</span></span>
<span data-ttu-id="f23b7-153">A napok szerinti adatmegőrzési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="f23b7-153">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="f23b7-154">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="f23b7-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="f23b7-155">A Service Bus szabály azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f23b7-155">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="f23b7-156">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f23b7-156">-StorageAccountId</span></span>
<span data-ttu-id="f23b7-157">Annak a tárolási fióknak az AZONOSÍTÓját adja meg, amelybe az adatot menteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="f23b7-157">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="f23b7-158">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="f23b7-158">-Timegrains</span></span>
<span data-ttu-id="f23b7-159">A metrikák engedélyezéséhez vagy letiltásához szükséges időmennyiséget adja meg az *engedélyezett* értéknek megfelelően.</span><span class="sxs-lookup"><span data-stu-id="f23b7-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="f23b7-160">Ha nem ad meg időgabonát, ez a parancs minden rendelkezésre álló időgabona esetén működik.</span><span class="sxs-lookup"><span data-stu-id="f23b7-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases: Timegrain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f23b7-161">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="f23b7-161">-WorkspaceId</span></span>
<span data-ttu-id="f23b7-162">A munkaterület azonosítója</span><span class="sxs-lookup"><span data-stu-id="f23b7-162">The Id of the workspace</span></span>

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

### <span data-ttu-id="f23b7-163">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f23b7-163">-Confirm</span></span>
<span data-ttu-id="f23b7-164">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f23b7-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f23b7-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f23b7-165">-WhatIf</span></span>
<span data-ttu-id="f23b7-166">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f23b7-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f23b7-167">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f23b7-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f23b7-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23b7-168">CommonParameters</span></span>
<span data-ttu-id="f23b7-169">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f23b7-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23b7-170">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f23b7-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23b7-171">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f23b7-171">INPUTS</span></span>

### <span data-ttu-id="f23b7-172">Microsoft. Azure. commands. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="f23b7-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>
<span data-ttu-id="f23b7-173">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f23b7-173">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f23b7-174">System. String</span><span class="sxs-lookup"><span data-stu-id="f23b7-174">System.String</span></span>

### <span data-ttu-id="f23b7-175">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f23b7-175">System.Boolean</span></span>

### <span data-ttu-id="f23b7-176">System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f23b7-176">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f23b7-177">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f23b7-177">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f23b7-178">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f23b7-178">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f23b7-179">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f23b7-179">OUTPUTS</span></span>

### <span data-ttu-id="f23b7-180">Microsoft. Azure. commands. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="f23b7-180">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="f23b7-181">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f23b7-181">NOTES</span></span>

## <span data-ttu-id="f23b7-182">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f23b7-182">RELATED LINKS</span></span>

<span data-ttu-id="f23b7-183">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md) 
 [Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="f23b7-183">[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)
[Remove-AzureRmDiagnosticSetting](./Remove-AzureRmDiagnosticSetting.md)</span></span>
