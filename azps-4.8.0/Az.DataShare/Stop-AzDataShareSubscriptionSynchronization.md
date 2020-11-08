---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: e865098b0c85227baf1f537fb22c40ee351902fd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183641"
---
# <span data-ttu-id="2d1af-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="2d1af-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="2d1af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2d1af-102">SYNOPSIS</span></span>
<span data-ttu-id="2d1af-103">A megosztási előfizetés folyamatban lévő szinkronizálásának leállítása.</span><span class="sxs-lookup"><span data-stu-id="2d1af-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="2d1af-104">A megosztási előfizetések az erőforrás-azonosítón vagy annak nevén keresztül adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="2d1af-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="2d1af-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2d1af-105">SYNTAX</span></span>

### <span data-ttu-id="2d1af-106">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2d1af-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d1af-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d1af-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d1af-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d1af-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d1af-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="2d1af-109">DESCRIPTION</span></span>
<span data-ttu-id="2d1af-110">A **stop-AzDataShareSubscriptionSynchronization** parancsmag a megosztási előfizetések folyamatos szinkronizálását megszünteti</span><span class="sxs-lookup"><span data-stu-id="2d1af-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="2d1af-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2d1af-111">EXAMPLES</span></span>

### <span data-ttu-id="2d1af-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2d1af-112">Example 1</span></span>
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

<span data-ttu-id="2d1af-113">Az id-20a4416b-b33b-4539-a908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="2d1af-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="2d1af-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2d1af-114">PARAMETERS</span></span>

### <span data-ttu-id="2d1af-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2d1af-115">-AccountName</span></span>
<span data-ttu-id="2d1af-116">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="2d1af-116">Azure data share account name</span></span>

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

### <span data-ttu-id="2d1af-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d1af-117">-AsJob</span></span>
<span data-ttu-id="2d1af-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="2d1af-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="2d1af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d1af-119">-DefaultProfile</span></span>
<span data-ttu-id="2d1af-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d1af-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d1af-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d1af-121">-InputObject</span></span>
<span data-ttu-id="2d1af-122">Azure Data Share-előfizetés objektum</span><span class="sxs-lookup"><span data-stu-id="2d1af-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="2d1af-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d1af-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d1af-124">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="2d1af-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="2d1af-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d1af-125">-ResourceId</span></span>
<span data-ttu-id="2d1af-126">Az Azure Share-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="2d1af-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="2d1af-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="2d1af-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="2d1af-128">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="2d1af-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="2d1af-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="2d1af-129">-SynchronizationId</span></span>
<span data-ttu-id="2d1af-130">Leállítani kívánt szinkronizálási azonosító</span><span class="sxs-lookup"><span data-stu-id="2d1af-130">Synchronization id that needs to be stopped</span></span>

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

### <span data-ttu-id="2d1af-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2d1af-131">-Confirm</span></span>
<span data-ttu-id="2d1af-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2d1af-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d1af-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d1af-133">-WhatIf</span></span>
<span data-ttu-id="2d1af-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2d1af-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d1af-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2d1af-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d1af-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d1af-136">CommonParameters</span></span>
<span data-ttu-id="2d1af-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2d1af-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d1af-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2d1af-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d1af-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d1af-139">INPUTS</span></span>

### <span data-ttu-id="2d1af-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2d1af-140">System.String</span></span>

### <span data-ttu-id="2d1af-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="2d1af-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="2d1af-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d1af-142">OUTPUTS</span></span>

### <span data-ttu-id="2d1af-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="2d1af-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="2d1af-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2d1af-144">NOTES</span></span>

## <span data-ttu-id="2d1af-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d1af-145">RELATED LINKS</span></span>
