---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/start-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Start-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: b2fe61d4493fea64f4ee7b07bdd14905fb7661db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925873"
---
# <span data-ttu-id="8c33f-101">Start-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="8c33f-101">Start-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="8c33f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c33f-102">SYNOPSIS</span></span>
<span data-ttu-id="8c33f-103">Szinkronizálást kezdeményez egy megosztási előfizetéshez.</span><span class="sxs-lookup"><span data-stu-id="8c33f-103">Initiates synchronization for a share subscription.</span></span> <span data-ttu-id="8c33f-104">A megosztási előfizetés az erőforrás-azonosítón vagy a nevén keresztül is megadva lehet.</span><span class="sxs-lookup"><span data-stu-id="8c33f-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="8c33f-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c33f-105">SYNTAX</span></span>

### <span data-ttu-id="8c33f-106">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8c33f-106">ByFieldsParameterSet (Default)</span></span>
```
Start-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationMode <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c33f-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c33f-107">ByResourceIdParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -SynchronizationMode <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c33f-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c33f-108">ByObjectParameterSet</span></span>
```
Start-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c33f-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c33f-109">DESCRIPTION</span></span>
<span data-ttu-id="8c33f-110">A **Start-AzDataShareSubscriptionSynchronization** parancsmag elindítja a szinkronizálást a megosztási előfizetéshez</span><span class="sxs-lookup"><span data-stu-id="8c33f-110">The **Start-AzDataShareSubscriptionSynchronization** cmdlet initiates synchronization for a share subscription</span></span>

## <span data-ttu-id="8c33f-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c33f-111">EXAMPLES</span></span>

### <span data-ttu-id="8c33f-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="8c33f-112">Example 1</span></span>
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

<span data-ttu-id="8c33f-113">Ez a parancs szinkronizálást kezdeményez egy AdsShareSubscription nevű sharesubscriptionhoz a wikiad-fiókokban.</span><span class="sxs-lookup"><span data-stu-id="8c33f-113">This commands initiates synchronization for a sharesubscription named AdsShareSubscription in account WikiAds.</span></span> 

## <span data-ttu-id="8c33f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c33f-114">PARAMETERS</span></span>

### <span data-ttu-id="8c33f-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8c33f-115">-AccountName</span></span>
<span data-ttu-id="8c33f-116">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="8c33f-116">Azure data share account name</span></span>

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

### <span data-ttu-id="8c33f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c33f-117">-AsJob</span></span>
<span data-ttu-id="8c33f-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="8c33f-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="8c33f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c33f-119">-DefaultProfile</span></span>
<span data-ttu-id="8c33f-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8c33f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c33f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c33f-121">-InputObject</span></span>
<span data-ttu-id="8c33f-122">Azure data share subscription object</span><span class="sxs-lookup"><span data-stu-id="8c33f-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="8c33f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c33f-123">-ResourceGroupName</span></span>
<span data-ttu-id="8c33f-124">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="8c33f-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="8c33f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c33f-125">-ResourceId</span></span>
<span data-ttu-id="8c33f-126">Az Azure Share-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="8c33f-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="8c33f-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8c33f-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="8c33f-128">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="8c33f-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="8c33f-129">-SynchronizationMode</span><span class="sxs-lookup"><span data-stu-id="8c33f-129">-SynchronizationMode</span></span>
<span data-ttu-id="8c33f-130">Szinkronizálási mód (FullSync vagy Növekményes)</span><span class="sxs-lookup"><span data-stu-id="8c33f-130">Synchronization mode (FullSync or Incremental)</span></span>

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

### <span data-ttu-id="8c33f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c33f-131">-Confirm</span></span>
<span data-ttu-id="8c33f-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="8c33f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c33f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c33f-133">-WhatIf</span></span>
<span data-ttu-id="8c33f-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="8c33f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c33f-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="8c33f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c33f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c33f-136">CommonParameters</span></span>
<span data-ttu-id="8c33f-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c33f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c33f-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c33f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c33f-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c33f-139">INPUTS</span></span>

### <span data-ttu-id="8c33f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8c33f-140">System.String</span></span>

### <span data-ttu-id="8c33f-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="8c33f-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="8c33f-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c33f-142">OUTPUTS</span></span>

### <span data-ttu-id="8c33f-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="8c33f-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="8c33f-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c33f-144">NOTES</span></span>

## <span data-ttu-id="8c33f-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c33f-145">RELATED LINKS</span></span>
