---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e1f85cbb90e1318c6eab595ef00929ceb1a5b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493433"
---
# <span data-ttu-id="5ebd9-101">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5ebd9-101">New-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="5ebd9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ebd9-102">SYNOPSIS</span></span>
<span data-ttu-id="5ebd9-103">Új VPN-ügyfél-visszavonási tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="5ebd9-103">Creates a new VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ebd9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ebd9-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ebd9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ebd9-105">DESCRIPTION</span></span>
<span data-ttu-id="5ebd9-106">A **New-AzureRmVpnClientRevokedCertificate** parancsmag létrehoz egy új virtuális MAGÁNHÁLÓZATI (VPN) ügyfél-visszavonási tanúsítványt a virtuális hálózati átjáróban való használatra.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-106">The **New-AzureRmVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="5ebd9-107">Ügyfél – visszavonási tanúsítványok: megakadályozza, hogy az ügyfélszámítógépek a megadott tanúsítványt használják a hitelesítéshez.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>

<span data-ttu-id="5ebd9-108">Ez a parancsmag olyan különálló tanúsítványt hoz létre, amely nem egy virtuális átjáróhoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="5ebd9-109">Ehelyett az **új AzureRmVpnClientRevokedCertificate** által létrehozott tanúsítvány az New-AzureRmVirtualNetworkGateway parancsmaggal együtt használatos, amikor új átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-109">Instead, the certificate created by **New-AzureRmVpnClientRevokedCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="5ebd9-110">Tegyük fel például, hogy létrehoz egy új tanúsítványt, és egy $Certificate nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="5ebd9-111">Az új virtuális átjáró létrehozásakor ezt a objektumtípust használhatja.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="5ebd9-112">Például</span><span class="sxs-lookup"><span data-stu-id="5ebd9-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

<span data-ttu-id="5ebd9-113">További információt az New-AzureRmVirtualNetworkGateway parancsmag dokumentációjában talál.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="5ebd9-114">Példák</span><span class="sxs-lookup"><span data-stu-id="5ebd9-114">EXAMPLES</span></span>

### <span data-ttu-id="5ebd9-115">1. példa: új ügyfél által visszavont tanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="5ebd9-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="5ebd9-116">Ez a parancs új ügyfél által visszavont tanúsítványt hoz létre, és a bizonyítvány-objektumot egy $Certificate nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="5ebd9-117">Ezt a változót a **New-AzureRmVirtualNetworkGateway** parancsmag használhatja a tanúsítvány új virtuális hálózati átjáróhoz való hozzáadására.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="5ebd9-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ebd9-118">PARAMETERS</span></span>

### <span data-ttu-id="5ebd9-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ebd9-119">-Name</span></span>
<span data-ttu-id="5ebd9-120">Az új ügyfél-visszavonási tanúsítvány egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-120">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="5ebd9-121">-Ujjlenyomat</span><span class="sxs-lookup"><span data-stu-id="5ebd9-121">-Thumbprint</span></span>
<span data-ttu-id="5ebd9-122">A hozzáadott tanúsítvány egyedi azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-122">Specifies the unique identifier of the certificate being added.</span></span>

<span data-ttu-id="5ebd9-123">A tanúsítványok ujjlenyomat-adatait a következőhöz hasonló Windows PowerShell-parancs használatával adhatja vissza:</span><span class="sxs-lookup"><span data-stu-id="5ebd9-123">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path Cert:\LocalMachine\Root`

<span data-ttu-id="5ebd9-124">Az előző parancs a Root Certificate Store áruházban talált összes helyi számítógép-tanúsítványra vonatkozó információt ad vissza.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-124">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="5ebd9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ebd9-125">-DefaultProfile</span></span>
<span data-ttu-id="5ebd9-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ebd9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ebd9-127">CommonParameters</span></span>
<span data-ttu-id="5ebd9-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ebd9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ebd9-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ebd9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ebd9-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ebd9-130">INPUTS</span></span>

###  
<span data-ttu-id="5ebd9-131">Ez a parancsmag nem fogadja el a csővezetékes bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-131">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="5ebd9-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ebd9-132">OUTPUTS</span></span>

###  
<span data-ttu-id="5ebd9-133">Ez a parancsmag a **Microsoft. Azure. commands. Network. models. PSVpnClientRevokedCertificate** objektum új példányait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="5ebd9-133">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="5ebd9-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ebd9-134">NOTES</span></span>

## <span data-ttu-id="5ebd9-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ebd9-135">RELATED LINKS</span></span>

[<span data-ttu-id="5ebd9-136">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5ebd9-136">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="5ebd9-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5ebd9-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="5ebd9-138">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="5ebd9-138">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


