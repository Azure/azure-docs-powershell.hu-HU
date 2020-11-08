---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: bc0f1a6aacc6188a982fe75fa021bdafdc4e02de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184447"
---
# <span data-ttu-id="2dd58-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="2dd58-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="2dd58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2dd58-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd58-103">Új műveletnapló-profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2dd58-103">Creates a new activity log profile.</span></span> <span data-ttu-id="2dd58-104">Ezzel a profillal a tevékenység naplóját Azure-tárterületre archiválhatja, vagy ugyanazon előfizetésben továbbíthatja egy Azure Event hub-ra.</span><span class="sxs-lookup"><span data-stu-id="2dd58-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="2dd58-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2dd58-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dd58-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="2dd58-106">DESCRIPTION</span></span>
<span data-ttu-id="2dd58-107">Az **Add-AzLogProfile** parancsmag naplózó profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2dd58-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="2dd58-108">**Storage Account** -only standard Storage Account (prémium tárterület-fiók nem támogatott) támogatott.</span><span class="sxs-lookup"><span data-stu-id="2dd58-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="2dd58-109">Lehet, hogy a kar vagy a klasszikus típus közül kell lennie.</span><span class="sxs-lookup"><span data-stu-id="2dd58-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="2dd58-110">Ha egy tárolási fiókba van bejelentkezve, a műveletnapló tárolási költségét a normál szokásos tárolási áron számlázzák.</span><span class="sxs-lookup"><span data-stu-id="2dd58-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="2dd58-111">Egy előfizetésben csak egy log-profil lehet, egy előfizetésben csak egy tárterület-fiók használható a műveletnapló exportálásához.</span><span class="sxs-lookup"><span data-stu-id="2dd58-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="2dd58-112">**Esemény-hub** : egy előfizetésben csak egy naplózási profil lehet, az előfizetéssel csak egy esemény-előfizetéssel exportálható a tevékenység naplója.</span><span class="sxs-lookup"><span data-stu-id="2dd58-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="2dd58-113">Ha a műveletnapló egy esemény központjának van továbbítva, a normál esemény hub árazása érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="2dd58-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="2dd58-114">A tevékenység naplóban az események egy régióra vonatkozhat vagy "globálisak" lehetnek.</span><span class="sxs-lookup"><span data-stu-id="2dd58-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="2dd58-115">Globális lényegében azt jelenti, hogy ezek az események a régió agnosztikusok és függetlenek a régiótól, az események többsége ebbe a kategóriába esik.</span><span class="sxs-lookup"><span data-stu-id="2dd58-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="2dd58-116">Ha a műveletnapló profilja a portálról van beállítva, implicit módon felveszi a "globális" kifejezést a felhasználói felületen kijelölt többi régióval együtt.</span><span class="sxs-lookup"><span data-stu-id="2dd58-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="2dd58-117">A parancsmag használatakor a "globális" helyet külön meg kell említeni a többi régióban kívül.</span><span class="sxs-lookup"><span data-stu-id="2dd58-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="2dd58-118">**Megjegyzés** : **a helyek "globális" beállításának hiánya következtében a tevékenység naplójának többsége nem fog exportálni.**</span><span class="sxs-lookup"><span data-stu-id="2dd58-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="2dd58-119">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="2dd58-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="2dd58-120">Példák</span><span class="sxs-lookup"><span data-stu-id="2dd58-120">EXAMPLES</span></span>

### <span data-ttu-id="2dd58-121">1. példa: új log-profil hozzáadása a tevékenység naplójának exportálásához, amely a hely feltételéhez illő tárolási fiókhoz van illesztve</span><span class="sxs-lookup"><span data-stu-id="2dd58-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="2dd58-122">2. példa</span><span class="sxs-lookup"><span data-stu-id="2dd58-122">Example 2</span></span>

<span data-ttu-id="2dd58-123">Új műveletnapló-profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2dd58-123">Creates a new activity log profile.</span></span> <span data-ttu-id="2dd58-124">autogenerated</span><span class="sxs-lookup"><span data-stu-id="2dd58-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="2dd58-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2dd58-125">PARAMETERS</span></span>

### <span data-ttu-id="2dd58-126">-Category (kategória)</span><span class="sxs-lookup"><span data-stu-id="2dd58-126">-Category</span></span>
<span data-ttu-id="2dd58-127">A kategóriák listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2dd58-127">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="2dd58-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dd58-128">-DefaultProfile</span></span>
<span data-ttu-id="2dd58-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2dd58-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2dd58-130">-Hely</span><span class="sxs-lookup"><span data-stu-id="2dd58-130">-Location</span></span>
<span data-ttu-id="2dd58-131">A napló profiljának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2dd58-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="2dd58-132">Érvényes értékek: az alábbi parancsmagot futtatva érheti el a helyek legújabb listáját.</span><span class="sxs-lookup"><span data-stu-id="2dd58-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="2dd58-133">Get-AzLocation | A DisplayName elem választása</span><span class="sxs-lookup"><span data-stu-id="2dd58-133">Get-AzLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd58-134">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2dd58-134">-Name</span></span>
<span data-ttu-id="2dd58-135">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2dd58-135">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="2dd58-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2dd58-136">-RetentionInDays</span></span>
<span data-ttu-id="2dd58-137">A napok szerinti adatmegőrzési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="2dd58-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="2dd58-138">Ez az a napok száma, amelyekben a naplók megmaradnak a megadott tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="2dd58-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="2dd58-139">Ha meg szeretné őrizni az adatvesztést, a **0** értékre kell állítania.</span><span class="sxs-lookup"><span data-stu-id="2dd58-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="2dd58-140">Ha nincs megadva, az alapértelmezett érték **0**.</span><span class="sxs-lookup"><span data-stu-id="2dd58-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="2dd58-141">A normál normál tárterület vagy az esemény-hub számlázási díja az adatmegőrzésre érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="2dd58-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="2dd58-142">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="2dd58-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="2dd58-143">A szolgáltatási busz szabályának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2dd58-143">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="2dd58-144">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2dd58-144">-StorageAccountId</span></span>
<span data-ttu-id="2dd58-145">A tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2dd58-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="2dd58-146">AZONOSÍTÓ: a tárolási fiók teljesen minősített erőforrás-azonosítója, például:</span><span class="sxs-lookup"><span data-stu-id="2dd58-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="2dd58-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="2dd58-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="2dd58-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2dd58-148">-Confirm</span></span>
<span data-ttu-id="2dd58-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2dd58-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dd58-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dd58-150">-WhatIf</span></span>
<span data-ttu-id="2dd58-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2dd58-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2dd58-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2dd58-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dd58-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd58-153">CommonParameters</span></span>
<span data-ttu-id="2dd58-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2dd58-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd58-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2dd58-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd58-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2dd58-156">INPUTS</span></span>

### <span data-ttu-id="2dd58-157">System. String</span><span class="sxs-lookup"><span data-stu-id="2dd58-157">System.String</span></span>

### <span data-ttu-id="2dd58-158">System. null ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2dd58-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2dd58-159">System. Collections. Generic. list ' 1 [[System. string, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2dd58-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2dd58-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2dd58-160">OUTPUTS</span></span>

### <span data-ttu-id="2dd58-161">Microsoft. Azure. commands. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="2dd58-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="2dd58-162">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2dd58-162">NOTES</span></span>

## <span data-ttu-id="2dd58-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2dd58-163">RELATED LINKS</span></span>

[<span data-ttu-id="2dd58-164">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="2dd58-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="2dd58-165">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="2dd58-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


