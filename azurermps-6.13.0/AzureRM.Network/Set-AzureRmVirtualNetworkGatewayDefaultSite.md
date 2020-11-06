---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 9c0eec0f38929efe188d8ab0ba8e30d31a16b717
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494989"
---
# <span data-ttu-id="cff9f-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="cff9f-101">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="cff9f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cff9f-102">SYNOPSIS</span></span>
<span data-ttu-id="cff9f-103">A virtuális hálózati átjáró alapértelmezett webhelyének beállítása.</span><span class="sxs-lookup"><span data-stu-id="cff9f-103">Sets the default site for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cff9f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cff9f-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cff9f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cff9f-105">DESCRIPTION</span></span>
<span data-ttu-id="cff9f-106">A **set-AzureRmVirtualNetworkGatewayDefaultSite** parancsmag kényszerített bújtatási alapértelmezett webhelyet rendel egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="cff9f-106">The **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet assigns a forced tunneling default site to a virtual network gateway.</span></span>
<span data-ttu-id="cff9f-107">A kényszeres bújtatás segítségével átirányíthatja az internethez kötött forgalmat az Azure virtuális gépekről a helyszíni hálózatra; Ezzel a beállítással ellenőrizheti és naplózhatja a forgalmat, mielőtt felszabadítja.</span><span class="sxs-lookup"><span data-stu-id="cff9f-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="cff9f-108">A kényszeres bújtatást virtuális magánhálózati (VPN) bújtatási alagúton keresztül valósítják meg; Ehhez az alagúthoz egy alapértelmezett webhelynek kell lennie, egy helyi átjárót, ahol az összes Azure internetes forgalmat átirányítja.</span><span class="sxs-lookup"><span data-stu-id="cff9f-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="cff9f-109">A **set-AzureRmVirtualNetworkGatewayDefaultSite** lehetővé teszi az átjáróhoz rendelt alapértelmezett webhely módosítását.</span><span class="sxs-lookup"><span data-stu-id="cff9f-109">**Set-AzureRmVirtualNetworkGatewayDefaultSite** provides a way to change the default site assigned to a gateway.</span></span>

## <span data-ttu-id="cff9f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cff9f-110">EXAMPLES</span></span>

### <span data-ttu-id="cff9f-111">Példa 1: alapértelmezett webhely hozzárendelése virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="cff9f-111">Example 1: Assign a default site to a virtual network gateway</span></span>
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

<span data-ttu-id="cff9f-112">Ez a példa egy alapértelmezett webhelyet rendel el egy ContosoVirtualGateway nevű virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="cff9f-112">This example assigns a default site to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="cff9f-113">Az első parancs egy ContosoLocalGateway nevű helyi átjáróhoz hoz létre egy objektumot.</span><span class="sxs-lookup"><span data-stu-id="cff9f-113">The first command creates an object reference to a local gateway named ContosoLocalGateway.</span></span>
<span data-ttu-id="cff9f-114">A $LocalGateway nevű változóban tárolt objektum hivatkozása az alapértelmezett webhelyként konfigurálni kívánt átjárót jelenti.</span><span class="sxs-lookup"><span data-stu-id="cff9f-114">This object reference that is stored in the variable named $LocalGateway represents the gateway to be configured as the default site .</span></span>
<span data-ttu-id="cff9f-115">A második parancs Ezután létrehoz egy objektumot a virtuális hálózati átjárónak, és az eredményt az $VirtualGateway nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cff9f-115">The second command then creates an object reference to the virtual network gateway and stores the result in the variable named $VirtualGateway.</span></span>
<span data-ttu-id="cff9f-116">A harmadik parancs a **set-AzureRmVirtualNetworkGatewayDefaultSite** parancsmagot használva rendeli hozzá az alapértelmezett webhelyet a ContosoVirtualGateway-hoz.</span><span class="sxs-lookup"><span data-stu-id="cff9f-116">The third command uses the **Set-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet to assign the default site to ContosoVirtualGateway.</span></span>

## <span data-ttu-id="cff9f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cff9f-117">PARAMETERS</span></span>

### <span data-ttu-id="cff9f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff9f-118">-DefaultProfile</span></span>
<span data-ttu-id="cff9f-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cff9f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cff9f-120">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="cff9f-120">-GatewayDefaultSite</span></span>
<span data-ttu-id="cff9f-121">A megadott virtuális hálózat alapértelmezett webhelyének adja meg a helyi hálózati átjáróhoz tartozó objektum hivatkozását.</span><span class="sxs-lookup"><span data-stu-id="cff9f-121">Specifies an object reference to the local network gateway to be assigned as the default site for the specified virtual network.</span></span>
<span data-ttu-id="cff9f-122">A Get-AzureRmLocalNetworkGateway parancsmaggal egy helyi átjáróra mutató objektumra mutató hivatkozást is létrehozhat.</span><span class="sxs-lookup"><span data-stu-id="cff9f-122">You can use the Get-AzureRmLocalNetworkGateway cmdlet to create an object reference to a local gateway.</span></span>

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

### <span data-ttu-id="cff9f-123">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cff9f-123">-VirtualNetworkGateway</span></span>
<span data-ttu-id="cff9f-124">Annak a virtuális hálózati átjárónak az objektum hivatkozását adja meg, amelybe az alapértelmezett webhelyet hozzá szeretné rendelni.</span><span class="sxs-lookup"><span data-stu-id="cff9f-124">Specifies an object reference to the virtual network gateway where the default site will be assigned.</span></span>
<span data-ttu-id="cff9f-125">Létrehozhat egy objektumot a virtuális hálózati átjáróhoz a **Get-AzureRmVirtualNetworkGateway** , és megadhatja az átjáró nevét.</span><span class="sxs-lookup"><span data-stu-id="cff9f-125">You can create an object reference to a virtual network gateway by using the **Get-AzureRmVirtualNetworkGateway** and specifying the name of the gateway.</span></span>
<span data-ttu-id="cff9f-126">A változó $VirtualGateway ezután a *VirtualNetworkGateway* paraméter paraméterének értékeként használhatók:</span><span class="sxs-lookup"><span data-stu-id="cff9f-126">The variable $VirtualGateway can then be used as the parameter value for the *VirtualNetworkGateway* parameter:</span></span>

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

### <span data-ttu-id="cff9f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff9f-127">CommonParameters</span></span>
<span data-ttu-id="cff9f-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cff9f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff9f-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cff9f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff9f-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cff9f-130">INPUTS</span></span>

### <span data-ttu-id="cff9f-131">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cff9f-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="cff9f-132">Paraméterek: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cff9f-132">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="cff9f-133">Microsoft. Azure. commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cff9f-133">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="cff9f-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cff9f-134">OUTPUTS</span></span>

### <span data-ttu-id="cff9f-135">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cff9f-135">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="cff9f-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cff9f-136">NOTES</span></span>

## <span data-ttu-id="cff9f-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cff9f-137">RELATED LINKS</span></span>

[<span data-ttu-id="cff9f-138">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cff9f-138">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="cff9f-139">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cff9f-139">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="cff9f-140">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="cff9f-140">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


