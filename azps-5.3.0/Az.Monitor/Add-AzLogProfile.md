---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: bc0f1a6aacc6188a982fe75fa021bdafdc4e02de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470030"
---
# <span data-ttu-id="7bfcb-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="7bfcb-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="7bfcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bfcb-102">SYNOPSIS</span></span>
<span data-ttu-id="7bfcb-103">Létrehoz egy új tevékenységnaplóprofilt.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-103">Creates a new activity log profile.</span></span> <span data-ttu-id="7bfcb-104">Ezzel a profillal archiválhatja a tevékenységnaplót egy Azure-tárfiókba, vagy adatfolyamként továbbíthatja egy Azure eseményközpontba ugyanabban az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="7bfcb-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7bfcb-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bfcb-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7bfcb-106">DESCRIPTION</span></span>
<span data-ttu-id="7bfcb-107">Az **Add-AzLogProfile** parancsmag létrehoz egy naplóprofilt.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="7bfcb-108">**Tárfiók** – Csak a normál tárfiók (a prémium szintű tárfiók nem támogatott) támogatott.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="7bfcb-109">Típusának vagy ARM lehet.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="7bfcb-110">Ha egy tárfiókba van bejelentkezve, a tevékenységnapló tárolásának költségeit normál normál tárterületárak szerint számlázjuk.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="7bfcb-111">Előfizetésenként csak egy naplóprofil lehet, ezért előfizetésenként csak egy tárfiók használható a tevékenységnapló exportálására.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="7bfcb-112">**Eseményközpont** – Előfizetésenként csak egy naplóprofil lehet, ezért előfizetésenként csak egy eseményközpont használható a tevékenységnapló exportálására.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="7bfcb-113">Ha a tevékenységnaplót egy eseményközpontba továbbítja, az eseményközpont szokásos ára lesz érvényben.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="7bfcb-114">A tevékenységnaplóban az események egy régióra vonatkoznak, vagy lehetnek "globálisak".</span><span class="sxs-lookup"><span data-stu-id="7bfcb-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="7bfcb-115">Globálisan azt jelenti, hogy ezek az események régiódiagnosztikai események, és függetlenek a régiótól, valójában az események többsége ebbe a kategóriába tartozik.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="7bfcb-116">Ha a tevékenységnapló profilja a portálról van beállítva, az implicit módon hozzáadja a "Global" értéket a felhasználói felületen kijelölt többi régióval együtt.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="7bfcb-117">A parancsmag használata esetén a "Global" (Globális) helyet minden más régión kívül külön meg kell említeni.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="7bfcb-118">**Megjegyzés:-** Ha nem sikerül beállítani **a "Global" (Globális)** beállítását a helyeken, a tevékenységnapló nagy része nem lesz exportálva.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="7bfcb-119">Ez a parancsmag implementálja a ShouldProcess mintát, azaz megerősítést kérhet a felhasználótól, mielőtt ténylegesen létrehozza, módosítja vagy eltávolítja az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="7bfcb-120">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7bfcb-120">EXAMPLES</span></span>

### <span data-ttu-id="7bfcb-121">1. példa: Új naplóprofil hozzáadása a helyfeltűnésnek megfelelő tevékenységnapló exportálása egy tárfiókba</span><span class="sxs-lookup"><span data-stu-id="7bfcb-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="7bfcb-122">2. példa</span><span class="sxs-lookup"><span data-stu-id="7bfcb-122">Example 2</span></span>

<span data-ttu-id="7bfcb-123">Létrehoz egy új tevékenységnaplóprofilt.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-123">Creates a new activity log profile.</span></span> <span data-ttu-id="7bfcb-124">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="7bfcb-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="7bfcb-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bfcb-125">PARAMETERS</span></span>

### <span data-ttu-id="7bfcb-126">-Category</span><span class="sxs-lookup"><span data-stu-id="7bfcb-126">-Category</span></span>
<span data-ttu-id="7bfcb-127">A kategóriák listáját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-127">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="7bfcb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bfcb-128">-DefaultProfile</span></span>
<span data-ttu-id="7bfcb-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7bfcb-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bfcb-130">-Location</span><span class="sxs-lookup"><span data-stu-id="7bfcb-130">-Location</span></span>
<span data-ttu-id="7bfcb-131">A naplóprofil helyét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="7bfcb-132">Érvényes értékek: Futtassa a parancsmag alatt a helyek legújabb listáját.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="7bfcb-133">Get-AzLocation | Select DisplayName</span><span class="sxs-lookup"><span data-stu-id="7bfcb-133">Get-AzLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="7bfcb-134">-Name</span><span class="sxs-lookup"><span data-stu-id="7bfcb-134">-Name</span></span>
<span data-ttu-id="7bfcb-135">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-135">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="7bfcb-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7bfcb-136">-RetentionInDays</span></span>
<span data-ttu-id="7bfcb-137">Az adatmegőrzési házirendet napokban adja meg.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="7bfcb-138">Ez az a napok száma, amikor a naplók megőrzve vannak a megadott tárfiókban.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="7bfcb-139">Az adatok megőrzéséhez állítsa ezt **0-ra.**</span><span class="sxs-lookup"><span data-stu-id="7bfcb-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="7bfcb-140">Ha nincs megadva, akkor alapértelmezés szerint **0 lesz.**</span><span class="sxs-lookup"><span data-stu-id="7bfcb-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="7bfcb-141">Az adatmegőrzésre normál normál tárterület- vagy eseményközponti számlázási díjak vonatkoznak.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="7bfcb-142">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="7bfcb-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="7bfcb-143">A Szolgáltatásbusz szabály azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-143">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="7bfcb-144">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7bfcb-144">-StorageAccountId</span></span>
<span data-ttu-id="7bfcb-145">A Tárfiók azonosítója.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="7bfcb-146">Az azonosító például a tárfiók teljes erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="7bfcb-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="7bfcb-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="7bfcb-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="7bfcb-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bfcb-148">-Confirm</span></span>
<span data-ttu-id="7bfcb-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bfcb-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bfcb-150">-WhatIf</span></span>
<span data-ttu-id="7bfcb-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bfcb-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bfcb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bfcb-153">CommonParameters</span></span>
<span data-ttu-id="7bfcb-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bfcb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bfcb-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bfcb-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bfcb-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bfcb-156">INPUTS</span></span>

### <span data-ttu-id="7bfcb-157">System.String</span><span class="sxs-lookup"><span data-stu-id="7bfcb-157">System.String</span></span>

### <span data-ttu-id="7bfcb-158">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7bfcb-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7bfcb-159">System.Collections.Generic.List'1[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7bfcb-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="7bfcb-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bfcb-160">OUTPUTS</span></span>

### <span data-ttu-id="7bfcb-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="7bfcb-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="7bfcb-162">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7bfcb-162">NOTES</span></span>

## <span data-ttu-id="7bfcb-163">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7bfcb-163">RELATED LINKS</span></span>

[<span data-ttu-id="7bfcb-164">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="7bfcb-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="7bfcb-165">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="7bfcb-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


