---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158827"
---
# <span data-ttu-id="b54fc-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="b54fc-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="b54fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b54fc-102">SYNOPSIS</span></span>
<span data-ttu-id="b54fc-103">Beállítja egy virtuális hálózati átjáró alapértelmezett webhelyét.</span><span class="sxs-lookup"><span data-stu-id="b54fc-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="b54fc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b54fc-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b54fc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b54fc-105">DESCRIPTION</span></span>
<span data-ttu-id="b54fc-106">A **Set-AzVirtualNetworkGatewayDefaultSite** parancsmag egy kényszerített alagutas alapértelmezett webhelyet rendel egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b54fc-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="b54fc-107">A kényszerített átjárók használatával átirányíthatja az internetes forgalmat az Azure virtuális gépeiből a helyszíni hálózatba; ez lehetővé teszi a forgalom vizsgálatát és naplózását, mielőtt felengedi azt.</span><span class="sxs-lookup"><span data-stu-id="b54fc-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="b54fc-108">A kényszerített alagutaszás virtuális magánhálózati alagutat használ; Ehhez az átjáróhoz egy alapértelmezett webhelyre, egy helyi átjáróra van szükség, ahol az Összes Azure internetes forgalmat átirányítják.</span><span class="sxs-lookup"><span data-stu-id="b54fc-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="b54fc-109">**A Set-AzVirtualNetworkGatewayDefaultSite** segítségével módosíthatja az átjárókhoz rendelt alapértelmezett webhelyet.</span><span class="sxs-lookup"><span data-stu-id="b54fc-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="b54fc-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b54fc-110">EXAMPLES</span></span>

### <span data-ttu-id="b54fc-111">1. példa: Alapértelmezett webhely hozzárendelése virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="b54fc-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="b54fc-112">Ez a példa hozzárendel egy alapértelmezett webhelyet a ContosoVirtualGateway nevű virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b54fc-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="b54fc-113">Az első parancs létrehoz egy objektumhivatkozást a ContosoLocalGateway nevű helyi átjáróra.</span><span class="sxs-lookup"><span data-stu-id="b54fc-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="b54fc-114">Ez az objektumhivatkozás, amely a $LocalGateway nevű változóban van tárolva, az alapértelmezett webhelyként konfigurálni szükséges átjárót jelöli.</span><span class="sxs-lookup"><span data-stu-id="b54fc-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="b54fc-115">A második parancs ezután létrehoz egy objektumhivatkozást a virtuális hálózati átjáróra, és az eredményt a következő nevű változóban $VirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="b54fc-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="b54fc-116">A harmadik parancs a **Set-AzVirtualNetworkGatewayDefaultSite parancsmag** használatával rendeli hozzá az alapértelmezett webhelyet a ContosoVirtualGatewayhez.</span><span class="sxs-lookup"><span data-stu-id="b54fc-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="b54fc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b54fc-117">PARAMETERS</span></span>

### <span data-ttu-id="b54fc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b54fc-118">-DefaultProfile</span></span>
<span data-ttu-id="b54fc-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b54fc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b54fc-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="b54fc-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="b54fc-121">Egy objektumhivatkozást ad meg, amely a megadott virtuális hálózat alapértelmezett webhelyeként a helyi hálózati átjáróra hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="b54fc-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="b54fc-122">A Get-AzLocalNetworkGateway segítségével létrehozhat egy objektumhivatkozást egy helyi átjáróra.</span><span class="sxs-lookup"><span data-stu-id="b54fc-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b54fc-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b54fc-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="b54fc-124">Egy objektumhivatkozást ad meg arra a virtuális hálózati átjáróra, ahol az alapértelmezett webhely lesz hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="b54fc-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="b54fc-125">Virtuális hálózati átjáróra a **Get-AzVirtualNetworkGateway** használatával hozhat létre objektumhivatkozást, és megadhatja az átjáró nevét.</span><span class="sxs-lookup"><span data-stu-id="b54fc-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="b54fc-126">A $VirtualGateway használható paraméterértékként a *VirtualNetworkGateway* paraméterhez:</span><span class="sxs-lookup"><span data-stu-id="b54fc-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="b54fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b54fc-127">CommonParameters</span></span>
<span data-ttu-id="b54fc-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b54fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b54fc-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b54fc-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b54fc-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b54fc-130">INPUTS</span></span>

### <span data-ttu-id="b54fc-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b54fc-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="b54fc-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b54fc-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="b54fc-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b54fc-133">OUTPUTS</span></span>

### <span data-ttu-id="b54fc-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b54fc-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="b54fc-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b54fc-135">NOTES</span></span>

## <span data-ttu-id="b54fc-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b54fc-136">RELATED LINKS</span></span>

[<span data-ttu-id="b54fc-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b54fc-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="b54fc-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b54fc-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="b54fc-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="b54fc-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


