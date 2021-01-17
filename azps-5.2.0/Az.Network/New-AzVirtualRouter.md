---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362682"
---
# <span data-ttu-id="f3712-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="f3712-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="f3712-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3712-102">SYNOPSIS</span></span>
<span data-ttu-id="f3712-103">Létrehoz egy Azure VirtualRoutert.</span><span class="sxs-lookup"><span data-stu-id="f3712-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="f3712-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f3712-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3712-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f3712-105">DESCRIPTION</span></span>
<span data-ttu-id="f3712-106">A **New-AzVirtualRouter** parancsmag létrehoz egy Azure VirtualRoutert</span><span class="sxs-lookup"><span data-stu-id="f3712-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="f3712-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f3712-107">EXAMPLES</span></span>

### <span data-ttu-id="f3712-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f3712-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="f3712-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3712-109">PARAMETERS</span></span>

### <span data-ttu-id="f3712-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3712-110">-AsJob</span></span>
<span data-ttu-id="f3712-111">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="f3712-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3712-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3712-112">-DefaultProfile</span></span>
<span data-ttu-id="f3712-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3712-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3712-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f3712-114">-Force</span></span>
<span data-ttu-id="f3712-115">Ne kérjen megerősítést, ha felül szeretne írni egy erőforrást</span><span class="sxs-lookup"><span data-stu-id="f3712-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f3712-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="f3712-116">-HostedSubnet</span></span>
<span data-ttu-id="f3712-117">A virtuális útválasztót üzemeltető alhálózat.</span><span class="sxs-lookup"><span data-stu-id="f3712-117">The subnet where the virtual router is hosted.</span></span>

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

### <span data-ttu-id="f3712-118">-Location</span><span class="sxs-lookup"><span data-stu-id="f3712-118">-Location</span></span>
<span data-ttu-id="f3712-119">A hely.</span><span class="sxs-lookup"><span data-stu-id="f3712-119">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3712-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f3712-120">-Name</span></span>
<span data-ttu-id="f3712-121">A virtuális útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="f3712-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3712-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3712-122">-ResourceGroupName</span></span>
<span data-ttu-id="f3712-123">A virtuális útválasztó erőforráscsoportneve.</span><span class="sxs-lookup"><span data-stu-id="f3712-123">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3712-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="f3712-124">-Tag</span></span>
<span data-ttu-id="f3712-125">Erőforráscímkéket képviselő hashtable.</span><span class="sxs-lookup"><span data-stu-id="f3712-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3712-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3712-126">-Confirm</span></span>
<span data-ttu-id="f3712-127">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f3712-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3712-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3712-128">-WhatIf</span></span>
<span data-ttu-id="f3712-129">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f3712-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3712-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f3712-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3712-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3712-131">CommonParameters</span></span>
<span data-ttu-id="f3712-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3712-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3712-133">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3712-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3712-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3712-134">INPUTS</span></span>

### <span data-ttu-id="f3712-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f3712-135">System.String</span></span>

### <span data-ttu-id="f3712-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f3712-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f3712-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3712-137">OUTPUTS</span></span>

### <span data-ttu-id="f3712-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="f3712-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="f3712-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f3712-139">NOTES</span></span>

## <span data-ttu-id="f3712-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3712-140">RELATED LINKS</span></span>
