---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 652a5668bd641ae1b68093f431e0aa0963aca50b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180656"
---
# <span data-ttu-id="73feb-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="73feb-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="73feb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="73feb-102">SYNOPSIS</span></span>
<span data-ttu-id="73feb-103">Betekintést hoz létre a kapcsolt tárolási fiók</span><span class="sxs-lookup"><span data-stu-id="73feb-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="73feb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="73feb-104">SYNTAX</span></span>

### <span data-ttu-id="73feb-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="73feb-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73feb-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73feb-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73feb-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73feb-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73feb-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="73feb-108">DESCRIPTION</span></span>
<span data-ttu-id="73feb-109">Betekintést hoz létre a kapcsolt tárolási fiók</span><span class="sxs-lookup"><span data-stu-id="73feb-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="73feb-110">Példák</span><span class="sxs-lookup"><span data-stu-id="73feb-110">EXAMPLES</span></span>

### <span data-ttu-id="73feb-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="73feb-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="73feb-112">Kapcsolt tárolási fiók létrehozása $account a "componentName" összetevő alatt</span><span class="sxs-lookup"><span data-stu-id="73feb-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="73feb-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="73feb-113">PARAMETERS</span></span>

### <span data-ttu-id="73feb-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="73feb-114">-ComponentName</span></span>
<span data-ttu-id="73feb-115">Összetevő neve</span><span class="sxs-lookup"><span data-stu-id="73feb-115">Component Name</span></span>

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

### <span data-ttu-id="73feb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73feb-116">-DefaultProfile</span></span>
<span data-ttu-id="73feb-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="73feb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73feb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73feb-118">-InputObject</span></span>
<span data-ttu-id="73feb-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="73feb-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="73feb-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="73feb-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="73feb-121">Tárolási fiók ResourceId</span><span class="sxs-lookup"><span data-stu-id="73feb-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="73feb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73feb-122">-ResourceGroupName</span></span>
<span data-ttu-id="73feb-123">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="73feb-123">Resource Group Name</span></span>

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

### <span data-ttu-id="73feb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73feb-124">-ResourceId</span></span>
<span data-ttu-id="73feb-125">Összetevő-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73feb-125">Component ResourceId</span></span>

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

### <span data-ttu-id="73feb-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="73feb-126">-Confirm</span></span>
<span data-ttu-id="73feb-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="73feb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73feb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73feb-128">-WhatIf</span></span>
<span data-ttu-id="73feb-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="73feb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73feb-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="73feb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73feb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73feb-131">CommonParameters</span></span>
<span data-ttu-id="73feb-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="73feb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73feb-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="73feb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73feb-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="73feb-134">INPUTS</span></span>

### <span data-ttu-id="73feb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="73feb-135">System.String</span></span>

### <span data-ttu-id="73feb-136">Microsoft. Azure. Command. ApplicationInsights. models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="73feb-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="73feb-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="73feb-137">OUTPUTS</span></span>

### <span data-ttu-id="73feb-138">Microsoft. Azure. Command. ApplicationInsights. models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="73feb-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="73feb-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="73feb-139">NOTES</span></span>

## <span data-ttu-id="73feb-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="73feb-140">RELATED LINKS</span></span>
