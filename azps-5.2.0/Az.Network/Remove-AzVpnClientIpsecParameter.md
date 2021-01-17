---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: cee8d5d1ca76fbf206b4695661cc8f452052e62c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342245"
---
# <span data-ttu-id="c33b1-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="c33b1-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="c33b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c33b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c33b1-103">Eltávolítja a Virtuális hálózati átjáró erőforráshoz beállított egyéni IPsec-házirendet.</span><span class="sxs-lookup"><span data-stu-id="c33b1-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="c33b1-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c33b1-104">SYNTAX</span></span>

### <span data-ttu-id="c33b1-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c33b1-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c33b1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c33b1-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c33b1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c33b1-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c33b1-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c33b1-108">DESCRIPTION</span></span>
<span data-ttu-id="c33b1-109">A virtuális hálózati átjáró az azure-beli átjárót képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="c33b1-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="c33b1-110">A **Remove-AzVpnClientIpsecParameter** parancsmag eltávolítja a virtuális hálózati átjárón beállított vpn-egyéni ipsec-paramétereket, így a VirtualNetworkGateway neve és az Erőforráscsoport neve alapján vpn-ipsec-házirendet állít be VPN-átjárón.</span><span class="sxs-lookup"><span data-stu-id="c33b1-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="c33b1-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c33b1-111">EXAMPLES</span></span>

### <span data-ttu-id="c33b1-112">1. példa: A virtuális hálózati átjárón beállított VPN ipsec-paraméterek törlése</span><span class="sxs-lookup"><span data-stu-id="c33b1-112">Example 1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```powershell
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="c33b1-113">Törli a virtuális hálózati átjáróban a "myGateway" nevű vpn egyéni ipsec-paramétereket a "myRG" erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="c33b1-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="c33b1-114">Ez a parancs olyan bool objektumot ad vissza, amely azt mutatja, hogy az eltávolítás sikeres vagy sikertelen volt-e.</span><span class="sxs-lookup"><span data-stu-id="c33b1-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="c33b1-115">Megjegyzés: Ez azt eredményezi, hogy a virtuális hálózat átjárója alapértelmezett vpn ipsec-házirendet ad meg.</span><span class="sxs-lookup"><span data-stu-id="c33b1-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="c33b1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c33b1-116">PARAMETERS</span></span>

### <span data-ttu-id="c33b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c33b1-117">-DefaultProfile</span></span>
<span data-ttu-id="c33b1-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c33b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c33b1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c33b1-119">-InputObject</span></span>
<span data-ttu-id="c33b1-120">A virtuális hálózati átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="c33b1-120">The virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c33b1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c33b1-121">-ResourceGroupName</span></span>
<span data-ttu-id="c33b1-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c33b1-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c33b1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c33b1-123">-ResourceId</span></span>
<span data-ttu-id="c33b1-124">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="c33b1-124">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c33b1-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="c33b1-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="c33b1-126">A virtuális hálózati átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="c33b1-126">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c33b1-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c33b1-127">-Confirm</span></span>
<span data-ttu-id="c33b1-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c33b1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c33b1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c33b1-129">-WhatIf</span></span>
<span data-ttu-id="c33b1-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c33b1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c33b1-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c33b1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c33b1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c33b1-132">CommonParameters</span></span>
<span data-ttu-id="c33b1-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c33b1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c33b1-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c33b1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c33b1-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c33b1-135">INPUTS</span></span>

### <span data-ttu-id="c33b1-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c33b1-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="c33b1-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c33b1-137">System.String</span></span>

## <span data-ttu-id="c33b1-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c33b1-138">OUTPUTS</span></span>

### <span data-ttu-id="c33b1-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c33b1-139">System.Boolean</span></span>

## <span data-ttu-id="c33b1-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c33b1-140">NOTES</span></span>

## <span data-ttu-id="c33b1-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c33b1-141">RELATED LINKS</span></span>

[<span data-ttu-id="c33b1-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="c33b1-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="c33b1-143">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="c33b1-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="c33b1-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="c33b1-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
