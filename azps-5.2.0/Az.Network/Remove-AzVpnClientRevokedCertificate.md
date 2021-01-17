---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 2dee180dff1489779dd2eb34f8bd5e3d8be10b91
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361926"
---
# <span data-ttu-id="a93ca-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a93ca-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="a93ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a93ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a93ca-103">Eltávolítja a VPN-ügyfél-visszavonási tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="a93ca-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="a93ca-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a93ca-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a93ca-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a93ca-105">DESCRIPTION</span></span>
<span data-ttu-id="a93ca-106">A **Remove-AzVpnClientRevokedCertificate parancsmag** eltávolítja az ügyfél-visszavonási tanúsítványt egy virtuális hálózati átjáróból.</span><span class="sxs-lookup"><span data-stu-id="a93ca-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="a93ca-107">Az ügyfél-visszavonási tanúsítványok megakadályozzák, hogy az ügyfélszámítógépek a megadott tanúsítványt használják hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="a93ca-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="a93ca-108">Ha eltávolít egy ügyfél-visszavonási tanúsítványt, az ügyfélszámítógépek a korábban letiltott tanúsítvánnyal virtuális magánhálózati kapcsolatot létesíthet.</span><span class="sxs-lookup"><span data-stu-id="a93ca-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="a93ca-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a93ca-109">EXAMPLES</span></span>

### <span data-ttu-id="a93ca-110">1. példa: Ügyfél-visszavonási tanúsítvány eltávolítása virtuális hálózati átjáróból</span><span class="sxs-lookup"><span data-stu-id="a93ca-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```powershell
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="a93ca-111">Ez a parancs eltávolítja az ügyfél-visszavonási tanúsítványt a ContosoVirtualNetwork nevű virtuális hálózati átjáróból.</span><span class="sxs-lookup"><span data-stu-id="a93ca-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="a93ca-112">Az ügyfél-visszavonási tanúsítvány eltávolításához meg kell adnia a tanúsítvány nevét és a tanúsítvány thumbprint-ját is.</span><span class="sxs-lookup"><span data-stu-id="a93ca-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="a93ca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a93ca-113">PARAMETERS</span></span>

### <span data-ttu-id="a93ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93ca-114">-DefaultProfile</span></span>
<span data-ttu-id="a93ca-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a93ca-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a93ca-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a93ca-116">-ResourceGroupName</span></span>
<span data-ttu-id="a93ca-117">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a virtuális hálózati átjáró hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a93ca-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="a93ca-118">Az erőforráscsoportok a készletkezelés és az általános Azure-felügyelet egyszerűsítése érdekében kategorizálják az elemeket.</span><span class="sxs-lookup"><span data-stu-id="a93ca-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93ca-119">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="a93ca-119">-Thumbprint</span></span>
<span data-ttu-id="a93ca-120">Az eltávolított tanúsítvány egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a93ca-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="a93ca-121">A tanúsítványokhoz az ehhez hasonló Windows PowerShell-paranccsal is vissza lehet nyomtatni a tanúsítványokat: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="a93ca-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="a93ca-122">Az előző parancs a gyökértanúsítvány-tárolóban található összes helyi számítógéptanúsítvány adatait adja vissza.</span><span class="sxs-lookup"><span data-stu-id="a93ca-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="a93ca-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="a93ca-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="a93ca-124">Annak a virtuális hálózati átjárónak a nevét adja meg, amelyhez a tanúsítvány hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a93ca-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93ca-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="a93ca-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="a93ca-126">Az eltávolított VPN-ügyfél tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a93ca-126">Specifies the name of the VPN client certificate being removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93ca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93ca-127">CommonParameters</span></span>
<span data-ttu-id="a93ca-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a93ca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93ca-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a93ca-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93ca-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a93ca-130">INPUTS</span></span>

### <span data-ttu-id="a93ca-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a93ca-131">System.String</span></span>

## <span data-ttu-id="a93ca-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a93ca-132">OUTPUTS</span></span>

### <span data-ttu-id="a93ca-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a93ca-133">System.Boolean</span></span>

## <span data-ttu-id="a93ca-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a93ca-134">NOTES</span></span>

## <span data-ttu-id="a93ca-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a93ca-135">RELATED LINKS</span></span>

[<span data-ttu-id="a93ca-136">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a93ca-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="a93ca-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a93ca-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="a93ca-138">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="a93ca-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


