---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e7c2b8d4e26e45fff0c81f5bf3fecd10e40cd7a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467410"
---
# <span data-ttu-id="04498-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="04498-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="04498-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04498-102">SYNOPSIS</span></span>
<span data-ttu-id="04498-103">Hozzáad egy VPN-ügyfél-visszavonási tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="04498-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="04498-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="04498-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04498-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="04498-105">DESCRIPTION</span></span>
<span data-ttu-id="04498-106">Az **Add-AzVpnClientRevokedCertificate parancsmag** ügyfél-visszavonási tanúsítványt rendel egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="04498-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="04498-107">Az ügyfél-visszavonási tanúsítványok megakadályozzák, hogy az ügyfélszámítógépek a megadott tanúsítványt használják hitelesítésre.</span><span class="sxs-lookup"><span data-stu-id="04498-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="04498-108">Ehhez a parancsmaghoz meg kell adnia a tanúsítvány nevét és a tanúsítvány thumbprint-ját is.</span><span class="sxs-lookup"><span data-stu-id="04498-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="04498-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="04498-109">EXAMPLES</span></span>

### <span data-ttu-id="04498-110">1. példa: Új ügyfél-visszavonási tanúsítvány hozzáadása virtuális hálózati átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="04498-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```powershell
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="04498-111">Ez a parancs hozzáad egy új ügyfél-visszavonási tanúsítványt a ContosoVirtualNetwork nevű virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="04498-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="04498-112">A tanúsítvány hozzáadásához meg kell adnia a tanúsítvány nevét és a tanúsítvány thumbprint-ját is.</span><span class="sxs-lookup"><span data-stu-id="04498-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="04498-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04498-113">PARAMETERS</span></span>

### <span data-ttu-id="04498-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04498-114">-DefaultProfile</span></span>
<span data-ttu-id="04498-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="04498-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04498-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04498-116">-ResourceGroupName</span></span>
<span data-ttu-id="04498-117">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a virtuális hálózati átjáró hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="04498-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="04498-118">Az erőforráscsoportok a készletkezelés és az általános Azure-felügyelet egyszerűsítése érdekében kategorizálják az elemeket.</span><span class="sxs-lookup"><span data-stu-id="04498-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="04498-119">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="04498-119">-Thumbprint</span></span>
<span data-ttu-id="04498-120">A hozzáadott tanúsítvány egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="04498-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="04498-121">Például: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" A tanúsítványokhoz az alábbihoz hasonló Windows PowerShell-paranccsal kaphat thumbprint információkat: `Get-ChildItem -Path Cert:\LocalMachine\Root` .</span><span class="sxs-lookup"><span data-stu-id="04498-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="04498-122">Az előző parancs információkat kap a legfelső szintű tanúsítványtárban található összes helyi számítógéptanúsítványról.</span><span class="sxs-lookup"><span data-stu-id="04498-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="04498-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="04498-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="04498-124">Megadja annak a virtuális hálózati átjárónak a nevét, ahol a tanúsítványt hozzá kell adni.</span><span class="sxs-lookup"><span data-stu-id="04498-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="04498-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="04498-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="04498-126">A hozzáadni szükséges VPN-ügyfél tanúsítvány neve.</span><span class="sxs-lookup"><span data-stu-id="04498-126">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="04498-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04498-127">CommonParameters</span></span>
<span data-ttu-id="04498-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04498-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04498-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04498-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04498-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04498-130">INPUTS</span></span>

### <span data-ttu-id="04498-131">System.String</span><span class="sxs-lookup"><span data-stu-id="04498-131">System.String</span></span>

## <span data-ttu-id="04498-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04498-132">OUTPUTS</span></span>

### <span data-ttu-id="04498-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="04498-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="04498-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="04498-134">NOTES</span></span>

## <span data-ttu-id="04498-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04498-135">RELATED LINKS</span></span>

[<span data-ttu-id="04498-136">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="04498-136">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="04498-137">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="04498-137">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="04498-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="04498-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


