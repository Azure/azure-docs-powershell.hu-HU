---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewaydefaultsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 9516d132f2c6b26c162dcbb8abc742e69dccfc14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670106"
---
# <span data-ttu-id="d963f-101">Remove-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d963f-101">Remove-AzVirtualNetworkGatewayDefaultSite</span></span>

## <span data-ttu-id="d963f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d963f-102">SYNOPSIS</span></span>
<span data-ttu-id="d963f-103">Eltávolítja az alapértelmezett webhelyet egy virtuális hálózati átjáróról.</span><span class="sxs-lookup"><span data-stu-id="d963f-103">Removes the default site from a virtual network gateway.</span></span>

## <span data-ttu-id="d963f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d963f-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d963f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d963f-105">DESCRIPTION</span></span>
<span data-ttu-id="d963f-106">A **Remove-AzVirtualNetworkGatewayDefaultSite** parancsmag eltávolítja a kényszerített bújtatási alapértelmezett webhelyet egy virtuális hálózati átjáróról.</span><span class="sxs-lookup"><span data-stu-id="d963f-106">The **Remove-AzVirtualNetworkGatewayDefaultSite** cmdlet removes the forced tunneling default site from a virtual network gateway.</span></span>
<span data-ttu-id="d963f-107">A kényszeres bújtatás segítségével átirányíthatja az internethez kötött forgalmat az Azure virtuális gépekről a helyszíni hálózatra; Ezzel a beállítással ellenőrizheti és naplózhatja a forgalmat, mielőtt felszabadítja.</span><span class="sxs-lookup"><span data-stu-id="d963f-107">Forced tunneling provides a way for you to redirect Internet-bound traffic from Azure virtual machines to your on-premises network; this enables you to inspect and audit traffic before releasing it.</span></span>
<span data-ttu-id="d963f-108">A kényszeres bújtatást virtuális magánhálózati (VPN) bújtatási alagúton keresztül valósítják meg; Ehhez az alagúthoz egy alapértelmezett webhelynek kell lennie, egy helyi átjárót, ahol az összes Azure internetes forgalmat átirányítja.</span><span class="sxs-lookup"><span data-stu-id="d963f-108">Forced tunneling is carried out by using a virtual private network (VPN) tunnel; this tunnel requires a default site, a local gateway where all the Azure Internet-bound traffic is redirected.</span></span>
<span data-ttu-id="d963f-109">**Eltávolítás – a AzVirtualNetworkGatewayDefaultSite** eltávolítja az átjáróhoz rendelt alapértelmezett webhelyet.</span><span class="sxs-lookup"><span data-stu-id="d963f-109">**Remove-AzVirtualNetworkGatewayDefaultSite** removes the default site assigned to a gateway.</span></span>
<span data-ttu-id="d963f-110">Ha ezt a lehetőséget választja, akkor Set-AzVirtualNetworkGatewayDefaultSite kell használnia egy új alapértelmezett webhely hozzárendelését ahhoz, hogy az átjáró használható legyen a kényszeres bújtatáshoz.</span><span class="sxs-lookup"><span data-stu-id="d963f-110">If you do this you will need to use Set-AzVirtualNetworkGatewayDefaultSite to assign a new default site before the gateway can be used for forced tunneling.</span></span>

## <span data-ttu-id="d963f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="d963f-111">EXAMPLES</span></span>

### <span data-ttu-id="d963f-112">1. példa: a virtuális hálózati átjáróhoz rendelt alapértelmezett webhely eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d963f-112">Example 1: Remove the default site assigned to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway $Gateway
```

<span data-ttu-id="d963f-113">Ez a példa eltávolítja a ContosoVirtualGateway nevű virtuális hálózati átjáróhoz jelenleg hozzárendelt alapértelmezett webhelyet.</span><span class="sxs-lookup"><span data-stu-id="d963f-113">This example removes the default site currently assigned to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="d963f-114">Az első parancs a **Get-AzVirtualNetworkGateway** használatával hoz létre objektumot az átjáróhoz; Ez az objektum hivatkozás a $Gateway nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="d963f-114">The first command uses **Get-AzVirtualNetworkGateway** to create an object reference to the gateway; this object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="d963f-115">A második parancs ezután eltávolítja a **Remove-AzVirtualNetworkGatewayDefaultSite** az átjáróhoz rendelt alapértelmezett webhely eltávolításához.</span><span class="sxs-lookup"><span data-stu-id="d963f-115">The second command then uses **Remove-AzVirtualNetworkGatewayDefaultSite** to remove the default site assigned to that gateway.</span></span>

## <span data-ttu-id="d963f-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d963f-116">PARAMETERS</span></span>

### <span data-ttu-id="d963f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d963f-117">-DefaultProfile</span></span>
<span data-ttu-id="d963f-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d963f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d963f-119">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d963f-119">-VirtualNetworkGateway</span></span>
<span data-ttu-id="d963f-120">Az eltávolítandó alapértelmezett webhelyt tartalmazó virtuális hálózati átjáróhoz tartozó objektum hivatkozását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d963f-120">Specifies an object reference to the virtual network gateway containing the default site to be removed.</span></span>
<span data-ttu-id="d963f-121">A virtuális hálózati átjáróhoz az Get-AzVirtualNetworkGateway használatával hozhat létre objektum-hivatkozást, és megadhatja az átjáró nevét.</span><span class="sxs-lookup"><span data-stu-id="d963f-121">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="d963f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d963f-122">CommonParameters</span></span>
<span data-ttu-id="d963f-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d963f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d963f-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d963f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d963f-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d963f-125">INPUTS</span></span>

### <span data-ttu-id="d963f-126">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d963f-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d963f-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d963f-127">OUTPUTS</span></span>

### <span data-ttu-id="d963f-128">Microsoft. Azure. commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d963f-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="d963f-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d963f-129">NOTES</span></span>

## <span data-ttu-id="d963f-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d963f-130">RELATED LINKS</span></span>

[<span data-ttu-id="d963f-131">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d963f-131">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="d963f-132">Set-AzVirtualNetworkGatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="d963f-132">Set-AzVirtualNetworkGatewayDefaultSite</span></span>](./Set-AzVirtualNetworkGatewayDefaultSite.md)


