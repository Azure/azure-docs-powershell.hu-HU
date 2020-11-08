---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025810"
---
# <span data-ttu-id="97a28-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97a28-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="97a28-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97a28-102">SYNOPSIS</span></span>
<span data-ttu-id="97a28-103">Az alkalmazásban észlelt, a hivatkozásokat tároló fiók módosítása</span><span class="sxs-lookup"><span data-stu-id="97a28-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="97a28-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97a28-104">SYNTAX</span></span>

### <span data-ttu-id="97a28-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="97a28-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97a28-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="97a28-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97a28-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="97a28-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97a28-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="97a28-108">DESCRIPTION</span></span>
<span data-ttu-id="97a28-109">Az alkalmazásban észlelt, a hivatkozásokat tároló fiók módosítása</span><span class="sxs-lookup"><span data-stu-id="97a28-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="97a28-110">Példák</span><span class="sxs-lookup"><span data-stu-id="97a28-110">EXAMPLES</span></span>

### <span data-ttu-id="97a28-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="97a28-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="97a28-112">A kapcsolódó tárolási fiók frissítése a "componentName" összetevővel a $account társításához</span><span class="sxs-lookup"><span data-stu-id="97a28-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="97a28-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97a28-113">PARAMETERS</span></span>

### <span data-ttu-id="97a28-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="97a28-114">-ComponentName</span></span>
<span data-ttu-id="97a28-115">Összetevő neve</span><span class="sxs-lookup"><span data-stu-id="97a28-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a28-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a28-116">-DefaultProfile</span></span>
<span data-ttu-id="97a28-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="97a28-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97a28-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97a28-118">-InputObject</span></span>
<span data-ttu-id="97a28-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="97a28-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97a28-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="97a28-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="97a28-121">Tárolási fiók ResourceId</span><span class="sxs-lookup"><span data-stu-id="97a28-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="97a28-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97a28-122">-ResourceGroupName</span></span>
<span data-ttu-id="97a28-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="97a28-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a28-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97a28-124">-ResourceId</span></span>
<span data-ttu-id="97a28-125">Összetevő-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97a28-125">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a28-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="97a28-126">-Confirm</span></span>
<span data-ttu-id="97a28-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="97a28-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97a28-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97a28-128">-WhatIf</span></span>
<span data-ttu-id="97a28-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="97a28-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97a28-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="97a28-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97a28-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a28-131">CommonParameters</span></span>
<span data-ttu-id="97a28-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97a28-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a28-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="97a28-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a28-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97a28-134">INPUTS</span></span>

### <span data-ttu-id="97a28-135">System. String</span><span class="sxs-lookup"><span data-stu-id="97a28-135">System.String</span></span>

### <span data-ttu-id="97a28-136">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="97a28-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="97a28-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97a28-137">OUTPUTS</span></span>

### <span data-ttu-id="97a28-138">Microsoft. Azure. Command. ApplicationInsights. models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="97a28-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="97a28-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97a28-139">NOTES</span></span>

## <span data-ttu-id="97a28-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97a28-140">RELATED LINKS</span></span>
