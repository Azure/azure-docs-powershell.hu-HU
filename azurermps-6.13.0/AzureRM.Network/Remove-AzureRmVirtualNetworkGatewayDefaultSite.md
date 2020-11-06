---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: a2c6c51a1f9f22130436e7d0a0d5fd888bccfb99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495012"
---
# <span data-ttu-id="d5dd0-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d5dd0-101">Remove-AzureRmVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="d5dd0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5dd0-102">SYNOPSIS</span></span>
<span data-ttu-id="d5dd0-103">Eltávolítja az alapértelmezett webhelyet egy virtuális hálózati átjáróról.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-103">Removes the default site from a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5dd0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5dd0-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5dd0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5dd0-105">DESCRIPTION</span></span>
<span data-ttu-id="d5dd0-106">A **Remove-AzureRmVirtualNetworkGatewayDefaultSite** parancsmag eltávolítja a kényszerített bújtatási alapértelmezett webhelyet egy virtuális hálózati átjáróról.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-106">The **Remove-AzureRmVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="d5dd0-107">A kényszeres bújtatás segítségével átirányíthatja az internethez kötött forgalmat az Azure virtuális gépekről a helyszíni hálózatra; Ezzel a beállítással ellenőrizheti és naplózhatja a forgalmat, mielőtt felszabadítja.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="d5dd0-108">A kényszeres bújtatást virtuális magánhálózati (VPN) bújtatási alagúton keresztül valósítják meg; Ehhez az alagúthoz egy alapértelmezett webhelynek kell lennie, egy helyi átjárót, ahol az összes Azure internetes forgalmat átirányítja.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="d5dd0-109">**Eltávolítás – a AzureRmVirtualNetworkGatewayDefaultSite** eltávolítja az átjáróhoz rendelt alapértelmezett webhelyet.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-109">**Remove-AzureRmVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="d5dd0-110">Ha ezt a lehetőséget választja, akkor Set-AzureRmVirtualNetworkGatewayDefaultSite kell használnia egy új alapértelmezett webhely hozzárendelését ahhoz, hogy az átjáró használható legyen a kényszeres bújtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-110">If you do this you will need to use Set-AzureRmVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="d5dd0-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d5dd0-111">EXAMPLES</span></span>

### <span data-ttu-id="d5dd0-112">1. példa: a virtuális hálózati átjáróhoz rendelt alapértelmezett webhely eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d5dd0-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="d5dd0-113">Ez a példa eltávolítja a ContosoVirtualGateway nevű virtuális hálózati átjáróhoz jelenleg hozzárendelt alapértelmezett webhelyet.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="d5dd0-114">Az első parancs a **Get-AzureRmVirtualNetworkGateway** használatával hoz létre objektumot az átjáróhoz; Ez az objektum hivatkozás a $Gateway nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-114">The first command uses **Get-AzureRmVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="d5dd0-115">A második parancs ezután eltávolítja a **Remove-AzureRmVirtualNetworkGatewayDefaultSite** az átjáróhoz rendelt alapértelmezett webhely eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-115">The second command then uses **Remove-AzureRmVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="d5dd0-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5dd0-116">PARAMETERS</span></span>

### <span data-ttu-id="d5dd0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5dd0-117">-DefaultProfile</span></span>
<span data-ttu-id="d5dd0-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5dd0-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5dd0-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="d5dd0-120">Az eltávolítandó alapértelmezett webhelyt tartalmazó virtuális hálózati átjáróhoz tartozó objektum hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="d5dd0-121">A virtuális hálózati átjáróhoz az Get-AzureRmVirtualNetworkGateway használatával hozhat létre objektum-hivatkozást, és megadhatja az átjáró nevét.</span><span class="sxs-lookup"><span data-stu-id="d5dd0-121">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="d5dd0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5dd0-122">CommonParameters</span></span>
<span data-ttu-id="d5dd0-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5dd0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5dd0-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5dd0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5dd0-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5dd0-125">INPUTS</span></span>

### <span data-ttu-id="d5dd0-126">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5dd0-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="d5dd0-127">Paraméterek: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d5dd0-127">Parameters: VirtualNetworkGateway (ByValue)</span></span>

## <span data-ttu-id="d5dd0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5dd0-128">OUTPUTS</span></span>

### <span data-ttu-id="d5dd0-129">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5dd0-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d5dd0-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5dd0-130">NOTES</span></span>

## <span data-ttu-id="d5dd0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5dd0-131">RELATED LINKS</span></span>

[<span data-ttu-id="d5dd0-132">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d5dd0-132">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="d5dd0-133">Set-AzureRmVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d5dd0-133">Set-AzureRmVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


