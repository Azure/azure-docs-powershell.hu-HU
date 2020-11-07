---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareTrigger.md
ms.openlocfilehash: a1ec489b91d2d510c16709fa0923117bbbaa804a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666684"
---
# <span data-ttu-id="189a8-101">Remove-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="189a8-101">Remove-AzDataShareTrigger</span></span>

## <span data-ttu-id="189a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="189a8-102">SYNOPSIS</span></span>
<span data-ttu-id="189a8-103">trigger eltávolítása</span><span class="sxs-lookup"><span data-stu-id="189a8-103">removes a trigger</span></span>

## <span data-ttu-id="189a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="189a8-104">SYNTAX</span></span>

### <span data-ttu-id="189a8-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="189a8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="189a8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="189a8-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareTrigger -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="189a8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="189a8-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareTrigger -InputObject <PSDataShareTrigger> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="189a8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="189a8-108">DESCRIPTION</span></span>
<span data-ttu-id="189a8-109">A **Remove-AzDataShareTrigger** parancsmag eltávolítja a DataShare-triggert</span><span class="sxs-lookup"><span data-stu-id="189a8-109">The **Remove-AzDataShareTrigger** cmdlet removes a datashare trigger</span></span>

## <span data-ttu-id="189a8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="189a8-110">EXAMPLES</span></span>

### <span data-ttu-id="189a8-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="189a8-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger"

Are you sure you want to remove trigger "AdsTrigger"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="189a8-112">Ez a parancs eltávolítja a AdsTrigger nevű triggert az előfizetés megosztása AdsShareSubscription.</span><span class="sxs-lookup"><span data-stu-id="189a8-112">This commands removes a trigger named AdsTrigger from share subscription AdsShareSubscription.</span></span> 

## <span data-ttu-id="189a8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="189a8-113">PARAMETERS</span></span>

### <span data-ttu-id="189a8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="189a8-114">-AccountName</span></span>
<span data-ttu-id="189a8-115">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="189a8-115">Azure data share account name</span></span>

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

### <span data-ttu-id="189a8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="189a8-116">-AsJob</span></span>
<span data-ttu-id="189a8-117">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="189a8-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="189a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="189a8-118">-DefaultProfile</span></span>
<span data-ttu-id="189a8-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="189a8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="189a8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="189a8-120">-InputObject</span></span>
<span data-ttu-id="189a8-121">Azure Data Share trigger objektum</span><span class="sxs-lookup"><span data-stu-id="189a8-121">Azure data share trigger object</span></span>


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

### <span data-ttu-id="189a8-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="189a8-122">-Name</span></span>
<span data-ttu-id="189a8-123">Azure Data Share – trigger neve</span><span class="sxs-lookup"><span data-stu-id="189a8-123">Azure data share trigger name</span></span>

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

### <span data-ttu-id="189a8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="189a8-124">-PassThru</span></span>
<span data-ttu-id="189a8-125">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="189a8-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="189a8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="189a8-126">-ResourceGroupName</span></span>
<span data-ttu-id="189a8-127">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="189a8-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="189a8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="189a8-128">-ResourceId</span></span>
<span data-ttu-id="189a8-129">Az Azure Data Share trigger erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="189a8-129">The resource id of azure data share trigger</span></span>

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

### <span data-ttu-id="189a8-130">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="189a8-130">-ShareSubscriptionName</span></span>
<span data-ttu-id="189a8-131">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="189a8-131">Azure data share subscription name</span></span>

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

### <span data-ttu-id="189a8-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="189a8-132">-Confirm</span></span>
<span data-ttu-id="189a8-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="189a8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="189a8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="189a8-134">-WhatIf</span></span>
<span data-ttu-id="189a8-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="189a8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="189a8-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="189a8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="189a8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="189a8-137">CommonParameters</span></span>
<span data-ttu-id="189a8-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="189a8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="189a8-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="189a8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="189a8-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="189a8-140">INPUTS</span></span>

### <span data-ttu-id="189a8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="189a8-141">System.String</span></span>

### <span data-ttu-id="189a8-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="189a8-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareTrigger</span></span>

## <span data-ttu-id="189a8-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="189a8-143">OUTPUTS</span></span>

### <span data-ttu-id="189a8-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="189a8-144">System.Boolean</span></span>

## <span data-ttu-id="189a8-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="189a8-145">NOTES</span></span>

## <span data-ttu-id="189a8-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="189a8-146">RELATED LINKS</span></span>
