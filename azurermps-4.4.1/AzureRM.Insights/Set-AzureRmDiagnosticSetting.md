---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 36e523fbb224b77df205b8c7e7d736af0faa2962
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679077"
---
# <span data-ttu-id="2e356-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="2e356-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="2e356-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e356-102">SYNOPSIS</span></span>
<span data-ttu-id="2e356-103">Az erőforrás naplók és metrikák beállításainak beállítása.</span><span class="sxs-lookup"><span data-stu-id="2e356-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e356-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e356-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e356-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e356-105">DESCRIPTION</span></span>
<span data-ttu-id="2e356-106">A **set-AzureRmDiagnosticSetting** parancsmag engedélyezi vagy letiltja az adott erőforráshoz tartozó minden gabona-és naplózási kategóriát.</span><span class="sxs-lookup"><span data-stu-id="2e356-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="2e356-107">A naplókat és a metrikákat a program a megadott tárterület-fiókban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2e356-107">The logs and metrics are stored in the specified storage account.</span></span>

## <span data-ttu-id="2e356-108">Példák</span><span class="sxs-lookup"><span data-stu-id="2e356-108">EXAMPLES</span></span>

### <span data-ttu-id="2e356-109">1. példa: egy erőforrás összes metrikájának és naplójának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="2e356-109">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="2e356-110">Ez a parancs a Resource01 minden elérhető metrikáját és naplóját engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="2e356-110">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="2e356-111">2. példa: az összes metrikák és naplók letiltása</span><span class="sxs-lookup"><span data-stu-id="2e356-111">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="2e356-112">Ez a parancs letiltja az erőforrás-Resource01 elérhető összes metrikát és naplót.</span><span class="sxs-lookup"><span data-stu-id="2e356-112">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="2e356-113">3. példa: több kategória engedélyezése</span><span class="sxs-lookup"><span data-stu-id="2e356-113">Example 3: Enable multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
Enabled   : True
Timegrain : PT1M
Enabled   : True
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

<span data-ttu-id="2e356-114">Ez a parancs lehetővé teszi a Category1 és a Category2.</span><span class="sxs-lookup"><span data-stu-id="2e356-114">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="2e356-115">Az összes timegrains és egyéb kategória változatlan marad.</span><span class="sxs-lookup"><span data-stu-id="2e356-115">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="2e356-116">4. példa: időgabona és több kategória engedélyezése</span><span class="sxs-lookup"><span data-stu-id="2e356-116">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="2e356-117">Ez a parancs csak a Category1, az Category2 és a Time Grain PT1M teszi lehetővé.</span><span class="sxs-lookup"><span data-stu-id="2e356-117">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="2e356-118">Minden más időgabona és kategória sem változik.</span><span class="sxs-lookup"><span data-stu-id="2e356-118">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="2e356-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e356-119">PARAMETERS</span></span>

### <span data-ttu-id="2e356-120">-Kategóriák</span><span class="sxs-lookup"><span data-stu-id="2e356-120">-Categories</span></span>
<span data-ttu-id="2e356-121">Az engedélyezni vagy letiltani kívánt naplózási kategóriák listáját adja meg az *engedélyezett* érték szerint.</span><span class="sxs-lookup"><span data-stu-id="2e356-121">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="2e356-122">Ha nem ad meg egy kategóriát, az a parancs minden kategórián működik.</span><span class="sxs-lookup"><span data-stu-id="2e356-122">If you do not specify a category, this command operates on all categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e356-123">-Engedélyezve</span><span class="sxs-lookup"><span data-stu-id="2e356-123">-Enabled</span></span>
<span data-ttu-id="2e356-124">Azt jelzi, hogy engedélyezi-e a diagnosztika használatát.</span><span class="sxs-lookup"><span data-stu-id="2e356-124">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="2e356-125">Adja meg $True a diagnosztika engedélyezéséhez, vagy $False a diagnosztika letiltásához.</span><span class="sxs-lookup"><span data-stu-id="2e356-125">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e356-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e356-126">-ResourceId</span></span>
<span data-ttu-id="2e356-127">Az erőforrás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e356-127">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e356-128">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="2e356-128">-RetentionEnabled</span></span>
<span data-ttu-id="2e356-129">Azt jelzi, hogy engedélyezve van-e a diagnosztikai adatok megőrzése.</span><span class="sxs-lookup"><span data-stu-id="2e356-129">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e356-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2e356-130">-RetentionInDays</span></span>
<span data-ttu-id="2e356-131">A napok szerinti adatmegőrzési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="2e356-131">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e356-132">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="2e356-132">-ServiceBusRuleId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e356-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2e356-133">-StorageAccountId</span></span>
<span data-ttu-id="2e356-134">Annak a tárolási fióknak az AZONOSÍTÓját adja meg, amelybe az adatot menteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="2e356-134">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e356-135">-Timegrains</span><span class="sxs-lookup"><span data-stu-id="2e356-135">-Timegrains</span></span>
<span data-ttu-id="2e356-136">A metrikák engedélyezéséhez vagy letiltásához szükséges időmennyiséget adja meg az *engedélyezett* értéknek megfelelően.</span><span class="sxs-lookup"><span data-stu-id="2e356-136">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="2e356-137">Ha nem ad meg időgabonát, ez a parancs minden rendelkezésre álló időgabona esetén működik.</span><span class="sxs-lookup"><span data-stu-id="2e356-137">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e356-138">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="2e356-138">-WorkspaceId</span></span>
<span data-ttu-id="2e356-139">A munkaterület azonosítója</span><span class="sxs-lookup"><span data-stu-id="2e356-139">The Id of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e356-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e356-140">-DefaultProfile</span></span>
<span data-ttu-id="2e356-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e356-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e356-142">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="2e356-142">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="2e356-143">Az esemény-hub-szabály azonosítója</span><span class="sxs-lookup"><span data-stu-id="2e356-143">The event hub rule id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e356-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e356-144">CommonParameters</span></span>
<span data-ttu-id="2e356-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e356-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e356-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e356-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e356-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e356-147">INPUTS</span></span>

## <span data-ttu-id="2e356-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e356-148">OUTPUTS</span></span>

### <span data-ttu-id="2e356-149">Microsoft. Azure. commands. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="2e356-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="2e356-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e356-150">NOTES</span></span>

## <span data-ttu-id="2e356-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e356-151">RELATED LINKS</span></span>

[<span data-ttu-id="2e356-152">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="2e356-152">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


