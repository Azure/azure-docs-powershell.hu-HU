---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 01ca3c42db57760f23e49f93fc7e4d533b4047b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666678"
---
# <span data-ttu-id="3f1e5-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="3f1e5-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="3f1e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f1e5-102">SYNOPSIS</span></span>
<span data-ttu-id="3f1e5-103">A megosztási előfizetés folyamatban lévő szinkronizálásának leállítása.</span><span class="sxs-lookup"><span data-stu-id="3f1e5-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="3f1e5-104">A megosztási előfizetések az erőforrás-azonosítón vagy annak nevén keresztül adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="3f1e5-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="3f1e5-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f1e5-105">SYNTAX</span></span>

### <span data-ttu-id="3f1e5-106">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3f1e5-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f1e5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f1e5-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f1e5-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f1e5-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f1e5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f1e5-109">DESCRIPTION</span></span>
<span data-ttu-id="3f1e5-110">A **stop-AzDataShareSubscriptionSynchronization** parancsmag a megosztási előfizetések folyamatos szinkronizálását megszünteti</span><span class="sxs-lookup"><span data-stu-id="3f1e5-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="3f1e5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3f1e5-111">EXAMPLES</span></span>

### <span data-ttu-id="3f1e5-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3f1e5-112">Example 1</span></span>
```
PS C:\> Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId 20a4416b-b33b-4539-a908-71dc8ef698fb

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Canceled
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="3f1e5-113">Az id-20a4416b-b33b-4539-a908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="3f1e5-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="3f1e5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f1e5-114">PARAMETERS</span></span>

### <span data-ttu-id="3f1e5-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3f1e5-115">-AccountName</span></span>
<span data-ttu-id="3f1e5-116">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="3f1e5-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f1e5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f1e5-117">-AsJob</span></span>
<span data-ttu-id="3f1e5-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="3f1e5-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="3f1e5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f1e5-119">-DefaultProfile</span></span>
<span data-ttu-id="3f1e5-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f1e5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f1e5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f1e5-121">-InputObject</span></span>
<span data-ttu-id="3f1e5-122">Azure Data Share-előfizetés objektum</span><span class="sxs-lookup"><span data-stu-id="3f1e5-122">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f1e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f1e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="3f1e5-124">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="3f1e5-124">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f1e5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f1e5-125">-ResourceId</span></span>
<span data-ttu-id="3f1e5-126">Az Azure Share-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3f1e5-126">The resource id of the azure share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f1e5-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3f1e5-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="3f1e5-128">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="3f1e5-128">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f1e5-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="3f1e5-129">-SynchronizationId</span></span>
<span data-ttu-id="3f1e5-130">Leállítani kívánt szinkronizálási azonosító</span><span class="sxs-lookup"><span data-stu-id="3f1e5-130">Synchronization id that needs to be stopped</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f1e5-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3f1e5-131">-Confirm</span></span>
<span data-ttu-id="3f1e5-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3f1e5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f1e5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f1e5-133">-WhatIf</span></span>
<span data-ttu-id="3f1e5-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3f1e5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f1e5-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3f1e5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f1e5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f1e5-136">CommonParameters</span></span>
<span data-ttu-id="3f1e5-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f1e5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f1e5-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f1e5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f1e5-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f1e5-139">INPUTS</span></span>

### <span data-ttu-id="3f1e5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3f1e5-140">System.String</span></span>

### <span data-ttu-id="3f1e5-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="3f1e5-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="3f1e5-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f1e5-142">OUTPUTS</span></span>

### <span data-ttu-id="3f1e5-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="3f1e5-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="3f1e5-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f1e5-144">NOTES</span></span>

## <span data-ttu-id="3f1e5-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f1e5-145">RELATED LINKS</span></span>
