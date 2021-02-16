---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: ba9715b6f29cd45ba25f8b2d2ab85ba0d7ef7979
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160771"
---
# <span data-ttu-id="d3912-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d3912-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="d3912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3912-102">SYNOPSIS</span></span>
<span data-ttu-id="d3912-103">Létrehoz egy új VPN-ügyfél-visszavonási tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="d3912-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="d3912-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d3912-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3912-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d3912-105">DESCRIPTION</span></span>
<span data-ttu-id="d3912-106">A **New-AzVpnClientRevokedCertificate parancsmag** létrehoz egy új virtuális magánhálózati ügyfél-visszavonási tanúsítványt virtuális hálózati átjárón való használatra.</span><span class="sxs-lookup"><span data-stu-id="d3912-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="d3912-107">Az ügyfél-visszavonási tanúsítványok megakadályozzák, hogy az ügyfélszámítógépek a megadott tanúsítványt használják hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="d3912-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="d3912-108">Ez a parancsmag egy olyan különálló tanúsítványt hoz létre, amely nincs hozzárendelve egy virtuális átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="d3912-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="d3912-109">Ehelyett a **New-AzVpnClientRevokedCertificate** által létrehozott tanúsítványt a New-AzVirtualNetworkGateway-parancsmaggal együtt használja, amikor új átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d3912-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="d3912-110">Tegyük fel például, hogy létrehoz egy új tanúsítványt, és egy $Certificate.</span><span class="sxs-lookup"><span data-stu-id="d3912-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="d3912-111">Ezt a tanúsítványobjektumot használhatja új virtuális átjáró létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="d3912-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="d3912-112">Például: `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="d3912-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="d3912-113">További információt a New-AzVirtualNetworkGateway dokumentációjában talál.</span><span class="sxs-lookup"><span data-stu-id="d3912-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="d3912-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d3912-114">EXAMPLES</span></span>

### <span data-ttu-id="d3912-115">1. példa: Új ügyfél által visszavont tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="d3912-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="d3912-116">Ez a parancs létrehoz egy új ügyfél által visszavont tanúsítványt, és a tanúsítványobjektumot egy $Certificate.</span><span class="sxs-lookup"><span data-stu-id="d3912-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="d3912-117">Ezt a változót a **New-AzVirtualNetworkGateway** parancsmag használhatja a tanúsítvány új virtuális hálózati átjáróhoz való hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="d3912-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="d3912-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3912-118">PARAMETERS</span></span>

### <span data-ttu-id="d3912-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3912-119">-DefaultProfile</span></span>
<span data-ttu-id="d3912-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3912-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3912-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d3912-121">-Name</span></span>
<span data-ttu-id="d3912-122">Az új ügyfél-visszavonási tanúsítvány egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3912-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="d3912-123">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="d3912-123">-Thumbprint</span></span>
<span data-ttu-id="d3912-124">A hozzáadott tanúsítvány egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="d3912-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="d3912-125">A tanúsítványokhoz az ehhez hasonló Windows PowerShell-paranccsal is vissza lehet nyomtatni a tanúsítványokat: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="d3912-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="d3912-126">Az előző parancs a gyökértanúsítvány-tárolóban található összes helyi számítógéptanúsítvány adatait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="d3912-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="d3912-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3912-127">CommonParameters</span></span>
<span data-ttu-id="d3912-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3912-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3912-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3912-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3912-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3912-130">INPUTS</span></span>

### <span data-ttu-id="d3912-131">Nincs</span><span class="sxs-lookup"><span data-stu-id="d3912-131">None</span></span>

## <span data-ttu-id="d3912-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3912-132">OUTPUTS</span></span>

### <span data-ttu-id="d3912-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d3912-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="d3912-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d3912-134">NOTES</span></span>

## <span data-ttu-id="d3912-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3912-135">RELATED LINKS</span></span>

[<span data-ttu-id="d3912-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d3912-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="d3912-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d3912-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="d3912-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="d3912-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


