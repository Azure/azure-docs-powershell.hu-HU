---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: fe082dc38f8a16dcca897623c4817d728fdaf3c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924985"
---
# <span data-ttu-id="b7fef-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="b7fef-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="b7fef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7fef-102">SYNOPSIS</span></span>
<span data-ttu-id="b7fef-103">Létrehoz egy eseményindítót a megosztási előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="b7fef-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="b7fef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7fef-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7fef-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7fef-105">DESCRIPTION</span></span>
<span data-ttu-id="b7fef-106">A **New-AzDataShareTrigger** parancsmag létrehoz egy eseményindítót a megosztási előfizetéshez a megadott ismétlődési időközre és szinkronizálási időre az Azure-adatmegosztási fiókban.</span><span class="sxs-lookup"><span data-stu-id="b7fef-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="b7fef-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7fef-107">EXAMPLES</span></span>

### <span data-ttu-id="b7fef-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b7fef-108">Example 1</span></span>
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

<span data-ttu-id="b7fef-109">Ez a parancs egy új eseményindítót hoz létre az AdsTriggerhez a share subscription AdsShareSubscription eseményhez, napi 9 órai ismétlődési időközzel.</span><span class="sxs-lookup"><span data-stu-id="b7fef-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="b7fef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7fef-110">PARAMETERS</span></span>

### <span data-ttu-id="b7fef-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b7fef-111">-AccountName</span></span>
<span data-ttu-id="b7fef-112">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="b7fef-112">Azure data share account name</span></span>

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

### <span data-ttu-id="b7fef-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7fef-113">-AsJob</span></span>
<span data-ttu-id="b7fef-114">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="b7fef-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="b7fef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7fef-115">-DefaultProfile</span></span>
<span data-ttu-id="b7fef-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7fef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7fef-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b7fef-117">-Name</span></span>
<span data-ttu-id="b7fef-118">Azure data share trigger name</span><span class="sxs-lookup"><span data-stu-id="b7fef-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="b7fef-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="b7fef-119">-RecurrenceInterval</span></span>
<span data-ttu-id="b7fef-120">Az eseményindító ismétlődési időköze (nap vagy óra)</span><span class="sxs-lookup"><span data-stu-id="b7fef-120">The recurrence interval for the trigger (Day or Hour)</span></span>

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

### <span data-ttu-id="b7fef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7fef-121">-ResourceGroupName</span></span>
<span data-ttu-id="b7fef-122">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="b7fef-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b7fef-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b7fef-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="b7fef-124">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="b7fef-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b7fef-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="b7fef-125">-SynchronizationTime</span></span>
<span data-ttu-id="b7fef-126">Az eseményindító ütemezett szinkronizálásának kezdési ideje</span><span class="sxs-lookup"><span data-stu-id="b7fef-126">The start time of the scheduled synchronization for the trigger</span></span>

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

### <span data-ttu-id="b7fef-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7fef-127">-Confirm</span></span>
<span data-ttu-id="b7fef-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b7fef-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7fef-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7fef-129">-WhatIf</span></span>
<span data-ttu-id="b7fef-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b7fef-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7fef-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b7fef-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7fef-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7fef-132">CommonParameters</span></span>
<span data-ttu-id="b7fef-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7fef-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7fef-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7fef-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7fef-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7fef-135">INPUTS</span></span>

### <span data-ttu-id="b7fef-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="b7fef-136">None</span></span>

## <span data-ttu-id="b7fef-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7fef-137">OUTPUTS</span></span>

### <span data-ttu-id="b7fef-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="b7fef-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="b7fef-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7fef-139">NOTES</span></span>

## <span data-ttu-id="b7fef-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7fef-140">RELATED LINKS</span></span>
