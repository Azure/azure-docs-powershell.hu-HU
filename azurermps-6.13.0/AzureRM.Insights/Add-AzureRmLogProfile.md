---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 7e746e7d67672a57e3e8aa257a4e3dfbe3b51054
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672483"
---
# <span data-ttu-id="45b0c-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="45b0c-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="45b0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="45b0c-102">SYNOPSIS</span></span>
<span data-ttu-id="45b0c-103">Új műveletnapló-profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="45b0c-103">Creates a new activity log profile.</span></span> <span data-ttu-id="45b0c-104">Ezzel a profillal a tevékenység naplóját Azure-tárterületre archiválhatja, vagy ugyanazon előfizetésben továbbíthatja egy Azure Event hub-ra.</span><span class="sxs-lookup"><span data-stu-id="45b0c-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45b0c-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="45b0c-105">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45b0c-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="45b0c-106">DESCRIPTION</span></span>
<span data-ttu-id="45b0c-107">Az **Add-AzureRmLogProfile** parancsmag naplózó profilt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="45b0c-107">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="45b0c-108">**Storage Account** -only standard Storage Account (prémium tárterület-fiók nem támogatott) támogatott.</span><span class="sxs-lookup"><span data-stu-id="45b0c-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="45b0c-109">Lehet, hogy a kar vagy a klasszikus típus közül kell lennie.</span><span class="sxs-lookup"><span data-stu-id="45b0c-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="45b0c-110">Ha egy tárolási fiókba van bejelentkezve, a műveletnapló tárolási költségét a normál szokásos tárolási áron számlázzák.</span><span class="sxs-lookup"><span data-stu-id="45b0c-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="45b0c-111">Egy előfizetésben csak egy log-profil lehet, egy előfizetésben csak egy tárterület-fiók használható a műveletnapló exportálásához.</span><span class="sxs-lookup"><span data-stu-id="45b0c-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="45b0c-112">**Esemény-hub** : egy előfizetésben csak egy naplózási profil lehet, az előfizetéssel csak egy esemény-előfizetéssel exportálható a tevékenység naplója.</span><span class="sxs-lookup"><span data-stu-id="45b0c-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="45b0c-113">Ha a műveletnapló egy esemény központjának van továbbítva, a normál esemény hub árazása érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="45b0c-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="45b0c-114">A tevékenység naplóban az események egy régióra vonatkozhat vagy "globálisak" lehetnek.</span><span class="sxs-lookup"><span data-stu-id="45b0c-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="45b0c-115">Globális lényegében azt jelenti, hogy ezek az események a régió agnosztikusok és függetlenek a régiótól, az események többsége ebbe a kategóriába esik.</span><span class="sxs-lookup"><span data-stu-id="45b0c-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="45b0c-116">Ha a műveletnapló profilja a portálról van beállítva, implicit módon felveszi a "globális" kifejezést a felhasználói felületen kijelölt többi régióval együtt.</span><span class="sxs-lookup"><span data-stu-id="45b0c-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="45b0c-117">A parancsmag használatakor a "globális" helyet külön meg kell említeni a többi régióban kívül.</span><span class="sxs-lookup"><span data-stu-id="45b0c-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="45b0c-118">**Megjegyzés** : **a helyek "globális" beállításának hiánya következtében a tevékenység naplójának többsége nem fog exportálni.**</span><span class="sxs-lookup"><span data-stu-id="45b0c-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="45b0c-119">Ez a parancsmag végrehajtja a ShouldProcess mintát, azaz a felhasználó megerősítését kérheti az erőforrás tényleges létrehozása, módosítása vagy eltávolítása előtt.</span><span class="sxs-lookup"><span data-stu-id="45b0c-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="45b0c-120">Példák</span><span class="sxs-lookup"><span data-stu-id="45b0c-120">EXAMPLES</span></span>

### <span data-ttu-id="45b0c-121">1. példa: új log-profil hozzáadása a tevékenység naplójának exportálásához, amely a hely feltételéhez illő tárolási fiókhoz van illesztve</span><span class="sxs-lookup"><span data-stu-id="45b0c-121">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="45b0c-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="45b0c-122">PARAMETERS</span></span>

