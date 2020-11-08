---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a4be0aed365517e1ae3ae11155f82ea097db309a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025130"
---
# <span data-ttu-id="178f1-101">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="178f1-101">Set-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="178f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="178f1-102">SYNOPSIS</span></span>
<span data-ttu-id="178f1-103">A virtuális hálózati átjáró alapértelmezett webhelyének beállítása.</span><span class="sxs-lookup"><span data-stu-id="178f1-103">Sets the default site for a virtual network gateway.</span></span>

## <span data-ttu-id="178f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="178f1-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="178f1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="178f1-105">DESCRIPTION</span></span>
<span data-ttu-id="178f1-106">A **set-AzVirtualNetworkGatewayDefaultSite** parancsmag kényszerített bújtatási alapértelmezett webhelyet rendel egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="178f1-106">The **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="178f1-107">A kényszeres bújtatás segítségével átirányíthatja az internethez kötött forgalmat az Azure virtuális gépekről a helyszíni hálózatra; Ezzel a beállítással ellenőrizheti és naplózhatja a forgalmat, mielőtt felszabadítja.</span><span class="sxs-lookup"><span data-stu-id="178f1-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="178f1-108">A kényszeres bújtatást virtuális magánhálózati (VPN) bújtatási alagúton keresztül valósítják meg; Ehhez az alagúthoz egy alapértelmezett webhelynek kell lennie, egy helyi átjárót, ahol az összes Azure internetes forgalmat átirányítja.</span><span class="sxs-lookup"><span data-stu-id="178f1-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="178f1-109">A **set-AzVirtualNetworkGatewayDefaultSite** lehetővé teszi az átjáróhoz rendelt alapértelmezett webhely módosítását.</span><span class="sxs-lookup"><span data-stu-id="178f1-109">**Set-AzVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="178f1-110">Példák</span><span class="sxs-lookup"><span data-stu-id="178f1-110">EXAMPLES</span></span>

### <span data-ttu-id="178f1-111">Példa 1: alapértelmezett webhely hozzárendelése virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="178f1-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="178f1-112">Ez a példa egy alapértelmezett webhelyet rendel el egy ContosoVirtualGateway nevű virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="178f1-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="178f1-113">Az első parancs egy ContosoLocalGateway nevű helyi átjáróhoz hoz létre egy objektumot.</span><span class="sxs-lookup"><span data-stu-id="178f1-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="178f1-114">A $LocalGateway nevű változóban tárolt objektum hivatkozása az alapértelmezett webhelyként konfigurálni kívánt átjárót jelenti.</span><span class="sxs-lookup"><span data-stu-id="178f1-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="178f1-115">A második parancs Ezután létrehoz egy objektumot a virtuális hálózati átjárónak, és az eredményt az $VirtualGateway nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="178f1-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="178f1-116">A harmadik parancs a **set-AzVirtualNetworkGatewayDefaultSite** parancsmagot használva rendeli hozzá az alapértelmezett webhelyet a ContosoVirtualGateway-hoz.</span><span class="sxs-lookup"><span data-stu-id="178f1-116">The third command uses the **Set-AzVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="178f1-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="178f1-117">PARAMETERS</span></span>

### <span data-ttu-id="178f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178f1-118">-DefaultProfile</span></span>
<span data-ttu-id="178f1-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="178f1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="178f1-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="178f1-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="178f1-121">A megadott virtuális hálózat alapértelmezett webhelyének adja meg a helyi hálózati átjáróhoz tartozó objektum hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="178f1-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="178f1-122">A Get-AzLocalNetworkGateway parancsmaggal egy helyi átjáróra mutató objektumra mutató hivatkozást is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="178f1-122">You can use the Get-AzLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

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

### <span data-ttu-id="178f1-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="178f1-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="178f1-124">Annak a virtuális hálózati átjárónak az objektum hivatkozását adja meg, amelybe az alapértelmezett webhelyet hozzá szeretné rendelni.</span><span class="sxs-lookup"><span data-stu-id="178f1-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="178f1-125">Létrehozhat egy objektumot a virtuális hálózati átjáróhoz a **Get-AzVirtualNetworkGateway** , és megadhatja az átjáró nevét.</span><span class="sxs-lookup"><span data-stu-id="178f1-125">You can create an object reference to a virtual network gateway by using the **Get-AzVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="178f1-126">A változó $VirtualGateway ezután a *VirtualNetworkGateway* paraméter paraméterének értékeként használhatók:</span><span class="sxs-lookup"><span data-stu-id="178f1-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="178f1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178f1-127">CommonParameters</span></span>
<span data-ttu-id="178f1-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="178f1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178f1-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="178f1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178f1-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="178f1-130">INPUTS</span></span>

### <span data-ttu-id="178f1-131">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="178f1-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="178f1-132">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="178f1-132">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="178f1-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="178f1-133">OUTPUTS</span></span>

### <span data-ttu-id="178f1-134">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="178f1-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="178f1-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="178f1-135">NOTES</span></span>

## <span data-ttu-id="178f1-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="178f1-136">RELATED LINKS</span></span>

[<span data-ttu-id="178f1-137">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="178f1-137">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="178f1-138">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="178f1-138">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="178f1-139">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="178f1-139">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzVirtualNetworkGatewayDefaultSite.md)


