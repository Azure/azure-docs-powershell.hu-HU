---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 5f642892413b027d3eee4dec3c0264587dbb02a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503560"
---
# <span data-ttu-id="07bc9-101">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07bc9-101">Add-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="07bc9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="07bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="07bc9-103">VPN-ügyfél legfelső szintű tanúsítványát adja hozzá.</span><span class="sxs-lookup"><span data-stu-id="07bc9-103">Adds a VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07bc9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="07bc9-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07bc9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="07bc9-105">DESCRIPTION</span></span>
<span data-ttu-id="07bc9-106">Az **Add-AzureRmVpnClientRootCertificate** parancsmag főtanúsítványot ad egy virtuális hálózati átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="07bc9-106">The **Add-AzureRmVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="07bc9-107">A gyökérszintű tanúsítványok olyan X. 509 tanúsítványok, amelyek a legfelső szintű hitelesítésszolgáltatót hitelesítik.</span><span class="sxs-lookup"><span data-stu-id="07bc9-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="07bc9-108">Tervezéssel minden olyan tanúsítvány, amely az átjárón a legfelső szintű tanúsítványt használja.</span><span class="sxs-lookup"><span data-stu-id="07bc9-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="07bc9-109">Ez a parancsmag egy meglévő tanúsítványt rendel el átjáró legfelső szintű tanúsítványként.</span><span class="sxs-lookup"><span data-stu-id="07bc9-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="07bc9-110">Ha nincs olyan X. 509 tanúsítvány, amellyel létrehozhatja a nyilvános kulcsú infrastruktúráját, vagy használhatja a tanúsítványt Generator (például makecert.exe) segítségével.</span><span class="sxs-lookup"><span data-stu-id="07bc9-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="07bc9-111">Főtanúsítvány hozzáadásához meg kell adnia a tanúsítvány nevét, és csak szöveges formátumban kell megadnia a tanúsítványt (további információt *a PublicCertData* paraméterben talál).</span><span class="sxs-lookup"><span data-stu-id="07bc9-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="07bc9-112">Az Azure lehetővé teszi, hogy egynél több főtanúsítványt rendeljen egy átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="07bc9-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="07bc9-113">A több főtanúsítványt gyakran olyan szervezetek telepítik, amelyek egynél több vállalat felhasználóit tartalmazzák.</span><span class="sxs-lookup"><span data-stu-id="07bc9-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="07bc9-114">Példák</span><span class="sxs-lookup"><span data-stu-id="07bc9-114">EXAMPLES</span></span>

### <span data-ttu-id="07bc9-115">1. példa: az ügyfél legfelső szintű tanúsítványának felvétele virtuális átjáróba</span><span class="sxs-lookup"><span data-stu-id="07bc9-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="07bc9-116">Ez a példa a ContosoVirtualGateway nevű virtuális átjáróhoz hozzáadja az ügyfél főtanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="07bc9-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="07bc9-117">Az első parancs a **Get-Content** parancsmagot használva kapja meg a legfelső szintű tanúsítvány korábban exportált szöveges ábrázolását, és tárolja a szöveges adatok a $Text nevű változót.</span><span class="sxs-lookup"><span data-stu-id="07bc9-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="07bc9-118">A második parancs ezután az a – Loop függvénnyel kinyeri az összes szövegrészt, az első és az utolsó soron kívül.</span><span class="sxs-lookup"><span data-stu-id="07bc9-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="07bc9-119">A kibontott szöveg egy $CertificateText nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="07bc9-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="07bc9-120">A harmadik parancs ezután a $CertificateText-ban tárolt szöveget használja az **Add-AzureRmVpnClientRootCertificate** parancsmaggal a főtanúsítványnak az átjáróhoz való hozzáadásához.</span><span class="sxs-lookup"><span data-stu-id="07bc9-120">The third command then uses the text stored in $CertificateText with the **Add-AzureRmVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="07bc9-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="07bc9-121">PARAMETERS</span></span>

### <span data-ttu-id="07bc9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bc9-122">-DefaultProfile</span></span>
<span data-ttu-id="07bc9-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="07bc9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07bc9-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="07bc9-124">-PublicCertData</span></span>
<span data-ttu-id="07bc9-125">A beadni kívánt főtanúsítvány szöveges ábrázolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="07bc9-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="07bc9-126">A szöveges ábrázolás beolvasásához exportálja a tanúsítványt. cer formátumban (Base64 kódolással), majd nyissa meg az így létrejövő fájlt egy szövegszerkesztőben.</span><span class="sxs-lookup"><span data-stu-id="07bc9-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="07bc9-127">Ha ezt a lehetőséget választja, az alábbihoz hasonló kimenet jelenik meg (Megjegyzendő, hogy a tényleges kimenet több sornyi szöveget tartalmaz, mint az itt látható):-----a-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----záró TANÚSÍTVÁNYát,-----a PublicCertData az első sor (-----KEZDÉSi tanúsítvány-----) és a fájl utolsó sora (-----záró tanúsítvány-----) közötti sorokból áll.</span><span class="sxs-lookup"><span data-stu-id="07bc9-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="07bc9-128">Ezeket az adatforrásokat az alábbihoz hasonló Windows PowerShell-parancsok segítségével tudja letölteni: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="07bc9-128">You can retrieve this data  by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="07bc9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07bc9-129">-ResourceGroupName</span></span>
<span data-ttu-id="07bc9-130">Annak az erőforráscsoportnek a neve, amelyhez a főtanúsítvány van rendelve.</span><span class="sxs-lookup"><span data-stu-id="07bc9-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="07bc9-131">Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.</span><span class="sxs-lookup"><span data-stu-id="07bc9-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="07bc9-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="07bc9-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="07bc9-133">Annak a virtuális hálózati átjárónak a neve, amelybe a tanúsítványt felveszi.</span><span class="sxs-lookup"><span data-stu-id="07bc9-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="07bc9-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="07bc9-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="07bc9-135">Annak az ügyfél-főtanúsítványnak a nevét adja meg, amelyre a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="07bc9-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="07bc9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bc9-136">CommonParameters</span></span>
<span data-ttu-id="07bc9-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="07bc9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bc9-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07bc9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bc9-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="07bc9-139">INPUTS</span></span>

### <span data-ttu-id="07bc9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="07bc9-140">System.String</span></span>

## <span data-ttu-id="07bc9-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="07bc9-141">OUTPUTS</span></span>

### <span data-ttu-id="07bc9-142">Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07bc9-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="07bc9-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="07bc9-143">NOTES</span></span>

## <span data-ttu-id="07bc9-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="07bc9-144">RELATED LINKS</span></span>

[<span data-ttu-id="07bc9-145">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07bc9-145">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="07bc9-146">Új – AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07bc9-146">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="07bc9-147">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="07bc9-147">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


