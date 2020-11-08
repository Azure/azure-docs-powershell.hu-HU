---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: f4eff969d93f1c243b9dc15652249bc9800bfd45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017816"
---
# <span data-ttu-id="6fc0c-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="6fc0c-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="6fc0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6fc0c-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc0c-103">trigger eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6fc0c-103">removes a trigger</span></span>

## <span data-ttu-id="6fc0c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6fc0c-104">SYNTAX</span></span>

### <span data-ttu-id="6fc0c-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6fc0c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6fc0c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fc0c-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fc0c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fc0c-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fc0c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6fc0c-108">DESCRIPTION</span></span>
<span data-ttu-id="6fc0c-109">A **Remove-AzDataShareTrigger** parancsmag eltávolítja a DataShare-triggert</span><span class="sxs-lookup"><span data-stu-id="6fc0c-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="6fc0c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6fc0c-110">EXAMPLES</span></span>

### <span data-ttu-id="6fc0c-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6fc0c-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="6fc0c-112">Ez a parancs eltávolítja a AdsTrigger nevű triggert az előfizetés megosztása AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="6fc0c-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="6fc0c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6fc0c-113">PARAMETERS</span></span>

### <span data-ttu-id="6fc0c-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6fc0c-114">-AccountName</span></span>
<span data-ttu-id="6fc0c-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="6fc0c-115">Azure data share account name</span></span>

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

### <span data-ttu-id="6fc0c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fc0c-116">-AsJob</span></span>
<span data-ttu-id="6fc0c-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="6fc0c-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="6fc0c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc0c-118">-DefaultProfile</span></span>
<span data-ttu-id="6fc0c-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6fc0c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fc0c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fc0c-120">-InputObject</span></span>
<span data-ttu-id="6fc0c-121">Azure Data Share trigger objektum</span><span class="sxs-lookup"><span data-stu-id="6fc0c-121">Azure data share trigger object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fc0c-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6fc0c-122">-Name</span></span>
<span data-ttu-id="6fc0c-123">Azure Data Share – trigger neve</span><span class="sxs-lookup"><span data-stu-id="6fc0c-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="6fc0c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fc0c-124">-PassThru</span></span>
<span data-ttu-id="6fc0c-125">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="6fc0c-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="6fc0c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fc0c-126">-ResourceGroupName</span></span>
<span data-ttu-id="6fc0c-127">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="6fc0c-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="6fc0c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fc0c-128">-ResourceId</span></span>
<span data-ttu-id="6fc0c-129">Az Azure Data Share trigger erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="6fc0c-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="6fc0c-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6fc0c-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="6fc0c-131">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="6fc0c-131">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fc0c-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6fc0c-132">-Confirm</span></span>
<span data-ttu-id="6fc0c-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6fc0c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fc0c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fc0c-134">-WhatIf</span></span>
<span data-ttu-id="6fc0c-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6fc0c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fc0c-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6fc0c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fc0c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc0c-137">CommonParameters</span></span>
<span data-ttu-id="6fc0c-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6fc0c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc0c-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="6fc0c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc0c-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fc0c-140">INPUTS</span></span>

### <span data-ttu-id="6fc0c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6fc0c-141">System.String</span></span>

### <span data-ttu-id="6fc0c-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="6fc0c-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="6fc0c-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fc0c-143">OUTPUTS</span></span>

### <span data-ttu-id="6fc0c-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6fc0c-144">System.Boolean</span></span>

## <span data-ttu-id="6fc0c-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6fc0c-145">NOTES</span></span>

## <span data-ttu-id="6fc0c-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fc0c-146">RELATED LINKS</span></span>
