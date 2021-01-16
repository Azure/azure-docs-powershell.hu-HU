---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 288812137887e4fc22308bba56a3fbdbeeb28c85
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351414"
---
# <span data-ttu-id="7fb9a-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7fb9a-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="7fb9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fb9a-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb9a-103">Eltávolítja az alapértelmezett webhelyet egy virtuális hálózati átjáróból.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="7fb9a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7fb9a-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fb9a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7fb9a-105">DESCRIPTION</span></span>
<span data-ttu-id="7fb9a-106">A **Remove-AzVirtualNetworkGatewayDefaultSite** parancsmag eltávolítja a virtuális hálózati átjáróból az alapértelmezett kényszerített átjárót.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="7fb9a-107">A kényszerített átjárók használatával átirányíthatja az internetes forgalmat az Azure virtuális gépeiből a helyszíni hálózatba; ez lehetővé teszi a forgalom vizsgálatát és naplózását, mielőtt felengedi azt.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="7fb9a-108">A kényszerített alagutaszás virtuális magánhálózati alagutat használ; Ehhez az átjáróhoz egy alapértelmezett webhelyre, egy helyi átjáróra van szükség, ahol az Összes Azure internetes forgalmat átirányítják.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="7fb9a-109">**A Remove-AzVirtualNetworkGatewayDefaultSite** eltávolítja az átjárókhoz rendelt alapértelmezett webhelyet.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="7fb9a-110">Ha ezt a beállítást használja, a Set-AzVirtualNetworkGatewayDefaultSite kell hozzárendelni egy új alapértelmezett webhelyet, mielőtt az átjárót használva kényszerített átjárót használna.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="7fb9a-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7fb9a-111">EXAMPLES</span></span>

### <span data-ttu-id="7fb9a-112">1. példa: Virtuális hálózati átjáróhoz rendelt alapértelmezett webhely eltávolítása</span><span class="sxs-lookup"><span data-stu-id="7fb9a-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="7fb9a-113">Ez a példa eltávolítja a ContosoVirtualGateway nevű virtuális hálózati átjáróhoz jelenleg hozzárendelt alapértelmezett webhelyet.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="7fb9a-114">Az első parancs **a Get-AzVirtualNetworkGateway** segítségével hoz létre objektumhivatkozást az átjáróra; Ezt az objektumhivatkozást egy $Gateway.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="7fb9a-115">A második parancs ezután **a Remove-AzVirtualNetworkGatewayDefaultSite** paranccsal eltávolítja az átjáróhoz társított alapértelmezett webhelyet.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="7fb9a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fb9a-116">PARAMETERS</span></span>

### <span data-ttu-id="7fb9a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb9a-117">-DefaultProfile</span></span>
<span data-ttu-id="7fb9a-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fb9a-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7fb9a-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="7fb9a-120">Egy objektumhivatkozást ad meg a virtuális hálózati átjáróra, amely az alapértelmezett eltávolítható webhelyet tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="7fb9a-121">Virtuális hálózati átjáróra való hivatkozás létrehozásához használja a Get-AzVirtualNetworkGateway és adja meg az átjáró nevét.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb9a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb9a-122">CommonParameters</span></span>
<span data-ttu-id="7fb9a-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb9a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb9a-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fb9a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb9a-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7fb9a-125">INPUTS</span></span>

### <span data-ttu-id="7fb9a-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7fb9a-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7fb9a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fb9a-127">OUTPUTS</span></span>

### <span data-ttu-id="7fb9a-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7fb9a-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7fb9a-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7fb9a-129">NOTES</span></span>

## <span data-ttu-id="7fb9a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fb9a-130">RELATED LINKS</span></span>

[<span data-ttu-id="7fb9a-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7fb9a-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="7fb9a-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7fb9a-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)


