---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: ce4d2c61feb20c750d908b6f235d89dafa713e62
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850609"
---
# <span data-ttu-id="be0c0-101">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="be0c0-101">Remove-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="be0c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="be0c0-102">SYNOPSIS</span></span>
<span data-ttu-id="be0c0-103">A VPN-ügyfél-visszavonási tanúsítvány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="be0c0-103">Removes a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be0c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="be0c0-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be0c0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="be0c0-105">DESCRIPTION</span></span>
<span data-ttu-id="be0c0-106">A **Remove-AzureRmVpnClientRevokedCertificate** parancsmag egy ügyfél-visszavonási tanúsítványt távolít el egy virtuális hálózati átjáróról.</span><span class="sxs-lookup"><span data-stu-id="be0c0-106">The **Remove-AzureRmVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="be0c0-107">Ügyfél – visszavonási tanúsítványok: megakadályozza, hogy az ügyfélszámítógépek a megadott tanúsítványt használják a hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="be0c0-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="be0c0-108">Ha eltávolítja az ügyfél-visszavonási tanúsítványt futtató számítógépeket, a korábban betiltott tanúsítvány segítségével virtuális magánhálózati (VPN-) kapcsolatot hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="be0c0-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="be0c0-109">Példák</span><span class="sxs-lookup"><span data-stu-id="be0c0-109">EXAMPLES</span></span>

### <span data-ttu-id="be0c0-110">1. példa: ügyfél-visszavonási tanúsítvány eltávolítása virtuális hálózati átjáróról</span><span class="sxs-lookup"><span data-stu-id="be0c0-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="be0c0-111">Ez a parancs eltávolítja a ContosoVirtualNetwork nevű virtuális hálózati átjárótól származó ügyfél-visszavonási tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="be0c0-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="be0c0-112">Az ügyfél-visszavonási tanúsítvány eltávolításához meg kell adnia a tanúsítvány nevét és a tanúsítvány ujjlenyomatát is.</span><span class="sxs-lookup"><span data-stu-id="be0c0-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="be0c0-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="be0c0-113">PARAMETERS</span></span>

### <span data-ttu-id="be0c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be0c0-114">-DefaultProfile</span></span>
<span data-ttu-id="be0c0-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="be0c0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be0c0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be0c0-116">-ResourceGroupName</span></span>
<span data-ttu-id="be0c0-117">Annak az erőforráscsoportnek a neve, amelyhez a virtuális hálózati átjáró van rendelve.</span><span class="sxs-lookup"><span data-stu-id="be0c0-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="be0c0-118">Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.</span><span class="sxs-lookup"><span data-stu-id="be0c0-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be0c0-119">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="be0c0-119">-Thumbprint</span></span>
<span data-ttu-id="be0c0-120">Az eltávolított tanúsítvány egyedi azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="be0c0-120">Specifies the unique identifier of the certificate being removed.</span></span>

<span data-ttu-id="be0c0-121">A tanúsítványok ujjlenyomat-adatait a következőhöz hasonló Windows PowerShell-parancs használatával adhatja vissza:</span><span class="sxs-lookup"><span data-stu-id="be0c0-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path "Cert:\LocalMachine\Root"`

<span data-ttu-id="be0c0-122">Az előző parancs a Root Certificate Store áruházban talált összes helyi számítógép-tanúsítványra vonatkozó információt ad vissza.</span><span class="sxs-lookup"><span data-stu-id="be0c0-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be0c0-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="be0c0-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="be0c0-124">Annak a virtuális hálózati átjárónak a neve, amelyhez a tanúsítvány van rendelve.</span><span class="sxs-lookup"><span data-stu-id="be0c0-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be0c0-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="be0c0-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="be0c0-126">A VPN-ügyfél által eltávolított tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="be0c0-126">Specifies the name of the VPN client certificate being removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be0c0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be0c0-127">CommonParameters</span></span>
<span data-ttu-id="be0c0-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="be0c0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be0c0-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be0c0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be0c0-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="be0c0-130">INPUTS</span></span>

## <span data-ttu-id="be0c0-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="be0c0-131">OUTPUTS</span></span>

## <span data-ttu-id="be0c0-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="be0c0-132">NOTES</span></span>

## <span data-ttu-id="be0c0-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="be0c0-133">RELATED LINKS</span></span>

[<span data-ttu-id="be0c0-134">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="be0c0-134">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="be0c0-135">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="be0c0-135">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="be0c0-136">Új – AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="be0c0-136">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)


