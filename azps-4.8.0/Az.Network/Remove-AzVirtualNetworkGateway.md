---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7708202630b5c7797d9ec3eda77475c82e1c358a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024574"
---
# <span data-ttu-id="d757e-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d757e-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="d757e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d757e-102">SYNOPSIS</span></span>
<span data-ttu-id="d757e-103">Virtuális hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="d757e-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="d757e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d757e-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d757e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d757e-105">DESCRIPTION</span></span>
<span data-ttu-id="d757e-106">A virtuális hálózati átjáró az az objektum, amely az Azure-átjárót jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d757e-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="d757e-107">A **Get-AzVirtualNetworkGateway** parancsmag az Azure-átjáró objektumát adja eredményül a név és az erőforrás csoport neve alapján.</span><span class="sxs-lookup"><span data-stu-id="d757e-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="d757e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d757e-108">EXAMPLES</span></span>

### <span data-ttu-id="d757e-109">Példa 1: virtuális hálózati átjáró törlése</span><span class="sxs-lookup"><span data-stu-id="d757e-109">Example 1: Delete a Virtual Network Gateway</span></span>
```powershell
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="d757e-110">Törli a virtuális hálózati átjáró objektumát a "myGateway" nevű erőforrás-csoport "myRG" Megjegyzés: először törölnie kell a virtuális hálózati átjáróval való összes kapcsolatot a **Remove-AzVirtualNetworkGatewayConnection** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="d757e-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="d757e-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d757e-111">PARAMETERS</span></span>

### <span data-ttu-id="d757e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d757e-112">-AsJob</span></span>
<span data-ttu-id="d757e-113">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d757e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d757e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d757e-114">-DefaultProfile</span></span>
<span data-ttu-id="d757e-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d757e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d757e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d757e-116">-Force</span></span>
<span data-ttu-id="d757e-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="d757e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d757e-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d757e-118">-Name</span></span>
<span data-ttu-id="d757e-119">Annak a virtuális hálózati átjárónak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="d757e-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d757e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d757e-120">-PassThru</span></span>
<span data-ttu-id="d757e-121">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="d757e-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d757e-122">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="d757e-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d757e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d757e-123">-ResourceGroupName</span></span>
<span data-ttu-id="d757e-124">A virtuális hálózati átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d757e-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="d757e-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d757e-125">-Confirm</span></span>
<span data-ttu-id="d757e-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d757e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d757e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d757e-127">-WhatIf</span></span>
<span data-ttu-id="d757e-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d757e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d757e-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d757e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d757e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d757e-130">CommonParameters</span></span>
<span data-ttu-id="d757e-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d757e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d757e-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d757e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d757e-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d757e-133">INPUTS</span></span>

### <span data-ttu-id="d757e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d757e-134">System.String</span></span>

## <span data-ttu-id="d757e-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d757e-135">OUTPUTS</span></span>

### <span data-ttu-id="d757e-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d757e-136">System.Boolean</span></span>

## <span data-ttu-id="d757e-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d757e-137">NOTES</span></span>

## <span data-ttu-id="d757e-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d757e-138">RELATED LINKS</span></span>

[<span data-ttu-id="d757e-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d757e-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d757e-140">Új – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d757e-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d757e-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d757e-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d757e-142">Átméretezés-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d757e-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d757e-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d757e-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
