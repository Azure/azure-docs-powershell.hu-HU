---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 5fdd59bd97d5d3e94dd413716e0838ca91ae1b7e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014418"
---
# <span data-ttu-id="20060-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="20060-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="20060-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20060-102">SYNOPSIS</span></span>
<span data-ttu-id="20060-103">Szinkronizált kezdeményezést kezdeményez a megosztási előfizetésekhez.</span><span class="sxs-lookup"><span data-stu-id="20060-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="20060-104">A megosztási előfizetések az erőforrás-azonosítón vagy annak nevén keresztül adhatók meg.</span><span class="sxs-lookup"><span data-stu-id="20060-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="20060-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20060-105">SYNTAX</span></span>

### <span data-ttu-id="20060-106">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="20060-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20060-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20060-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20060-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20060-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20060-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="20060-109">DESCRIPTION</span></span>
<span data-ttu-id="20060-110">A **Start-AzDataShareSubscriptionSynchronization** parancsmag a megosztási előfizetés szinkronizálását kezdeményezi</span><span class="sxs-lookup"><span data-stu-id="20060-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="20060-111">Példák</span><span class="sxs-lookup"><span data-stu-id="20060-111">EXAMPLES</span></span>

### <span data-ttu-id="20060-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="20060-112">Example 1</span></span>
```
PS C:\> Start-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationMode Incremental

Confirm
AdsShareSubscription
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

durationMs        : 231869
endTime           : 7/9/2019 11:44:41 PM
message           :
startTime         : 7/9/2019 11:40:53 PM
status            : Succeeded
synchronizationId : 20a4416b-b33b-4539-a908-71dc8ef698fb
```

<span data-ttu-id="20060-113">Ez a parancs a AdsShareSubscription nevű sharesubscription szinkronizálását kezdeményezi a WikiAds fiókban.</span><span class="sxs-lookup"><span data-stu-id="20060-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="20060-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20060-114">PARAMETERS</span></span>

### <span data-ttu-id="20060-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="20060-115">-AccountName</span></span>
<span data-ttu-id="20060-116">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="20060-116">Azure data share account name</span></span>

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

### <span data-ttu-id="20060-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20060-117">-AsJob</span></span>
<span data-ttu-id="20060-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="20060-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="20060-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20060-119">-DefaultProfile</span></span>
<span data-ttu-id="20060-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20060-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20060-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20060-121">-InputObject</span></span>
<span data-ttu-id="20060-122">Azure Data Share-előfizetés objektum</span><span class="sxs-lookup"><span data-stu-id="20060-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="20060-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20060-123">-ResourceGroupName</span></span>
<span data-ttu-id="20060-124">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="20060-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="20060-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20060-125">-ResourceId</span></span>
<span data-ttu-id="20060-126">Az Azure Share-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="20060-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="20060-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="20060-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="20060-128">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="20060-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="20060-129">-SynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="20060-129">-SynchronizationMode</span></span>
<span data-ttu-id="20060-130">Szinkronizálási mód (FullSync vagy növekményes)</span><span class="sxs-lookup"><span data-stu-id="20060-130">Synchronization mode (FullSync or Incremental)</span></span>

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

### <span data-ttu-id="20060-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="20060-131">-Confirm</span></span>
<span data-ttu-id="20060-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="20060-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20060-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20060-133">-WhatIf</span></span>
<span data-ttu-id="20060-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="20060-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20060-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="20060-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20060-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20060-136">CommonParameters</span></span>
<span data-ttu-id="20060-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20060-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20060-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20060-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20060-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20060-139">INPUTS</span></span>

### <span data-ttu-id="20060-140">System. String</span><span class="sxs-lookup"><span data-stu-id="20060-140">System.String</span></span>

### <span data-ttu-id="20060-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="20060-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="20060-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20060-142">OUTPUTS</span></span>

### <span data-ttu-id="20060-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="20060-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="20060-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20060-144">NOTES</span></span>

## <span data-ttu-id="20060-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20060-145">RELATED LINKS</span></span>
