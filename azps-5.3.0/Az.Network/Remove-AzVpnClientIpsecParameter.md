---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientIpsecParameter.md
ms.openlocfilehash: cee8d5d1ca76fbf206b4695661cc8f452052e62c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98481176"
---
# <span data-ttu-id="cb13c-101">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cb13c-101">Remove-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="cb13c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb13c-102">SYNOPSIS</span></span>
<span data-ttu-id="cb13c-103">Eltávolítja a Virtuális hálózati átjáró erőforráshoz beállított egyéni IPsec-házirendet.</span><span class="sxs-lookup"><span data-stu-id="cb13c-103">Removes Vpn custom ipsec policy set on Virtual Network Gateway resource.</span></span>

## <span data-ttu-id="cb13c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cb13c-104">SYNTAX</span></span>

### <span data-ttu-id="cb13c-105">ByFactoryName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb13c-105">ByFactoryName (Default)</span></span>
```
Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb13c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cb13c-106">ByFactoryObject</span></span>
```
Remove-AzVpnClientIpsecParameter -InputObject <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb13c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cb13c-107">ByResourceId</span></span>
```
Remove-AzVpnClientIpsecParameter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb13c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cb13c-108">DESCRIPTION</span></span>
<span data-ttu-id="cb13c-109">A virtuális hálózati átjáró az azure-beli átjárót képviselő objektum.</span><span class="sxs-lookup"><span data-stu-id="cb13c-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="cb13c-110">A **Remove-AzVpnClientIpsecParameter** parancsmag eltávolítja a virtuális hálózati átjárón beállított egyéni IPsec-paramétereket, amelyek a VirtualNetworkGateway neve és az Erőforráscsoport neve alapján beállítja az alapértelmezett vpn ipsec-házirendet VPN-átjárón.</span><span class="sxs-lookup"><span data-stu-id="cb13c-110">The **Remove-AzVpnClientIpsecParameter** cmdlet removes the vpn custom ipsec parameters set on your Virtual Network Gateway, which in turn sets default vpn ipsec policy on VPN gateway based on VirtualNetworkGateway Name and Resource Group Name passed.</span></span>

## <span data-ttu-id="cb13c-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cb13c-111">EXAMPLES</span></span>

### <span data-ttu-id="cb13c-112">1. példa: A virtuális hálózati átjáróban beállított VPN ipsec-paraméterek törlése</span><span class="sxs-lookup"><span data-stu-id="cb13c-112">Example 1: Deletes the set vpn ipsec parameters set on the Virtual Network Gateway</span></span>
```powershell
PS C:\> $delete = Remove-AzVpnClientIpsecParameter -VirtualNetworkGatewayName myGateway -ResourceGroupName myRG
```

<span data-ttu-id="cb13c-113">Törli a virtuális hálózati átjáróban a "myGateway" nevű vpn egyéni ipsec-paramétereket a "myRG" erőforráscsoporton belül.</span><span class="sxs-lookup"><span data-stu-id="cb13c-113">Deletes the vpn custom ipsec parameters set on your Virtual Network Gateway with the name "myGateway" within the resource group "myRG".</span></span> <span data-ttu-id="cb13c-114">Ez a parancs olyan bool objektumot ad vissza, amely azt mutatja, hogy az eltávolítás sikeres vagy sikertelen volt-e.</span><span class="sxs-lookup"><span data-stu-id="cb13c-114">This command returns bool object showing if removal was successful or failed.</span></span>
<span data-ttu-id="cb13c-115">Megjegyzés: Ez azt eredményezi, hogy a virtuális hálózat átjárója alapértelmezett vpn ipsec-házirendet ad meg.</span><span class="sxs-lookup"><span data-stu-id="cb13c-115">Note: This will result in setting default vpn ipsec policy on your Virtual Network Gateway.</span></span>

## <span data-ttu-id="cb13c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb13c-116">PARAMETERS</span></span>

### <span data-ttu-id="cb13c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb13c-117">-DefaultProfile</span></span>
<span data-ttu-id="cb13c-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb13c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb13c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb13c-119">-InputObject</span></span>
<span data-ttu-id="cb13c-120">A virtuális hálózati átjáró objektum</span><span class="sxs-lookup"><span data-stu-id="cb13c-120">The virtual network gateway object</span></span>

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

### <span data-ttu-id="cb13c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb13c-121">-ResourceGroupName</span></span>
<span data-ttu-id="cb13c-122">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cb13c-122">The resource group name.</span></span>

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

### <span data-ttu-id="cb13c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb13c-123">-ResourceId</span></span>
<span data-ttu-id="cb13c-124">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="cb13c-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cb13c-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="cb13c-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="cb13c-126">A virtuális hálózati átjáró neve.</span><span class="sxs-lookup"><span data-stu-id="cb13c-126">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="cb13c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb13c-127">-Confirm</span></span>
<span data-ttu-id="cb13c-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cb13c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb13c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb13c-129">-WhatIf</span></span>
<span data-ttu-id="cb13c-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cb13c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb13c-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cb13c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb13c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb13c-132">CommonParameters</span></span>
<span data-ttu-id="cb13c-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb13c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb13c-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb13c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb13c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb13c-135">INPUTS</span></span>

### <span data-ttu-id="cb13c-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cb13c-136">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="cb13c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="cb13c-137">System.String</span></span>

## <span data-ttu-id="cb13c-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb13c-138">OUTPUTS</span></span>

### <span data-ttu-id="cb13c-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb13c-139">System.Boolean</span></span>

## <span data-ttu-id="cb13c-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cb13c-140">NOTES</span></span>

## <span data-ttu-id="cb13c-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb13c-141">RELATED LINKS</span></span>

[<span data-ttu-id="cb13c-142">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cb13c-142">Get-AzVpnClientIpsecParameter</span></span>](./Get-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="cb13c-143">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cb13c-143">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="cb13c-144">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cb13c-144">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
