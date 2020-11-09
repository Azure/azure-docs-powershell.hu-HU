---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301847"
---
# <span data-ttu-id="2a014-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="2a014-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="2a014-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2a014-102">SYNOPSIS</span></span>
<span data-ttu-id="2a014-103">Új VPN-ügyfél-visszavonási tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="2a014-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="2a014-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2a014-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a014-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2a014-105">DESCRIPTION</span></span>
<span data-ttu-id="2a014-106">A **New-AzVpnClientRevokedCertificate** parancsmag létrehoz egy új virtuális MAGÁNHÁLÓZATI (VPN) ügyfél-visszavonási tanúsítványt a virtuális hálózati átjáróban való használatra.</span><span class="sxs-lookup"><span data-stu-id="2a014-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="2a014-107">Ügyfél – visszavonási tanúsítványok: megakadályozza, hogy az ügyfélszámítógépek a megadott tanúsítványt használják a hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="2a014-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="2a014-108">Ez a parancsmag olyan különálló tanúsítványt hoz létre, amely nem egy virtuális átjáróhoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="2a014-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="2a014-109">Ehelyett az **új AzVpnClientRevokedCertificate** által létrehozott tanúsítvány az New-AzVirtualNetworkGateway parancsmaggal együtt használatos, amikor új átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2a014-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="2a014-110">Tegyük fel például, hogy létrehoz egy új tanúsítványt, és egy $Certificate nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2a014-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="2a014-111">Az új virtuális átjáró létrehozásakor ezt a objektumtípust használhatja.</span><span class="sxs-lookup"><span data-stu-id="2a014-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="2a014-112">Például `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="2a014-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="2a014-113">További információt az New-AzVirtualNetworkGateway parancsmag dokumentációjában talál.</span><span class="sxs-lookup"><span data-stu-id="2a014-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="2a014-114">Példák</span><span class="sxs-lookup"><span data-stu-id="2a014-114">EXAMPLES</span></span>

### <span data-ttu-id="2a014-115">1. példa: új ügyfél által visszavont tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="2a014-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="2a014-116">Ez a parancs új ügyfél által visszavont tanúsítványt hoz létre, és a bizonyítvány-objektumot egy $Certificate nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2a014-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="2a014-117">Ezt a változót a **New-AzVirtualNetworkGateway** parancsmag használhatja a tanúsítvány új virtuális hálózati átjáróhoz való hozzáadására.</span><span class="sxs-lookup"><span data-stu-id="2a014-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="2a014-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2a014-118">PARAMETERS</span></span>

### <span data-ttu-id="2a014-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a014-119">-DefaultProfile</span></span>
<span data-ttu-id="2a014-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2a014-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a014-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2a014-121">-Name</span></span>
<span data-ttu-id="2a014-122">Az új ügyfél-visszavonási tanúsítvány egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a014-122">Specifies a unique name for the new client-revocation certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a014-123">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="2a014-123">-Thumbprint</span></span>
<span data-ttu-id="2a014-124">A hozzáadott tanúsítvány egyedi azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2a014-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="2a014-125">A tanúsítványok ujjlenyomat-adatait a következőhöz hasonló Windows PowerShell-parancs használatával adhatja vissza: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="2a014-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="2a014-126">Az előző parancs a Root Certificate Store áruházban talált összes helyi számítógép-tanúsítványra vonatkozó információt ad vissza.</span><span class="sxs-lookup"><span data-stu-id="2a014-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a014-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a014-127">CommonParameters</span></span>
<span data-ttu-id="2a014-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2a014-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a014-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a014-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a014-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a014-130">INPUTS</span></span>

### <span data-ttu-id="2a014-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="2a014-131">None</span></span>

## <span data-ttu-id="2a014-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2a014-132">OUTPUTS</span></span>

### <span data-ttu-id="2a014-133">Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="2a014-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="2a014-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2a014-134">NOTES</span></span>

## <span data-ttu-id="2a014-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2a014-135">RELATED LINKS</span></span>

[<span data-ttu-id="2a014-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="2a014-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="2a014-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="2a014-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="2a014-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="2a014-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


