---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/stop-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Stop-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: e865098b0c85227baf1f537fb22c40ee351902fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204318"
---
# <span data-ttu-id="22f86-101">Stop-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="22f86-101">Stop-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="22f86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22f86-102">SYNOPSIS</span></span>
<span data-ttu-id="22f86-103">Leállítja a folyamatban lévő szinkronizálást egy megosztási előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="22f86-103">Stops ongoing synchronization for a share subscription.</span></span> <span data-ttu-id="22f86-104">A megosztási előfizetés az erőforrás-azonosítón vagy a nevén keresztül is megadva lehet.</span><span class="sxs-lookup"><span data-stu-id="22f86-104">A share subscription can be specified through its resource id or its name.</span></span>

## <span data-ttu-id="22f86-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22f86-105">SYNTAX</span></span>

### <span data-ttu-id="22f86-106">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22f86-106">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22f86-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22f86-107">ByResourceIdParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -SynchronizationId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22f86-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22f86-108">ByObjectParameterSet</span></span>
```
Stop-AzDataShareSubscriptionSynchronization -InputObject <PSDataShareSubscription> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22f86-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22f86-109">DESCRIPTION</span></span>
<span data-ttu-id="22f86-110">A **Stop-AzDataShareSubscriptionSynchronization** parancsmag leállítja a folyamatban lévő szinkronizálást egy megosztási előfizetésben</span><span class="sxs-lookup"><span data-stu-id="22f86-110">The **Stop-AzDataShareSubscriptionSynchronization** cmdlet stops ongoing synchronization for a share subscription</span></span>

## <span data-ttu-id="22f86-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22f86-111">EXAMPLES</span></span>

### <span data-ttu-id="22f86-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="22f86-112">Example 1</span></span>
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

<span data-ttu-id="22f86-113">Leállítja az id azonosítóval azonosított folyamatban lévő szinkronizálást – 20a4416b-b33b-4539-a908-71dc8ef698fb</span><span class="sxs-lookup"><span data-stu-id="22f86-113">Stops ongoing synchronization identified by id - 20a4416b-b33b-4539-a908-71dc8ef698fb</span></span>

## <span data-ttu-id="22f86-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22f86-114">PARAMETERS</span></span>

### <span data-ttu-id="22f86-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="22f86-115">-AccountName</span></span>
<span data-ttu-id="22f86-116">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="22f86-116">Azure data share account name</span></span>

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

### <span data-ttu-id="22f86-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22f86-117">-AsJob</span></span>
<span data-ttu-id="22f86-118">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="22f86-118">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="22f86-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22f86-119">-DefaultProfile</span></span>
<span data-ttu-id="22f86-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22f86-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22f86-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22f86-121">-InputObject</span></span>
<span data-ttu-id="22f86-122">Azure data share subscription object</span><span class="sxs-lookup"><span data-stu-id="22f86-122">Azure data share subscription object</span></span>


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

### <span data-ttu-id="22f86-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22f86-123">-ResourceGroupName</span></span>
<span data-ttu-id="22f86-124">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="22f86-124">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="22f86-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22f86-125">-ResourceId</span></span>
<span data-ttu-id="22f86-126">Az Azure Share-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="22f86-126">The resource id of the azure share subscription</span></span>

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

### <span data-ttu-id="22f86-127">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="22f86-127">-ShareSubscriptionName</span></span>
<span data-ttu-id="22f86-128">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="22f86-128">Azure data share subscription name</span></span>

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

### <span data-ttu-id="22f86-129">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="22f86-129">-SynchronizationId</span></span>
<span data-ttu-id="22f86-130">Le kell állítani a szinkronizálási azonosítót</span><span class="sxs-lookup"><span data-stu-id="22f86-130">Synchronization id that needs to be stopped</span></span>

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

### <span data-ttu-id="22f86-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22f86-131">-Confirm</span></span>
<span data-ttu-id="22f86-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="22f86-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22f86-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22f86-133">-WhatIf</span></span>
<span data-ttu-id="22f86-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="22f86-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22f86-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22f86-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22f86-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22f86-136">CommonParameters</span></span>
<span data-ttu-id="22f86-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22f86-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22f86-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22f86-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22f86-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22f86-139">INPUTS</span></span>

### <span data-ttu-id="22f86-140">System.String</span><span class="sxs-lookup"><span data-stu-id="22f86-140">System.String</span></span>

### <span data-ttu-id="22f86-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="22f86-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="22f86-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22f86-142">OUTPUTS</span></span>

### <span data-ttu-id="22f86-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="22f86-143">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="22f86-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22f86-144">NOTES</span></span>

## <span data-ttu-id="22f86-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22f86-145">RELATED LINKS</span></span>
