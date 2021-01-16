---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: 777e03a570f3915d6e0ebe4cbb5c84f9c1824120
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385250"
---
# <span data-ttu-id="9cd46-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9cd46-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="9cd46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cd46-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd46-103">Virtuális hálózat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9cd46-103">Removes a virtual network.</span></span>

## <span data-ttu-id="9cd46-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9cd46-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cd46-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9cd46-105">DESCRIPTION</span></span>
<span data-ttu-id="9cd46-106">A **Remove-AzVirtualNetwork** parancsmag eltávolít egy Azure virtuális hálózatot.</span><span class="sxs-lookup"><span data-stu-id="9cd46-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="9cd46-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9cd46-107">EXAMPLES</span></span>

### <span data-ttu-id="9cd46-108">1: Virtuális hálózat létrehozása és törlése</span><span class="sxs-lookup"><span data-stu-id="9cd46-108">1: Create and delete a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="9cd46-109">Ez a példa létrehoz egy virtuális hálózatot egy erőforráscsoportban, majd azonnal törli azt.</span><span class="sxs-lookup"><span data-stu-id="9cd46-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="9cd46-110">A -Force jelölővel elrejtheti a parancssort a virtuális hálózat törlésekor.</span><span class="sxs-lookup"><span data-stu-id="9cd46-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="9cd46-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cd46-111">PARAMETERS</span></span>

### <span data-ttu-id="9cd46-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cd46-112">-AsJob</span></span>
<span data-ttu-id="9cd46-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9cd46-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9cd46-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd46-114">-DefaultProfile</span></span>
<span data-ttu-id="9cd46-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9cd46-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cd46-116">-Force</span><span class="sxs-lookup"><span data-stu-id="9cd46-116">-Force</span></span>
<span data-ttu-id="9cd46-117">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="9cd46-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9cd46-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9cd46-118">-Name</span></span>
<span data-ttu-id="9cd46-119">A parancsmag által eltávolított virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9cd46-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9cd46-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cd46-120">-PassThru</span></span>
<span data-ttu-id="9cd46-121">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="9cd46-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9cd46-122">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="9cd46-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9cd46-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cd46-123">-ResourceGroupName</span></span>
<span data-ttu-id="9cd46-124">Annak az erőforráscsoportnak a nevét adja meg, amely a parancsmag által eltávolított virtuális hálózatot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="9cd46-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9cd46-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cd46-125">-Confirm</span></span>
<span data-ttu-id="9cd46-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9cd46-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd46-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cd46-127">-WhatIf</span></span>
<span data-ttu-id="9cd46-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9cd46-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cd46-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9cd46-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cd46-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd46-130">CommonParameters</span></span>
<span data-ttu-id="9cd46-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cd46-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd46-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cd46-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd46-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9cd46-133">INPUTS</span></span>

### <span data-ttu-id="9cd46-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9cd46-134">System.String</span></span>

## <span data-ttu-id="9cd46-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9cd46-135">OUTPUTS</span></span>

### <span data-ttu-id="9cd46-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9cd46-136">System.Boolean</span></span>

## <span data-ttu-id="9cd46-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9cd46-137">NOTES</span></span>

## <span data-ttu-id="9cd46-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9cd46-138">RELATED LINKS</span></span>

[<span data-ttu-id="9cd46-139">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9cd46-139">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="9cd46-140">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9cd46-140">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="9cd46-141">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9cd46-141">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