### <span data-ttu-id="45b0c-123">-Category (kategória)</span><span class="sxs-lookup"><span data-stu-id="45b0c-123">-Category</span></span>
<span data-ttu-id="45b0c-124">A kategóriák listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="45b0c-124">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="45b0c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45b0c-125">-DefaultProfile</span></span>
<span data-ttu-id="45b0c-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="45b0c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45b0c-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="45b0c-127">-Location</span></span>
<span data-ttu-id="45b0c-128">A napló profiljának helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45b0c-128">Specifies the location of the log profile.</span></span>
<span data-ttu-id="45b0c-129">Érvényes értékek: az alábbi parancsmagot futtatva érheti el a helyek legújabb listáját.</span><span class="sxs-lookup"><span data-stu-id="45b0c-129">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="45b0c-130">Get-AzureLocation | A DisplayName elem választása</span><span class="sxs-lookup"><span data-stu-id="45b0c-130">Get-AzureLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="45b0c-131">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="45b0c-131">-Name</span></span>
<span data-ttu-id="45b0c-132">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="45b0c-132">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="45b0c-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="45b0c-133">-RetentionInDays</span></span>
<span data-ttu-id="45b0c-134">A napok szerinti adatmegőrzési házirendet adja meg.</span><span class="sxs-lookup"><span data-stu-id="45b0c-134">Specifies the retention policy, in days.</span></span> <span data-ttu-id="45b0c-135">Ez az a napok száma, amelyekben a naplók megmaradnak a megadott tárolási fiókban.</span><span class="sxs-lookup"><span data-stu-id="45b0c-135">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="45b0c-136">Ha meg szeretné őrizni az adatvesztést, a **0** értékre kell állítania.</span><span class="sxs-lookup"><span data-stu-id="45b0c-136">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="45b0c-137">Ha nincs megadva, az alapértelmezett érték **0**.</span><span class="sxs-lookup"><span data-stu-id="45b0c-137">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="45b0c-138">A normál normál tárterület vagy az esemény-hub számlázási díja az adatmegőrzésre érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="45b0c-138">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="45b0c-139">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="45b0c-139">-ServiceBusRuleId</span></span>
<span data-ttu-id="45b0c-140">A szolgáltatási busz szabályának AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="45b0c-140">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="45b0c-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="45b0c-141">-StorageAccountId</span></span>
<span data-ttu-id="45b0c-142">A tárolási fiók AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="45b0c-142">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="45b0c-143">AZONOSÍTÓ: a tárolási fiók teljesen minősített erőforrás-azonosítója, például:</span><span class="sxs-lookup"><span data-stu-id="45b0c-143">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="45b0c-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="45b0c-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="45b0c-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="45b0c-145">-Confirm</span></span>
<span data-ttu-id="45b0c-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="45b0c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45b0c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45b0c-147">-WhatIf</span></span>
<span data-ttu-id="45b0c-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="45b0c-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45b0c-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="45b0c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45b0c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45b0c-150">CommonParameters</span></span>
<span data-ttu-id="45b0c-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="45b0c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45b0c-152">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45b0c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45b0c-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="45b0c-153">INPUTS</span></span>

### <span data-ttu-id="45b0c-154">System. String</span><span class="sxs-lookup"><span data-stu-id="45b0c-154">System.String</span></span>

### <span data-ttu-id="45b0c-155">System. null ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="45b0c-155">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="45b0c-156">System. Collections. Generic. list ' 1 [[System. string, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="45b0c-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="45b0c-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="45b0c-157">OUTPUTS</span></span>

### <span data-ttu-id="45b0c-158">Microsoft. Azure. commands. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="45b0c-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="45b0c-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="45b0c-159">NOTES</span></span>

## <span data-ttu-id="45b0c-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="45b0c-160">RELATED LINKS</span></span>

[<span data-ttu-id="45b0c-161">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="45b0c-161">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="45b0c-162">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="45b0c-162">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


