---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 866a3b9ac28de57a71fce5fb84b2fa1144d0ff8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924658"
---
# <span data-ttu-id="35730-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="35730-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="35730-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35730-102">SYNOPSIS</span></span>
<span data-ttu-id="35730-103">Létrehoz egy új VPN-ügyfél legfelső szintű tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="35730-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="35730-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="35730-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35730-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="35730-105">DESCRIPTION</span></span>
<span data-ttu-id="35730-106">A **New-AzVpnClientRootCertificate** parancsmag létrehoz egy új VPN-gyökértanúsítványt virtuális hálózati átjárón való használatra.</span><span class="sxs-lookup"><span data-stu-id="35730-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="35730-107">A főtanúsítványok olyan X.509-tanúsítványok, amelyek azonosítják a legfelső szintű hitelesítésszolgáltatót: az átjárón használt összes többi tanúsítvány megbízik a legfelső szintű tanúsítványban.</span><span class="sxs-lookup"><span data-stu-id="35730-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="35730-108">Ez a parancsmag egy olyan különálló tanúsítványt hoz létre, amely nincs hozzárendelve egy virtuális átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="35730-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="35730-109">Ehelyett a **New-AzVpnClientRootCertificate** által létrehozott tanúsítványt a New-AzVirtualNetworkGateway parancsmaggal együtt használja új átjáró létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="35730-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="35730-110">Tegyük fel például, hogy létrehoz egy új tanúsítványt, és egy $Certificate.</span><span class="sxs-lookup"><span data-stu-id="35730-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="35730-111">Ezt a tanúsítványobjektumot használhatja új virtuális átjáró létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="35730-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="35730-112">Például: `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="35730-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="35730-113">További információt a New-AzVirtualNetworkGateway dokumentációjában talál.</span><span class="sxs-lookup"><span data-stu-id="35730-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="35730-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="35730-114">EXAMPLES</span></span>

### <span data-ttu-id="35730-115">1. példa: Ügyfél-főtanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="35730-115">Example 1: Create a client root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="35730-116">Ebben a példában egy ügyfél-gyökértanúsítványt hoz létre, és a tanúsítványobjektumot egy "$Certificate" nevű változóban $Certificate.</span><span class="sxs-lookup"><span data-stu-id="35730-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="35730-117">Ezt a változót a **New-AzVirtualNetworkGateway** parancsmag arra használhatja, hogy gyökértanúsítványt adjon hozzá egy új virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="35730-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="35730-118">Az első parancs a **Get-Content** parancsmagot használja a gyökértanúsítvány korábban exportált szövegként való megjelenítéséhez; hogy a szöveges adatokat egy $Text.</span><span class="sxs-lookup"><span data-stu-id="35730-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="35730-119">A második parancs ezután egy hurok segítségével kinyeri az összes szöveget, kivéve az első és az utolsó sort, és a kinyert szöveget egy új nevű változóban $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="35730-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="35730-120">A harmadik parancs a **New-AzVpnClientRootCertificate** parancsmagot használja a tanúsítvány létrehozásához, és a létrehozott objektumot egy $Certificate.</span><span class="sxs-lookup"><span data-stu-id="35730-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="35730-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35730-121">PARAMETERS</span></span>

### <span data-ttu-id="35730-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35730-122">-DefaultProfile</span></span>
<span data-ttu-id="35730-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35730-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35730-124">-Name</span><span class="sxs-lookup"><span data-stu-id="35730-124">-Name</span></span>
<span data-ttu-id="35730-125">Az új ügyfél legfelső szintű tanúsítványának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35730-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="35730-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="35730-126">-PublicCertData</span></span>
<span data-ttu-id="35730-127">Megadja a hozzáadni szükséges főtanúsítvány szövegként való megjelenítését.</span><span class="sxs-lookup"><span data-stu-id="35730-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="35730-128">A szöveg reprezentáció beszerzéséhez exportálja a tanúsítványt .cer formátumban (Base64 kódolással), majd nyissa meg az így kapott fájlt egy szövegszerkesztőben.</span><span class="sxs-lookup"><span data-stu-id="35730-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="35730-129">Ehhez hasonló kimenetet kell látnia (ne feledje, hogy a tényleges kimenet az itt látható rövidített mintaszövegnél sokkal több szövegsort fog tartalmazni): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span><span class="sxs-lookup"><span data-stu-id="35730-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="35730-130">A PublicCertData lekérdezéséhez a következő Windows PowerShell-parancsokat használhatja: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="35730-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="35730-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35730-131">CommonParameters</span></span>
<span data-ttu-id="35730-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35730-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35730-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35730-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35730-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35730-134">INPUTS</span></span>

### <span data-ttu-id="35730-135">System.String</span><span class="sxs-lookup"><span data-stu-id="35730-135">System.String</span></span>

## <span data-ttu-id="35730-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35730-136">OUTPUTS</span></span>

### <span data-ttu-id="35730-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="35730-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="35730-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="35730-138">NOTES</span></span>

## <span data-ttu-id="35730-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35730-139">RELATED LINKS</span></span>

[<span data-ttu-id="35730-140">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="35730-140">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="35730-141">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="35730-141">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="35730-142">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="35730-142">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


