---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7708202630b5c7797d9ec3eda77475c82e1c358a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158946"
---
# <span data-ttu-id="c0003-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0003-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="c0003-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0003-102">SYNOPSIS</span></span>
<span data-ttu-id="c0003-103">Virtuális hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="c0003-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="c0003-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c0003-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0003-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c0003-105">DESCRIPTION</span></span>
<span data-ttu-id="c0003-106">A virtuális hálózati átjáró az azure-beli átjárót képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="c0003-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="c0003-107">A **Get-AzVirtualNetworkGateway** parancsmag az Azure-ban található átjáró objektumát adja vissza a név és az erőforráscsoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="c0003-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="c0003-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c0003-108">EXAMPLES</span></span>

### <span data-ttu-id="c0003-109">1. példa: Virtuális hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="c0003-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="c0003-110">Törli a virtuális hálózati átjáró "myGateway" nevű objektumát a "myRG" erőforráscsoportban: A **Remove-AzVirtualNetworkGatewayConnection** parancsmaggal először törölnie kell a virtuális hálózati átjáróval létesített összes kapcsolatot.</span><span class="sxs-lookup"><span data-stu-id="c0003-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="c0003-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0003-111">PARAMETERS</span></span>

### <span data-ttu-id="c0003-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0003-112">-AsJob</span></span>
<span data-ttu-id="c0003-113">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="c0003-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0003-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0003-114">-DefaultProfile</span></span>
<span data-ttu-id="c0003-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c0003-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0003-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c0003-116">-Force</span></span>
<span data-ttu-id="c0003-117">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="c0003-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0003-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c0003-118">-Name</span></span>
<span data-ttu-id="c0003-119">A parancsmag által eltávolított virtuális hálózati átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="c0003-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c0003-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0003-120">-PassThru</span></span>
<span data-ttu-id="c0003-121">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="c0003-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c0003-122">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="c0003-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c0003-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0003-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0003-124">A virtuális hálózati átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0003-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="c0003-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0003-125">-Confirm</span></span>
<span data-ttu-id="c0003-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c0003-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0003-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0003-127">-WhatIf</span></span>
<span data-ttu-id="c0003-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c0003-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0003-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c0003-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0003-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0003-130">CommonParameters</span></span>
<span data-ttu-id="c0003-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0003-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0003-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0003-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0003-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0003-133">INPUTS</span></span>

### <span data-ttu-id="c0003-134">System.String</span><span class="sxs-lookup"><span data-stu-id="c0003-134">System.String</span></span>

## <span data-ttu-id="c0003-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0003-135">OUTPUTS</span></span>

### <span data-ttu-id="c0003-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c0003-136">System.Boolean</span></span>

## <span data-ttu-id="c0003-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c0003-137">NOTES</span></span>

## <span data-ttu-id="c0003-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0003-138">RELATED LINKS</span></span>

[<span data-ttu-id="c0003-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0003-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c0003-140">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0003-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c0003-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0003-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c0003-142">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0003-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="c0003-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c0003-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
