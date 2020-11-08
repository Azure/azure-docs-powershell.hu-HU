---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: a0f8651bab30cf5a439b6e16110b34e7d256aa3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011827"
---
# <span data-ttu-id="50471-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="50471-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="50471-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="50471-102">SYNOPSIS</span></span>
<span data-ttu-id="50471-103">Létrehoz egy triggert a megosztási előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="50471-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="50471-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="50471-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50471-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="50471-105">DESCRIPTION</span></span>
<span data-ttu-id="50471-106">A **New-AzDataShareTrigger** parancsmag létrehoz egy triggert a megadott ismétlődési időtartományra és a szinkronizálási időpontra vonatkozóan az Azure Data Share-fiókban.</span><span class="sxs-lookup"><span data-stu-id="50471-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="50471-107">Példák</span><span class="sxs-lookup"><span data-stu-id="50471-107">EXAMPLES</span></span>

### <span data-ttu-id="50471-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="50471-108">Example 1</span></span>
```
PS C:\> New-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger" -RecurrenceInterval "Day" -SynchronizationTime "9:00"
CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="50471-109">Ez a parancs új trigger-AdsTrigger hoz létre a megosztási előfizetési AdsShareSubscription a 9-es napi ismétlődési intervallummal.</span><span class="sxs-lookup"><span data-stu-id="50471-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="50471-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="50471-110">PARAMETERS</span></span>

### <span data-ttu-id="50471-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="50471-111">-AccountName</span></span>
<span data-ttu-id="50471-112">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="50471-112">Azure data share account name</span></span>

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

### <span data-ttu-id="50471-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50471-113">-AsJob</span></span>
<span data-ttu-id="50471-114">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="50471-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="50471-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50471-115">-DefaultProfile</span></span>
<span data-ttu-id="50471-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="50471-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50471-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="50471-117">-Name</span></span>
<span data-ttu-id="50471-118">Azure Data Share – trigger neve</span><span class="sxs-lookup"><span data-stu-id="50471-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="50471-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="50471-119">-RecurrenceInterval</span></span>
<span data-ttu-id="50471-120">Az indítás ismétlődési intervalluma (nap vagy óra)</span><span class="sxs-lookup"><span data-stu-id="50471-120">The recurrence interval for the trigger (Day or Hour)</span></span>

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

### <span data-ttu-id="50471-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50471-121">-ResourceGroupName</span></span>
<span data-ttu-id="50471-122">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="50471-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="50471-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="50471-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="50471-124">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="50471-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="50471-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="50471-125">-SynchronizationTime</span></span>
<span data-ttu-id="50471-126">Az indító ütemezett szinkronizálás kezdési időpontja</span><span class="sxs-lookup"><span data-stu-id="50471-126">The start time of the scheduled synchronization for the trigger</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50471-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="50471-127">-Confirm</span></span>
<span data-ttu-id="50471-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="50471-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50471-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50471-129">-WhatIf</span></span>
<span data-ttu-id="50471-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="50471-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50471-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="50471-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50471-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50471-132">CommonParameters</span></span>
<span data-ttu-id="50471-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="50471-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50471-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50471-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50471-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="50471-135">INPUTS</span></span>

### <span data-ttu-id="50471-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="50471-136">None</span></span>

## <span data-ttu-id="50471-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="50471-137">OUTPUTS</span></span>

### <span data-ttu-id="50471-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="50471-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="50471-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="50471-139">NOTES</span></span>

## <span data-ttu-id="50471-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="50471-140">RELATED LINKS</span></span>
