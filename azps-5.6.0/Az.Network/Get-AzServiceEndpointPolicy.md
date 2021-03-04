---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: eac0d67e2c9ffc77d9387eeb599ad624ac01fbbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006278"
---
# <span data-ttu-id="0cf20-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0cf20-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="0cf20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cf20-102">SYNOPSIS</span></span>
<span data-ttu-id="0cf20-103">Szolgáltatásvégpont-házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="0cf20-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="0cf20-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0cf20-104">SYNTAX</span></span>

### <span data-ttu-id="0cf20-105">ListParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0cf20-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cf20-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0cf20-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cf20-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0cf20-107">DESCRIPTION</span></span>
<span data-ttu-id="0cf20-108">A **Get-AzServiceEndpointPolicy parancsmag** szolgáltatási végponti házirendet kap.</span><span class="sxs-lookup"><span data-stu-id="0cf20-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="0cf20-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0cf20-109">EXAMPLES</span></span>

### <span data-ttu-id="0cf20-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="0cf20-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0cf20-111">Ez a parancs leküldi a ServiceEndpointPolicy1 nevű szolgáltatásvégpont-házirendet, amely az ResourceGroup01 nevű erőforráscsoporthoz tartozik, és a $policy tárolja.</span><span class="sxs-lookup"><span data-stu-id="0cf20-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="0cf20-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="0cf20-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0cf20-113">Ez a parancs az ResourceGroup01 nevű erőforráscsoport összes szolgáltatásvégpont-házirendének listáját lekérte, és a $policyList tárolja.</span><span class="sxs-lookup"><span data-stu-id="0cf20-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="0cf20-114">3. példa</span><span class="sxs-lookup"><span data-stu-id="0cf20-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="0cf20-115">Ez a parancs a "ServiceEndpointPolicy" kezdetű összes szolgáltatásvégponti házirend listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="0cf20-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="0cf20-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0cf20-116">PARAMETERS</span></span>

### <span data-ttu-id="0cf20-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cf20-117">-DefaultProfile</span></span>
<span data-ttu-id="0cf20-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0cf20-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cf20-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0cf20-119">-Name</span></span>
<span data-ttu-id="0cf20-120">A szolgáltatás végponti házirendjának neve</span><span class="sxs-lookup"><span data-stu-id="0cf20-120">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="0cf20-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cf20-121">-ResourceGroupName</span></span>
<span data-ttu-id="0cf20-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="0cf20-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0cf20-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cf20-123">-ResourceId</span></span>
<span data-ttu-id="0cf20-124">A szolgáltatás végponti házirendje azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0cf20-124">The ID of the service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cf20-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0cf20-125">-Confirm</span></span>
<span data-ttu-id="0cf20-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0cf20-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cf20-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cf20-127">-WhatIf</span></span>
<span data-ttu-id="0cf20-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0cf20-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0cf20-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0cf20-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cf20-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cf20-130">CommonParameters</span></span>
<span data-ttu-id="0cf20-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cf20-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cf20-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0cf20-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cf20-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0cf20-133">INPUTS</span></span>

### <span data-ttu-id="0cf20-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0cf20-134">System.String</span></span>

## <span data-ttu-id="0cf20-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0cf20-135">OUTPUTS</span></span>

### <span data-ttu-id="0cf20-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0cf20-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="0cf20-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0cf20-137">NOTES</span></span>

## <span data-ttu-id="0cf20-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0cf20-138">RELATED LINKS</span></span>

[<span data-ttu-id="0cf20-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0cf20-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="0cf20-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0cf20-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="0cf20-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="0cf20-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
