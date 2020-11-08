---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184812"
---
# <span data-ttu-id="5f8d6-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5f8d6-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="5f8d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f8d6-102">SYNOPSIS</span></span>
<span data-ttu-id="5f8d6-103">Azure-VirtualRouter hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5f8d6-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="5f8d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f8d6-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f8d6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f8d6-105">DESCRIPTION</span></span>
<span data-ttu-id="5f8d6-106">A **New-AzVirtualRouter** parancsmag létrehoz egy Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5f8d6-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="5f8d6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5f8d6-107">EXAMPLES</span></span>

### <span data-ttu-id="5f8d6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5f8d6-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="5f8d6-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f8d6-109">PARAMETERS</span></span>

### <span data-ttu-id="5f8d6-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5f8d6-110">-AsJob</span></span>
<span data-ttu-id="5f8d6-111">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="5f8d6-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5f8d6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f8d6-112">-DefaultProfile</span></span>
<span data-ttu-id="5f8d6-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f8d6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f8d6-114">-Force</span><span class="sxs-lookup"><span data-stu-id="5f8d6-114">-Force</span></span>
<span data-ttu-id="5f8d6-115">Ha egy erőforrást felül szeretne írni, ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5f8d6-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5f8d6-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="5f8d6-116">-HostedSubnet</span></span>
<span data-ttu-id="5f8d6-117">Annak az alhálózatnak a helye, ahol a virtuális útválasztó van tárolva.</span><span class="sxs-lookup"><span data-stu-id="5f8d6-117">The subnet where the virtual router is hosted.</span></span>

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

### <span data-ttu-id="5f8d6-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="5f8d6-118">-Location</span></span>
<span data-ttu-id="5f8d6-119">A hely.</span><span class="sxs-lookup"><span data-stu-id="5f8d6-119">The location.</span></span>

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

### <span data-ttu-id="5f8d6-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5f8d6-120">-Name</span></span>
<span data-ttu-id="5f8d6-121">A virtuális útválasztó neve.</span><span class="sxs-lookup"><span data-stu-id="5f8d6-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="5f8d6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f8d6-122">-ResourceGroupName</span></span>
<span data-ttu-id="5f8d6-123">A virtuális útválasztó erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5f8d6-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="5f8d6-124">-Címke</span><span class="sxs-lookup"><span data-stu-id="5f8d6-124">-Tag</span></span>
<span data-ttu-id="5f8d6-125">Egy Hashtable, amely az erőforrás címkéit jelképezi.</span><span class="sxs-lookup"><span data-stu-id="5f8d6-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="5f8d6-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5f8d6-126">-Confirm</span></span>
<span data-ttu-id="5f8d6-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5f8d6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f8d6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f8d6-128">-WhatIf</span></span>
<span data-ttu-id="5f8d6-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5f8d6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f8d6-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f8d6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f8d6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f8d6-131">CommonParameters</span></span>
<span data-ttu-id="5f8d6-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f8d6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f8d6-133">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5f8d6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f8d6-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f8d6-134">INPUTS</span></span>

### <span data-ttu-id="5f8d6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5f8d6-135">System.String</span></span>

### <span data-ttu-id="5f8d6-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5f8d6-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5f8d6-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f8d6-137">OUTPUTS</span></span>

### <span data-ttu-id="5f8d6-138">Microsoft. Azure. commands. Network. models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5f8d6-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="5f8d6-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f8d6-139">NOTES</span></span>

## <span data-ttu-id="5f8d6-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f8d6-140">RELATED LINKS</span></span>
