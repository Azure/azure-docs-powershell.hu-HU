---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: ed7114f37cebb093c8ba27ed60c0328234571f06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938345"
---
# <span data-ttu-id="edf7e-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="edf7e-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="edf7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edf7e-102">SYNOPSIS</span></span>
<span data-ttu-id="edf7e-103">Alkalmazásstatikációkhoz kapcsolt tárfiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="edf7e-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="edf7e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="edf7e-104">SYNTAX</span></span>

### <span data-ttu-id="edf7e-105">ByResourceNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="edf7e-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edf7e-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="edf7e-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edf7e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="edf7e-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edf7e-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="edf7e-108">DESCRIPTION</span></span>
<span data-ttu-id="edf7e-109">Alkalmazásstatikációkhoz kapcsolt tárfiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="edf7e-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="edf7e-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="edf7e-110">EXAMPLES</span></span>

### <span data-ttu-id="edf7e-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="edf7e-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="edf7e-112">Csatolt tárfiók létrehozása $account component "componentName" csoportban</span><span class="sxs-lookup"><span data-stu-id="edf7e-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="edf7e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edf7e-113">PARAMETERS</span></span>

### <span data-ttu-id="edf7e-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="edf7e-114">-ComponentName</span></span>
<span data-ttu-id="edf7e-115">Összetevő neve</span><span class="sxs-lookup"><span data-stu-id="edf7e-115">Component Name</span></span>

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

### <span data-ttu-id="edf7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf7e-116">-DefaultProfile</span></span>
<span data-ttu-id="edf7e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="edf7e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edf7e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edf7e-118">-InputObject</span></span>
<span data-ttu-id="edf7e-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="edf7e-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="edf7e-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="edf7e-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="edf7e-121">Tárfiók Erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="edf7e-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="edf7e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edf7e-122">-ResourceGroupName</span></span>
<span data-ttu-id="edf7e-123">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="edf7e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="edf7e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edf7e-124">-ResourceId</span></span>
<span data-ttu-id="edf7e-125">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="edf7e-125">Component ResourceId</span></span>

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

### <span data-ttu-id="edf7e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edf7e-126">-Confirm</span></span>
<span data-ttu-id="edf7e-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="edf7e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edf7e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edf7e-128">-WhatIf</span></span>
<span data-ttu-id="edf7e-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="edf7e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edf7e-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="edf7e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edf7e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf7e-131">CommonParameters</span></span>
<span data-ttu-id="edf7e-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edf7e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf7e-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edf7e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf7e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="edf7e-134">INPUTS</span></span>

### <span data-ttu-id="edf7e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="edf7e-135">System.String</span></span>

### <span data-ttu-id="edf7e-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="edf7e-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="edf7e-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="edf7e-137">OUTPUTS</span></span>

### <span data-ttu-id="edf7e-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="edf7e-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="edf7e-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="edf7e-139">NOTES</span></span>

## <span data-ttu-id="edf7e-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="edf7e-140">RELATED LINKS</span></span>
