---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 95442c724548119726aa466edf1b4fa223271865
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504324"
---
# <span data-ttu-id="8637d-101">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8637d-101">Remove-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="8637d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8637d-102">SYNOPSIS</span></span>
<span data-ttu-id="8637d-103">Eltávolítja a meglévő VPN-ügyfél legfelső szintű tanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="8637d-103">Removes an existing VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8637d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8637d-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8637d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8637d-105">DESCRIPTION</span></span>
<span data-ttu-id="8637d-106">A **Remove-AzureRmVpnClientRootCertificate** parancsmag eltávolítja a megadott főtanúsítványt egy virtuális hálózati átjáróról.</span><span class="sxs-lookup"><span data-stu-id="8637d-106">The **Remove-AzureRmVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="8637d-107">A legfelső szintű tanúsítványok olyan X. 509 tanúsítványok, amelyek a legfelső szintű hitelesítésszolgáltatót használják: az átjárón használt összes többi tanúsítvány meghatalmazza a főtanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="8637d-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="8637d-108">Ha eltávolít egy olyan főtanúsítványos számítógépeket, amelyek a tanúsítványt a hitelesítés céljából használják, a továbbiakban nem fog tudni csatlakozni az átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="8637d-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>
<span data-ttu-id="8637d-109">A **Remove-AzureRmVpnClientRootCertificate** használata esetén mind a tanúsítvány nevét, mind a tanúsítvány adatainak szöveges ábrázolását meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="8637d-109">When you use **Remove-AzureRmVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="8637d-110">A tanúsítványok szöveges ábrázolásáról további információt a *PublicCertData* paraméter leírása című témakörben találhat.</span><span class="sxs-lookup"><span data-stu-id="8637d-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="8637d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8637d-111">EXAMPLES</span></span>

### <span data-ttu-id="8637d-112">1. példa: az ügyfél legfelső szintű tanúsítványának eltávolítása virtuális hálózati átjáróról</span><span class="sxs-lookup"><span data-stu-id="8637d-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="8637d-113">Ez a példa eltávolítja a ContosoRootCertificate nevű ügyfél-főtanúsítványt a virtuális hálózati átjáró ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="8637d-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>
<span data-ttu-id="8637d-114">Az első parancs a **Get-Content** parancsmagot használva kapja meg a tanúsítvány korábban kivitt szöveges ábrázolását; ezt a szöveges ábrázolást a $Text nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="8637d-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>
<span data-ttu-id="8637d-115">A második parancs ezután az a – Loop függvénnyel kinyeri az összes szöveget $Text az első és az utolsó sorának kivételével.</span><span class="sxs-lookup"><span data-stu-id="8637d-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="8637d-116">Ez a kibontott szöveg egy $CertificateText nevű változóban tárolódik.</span><span class="sxs-lookup"><span data-stu-id="8637d-116">This extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="8637d-117">A harmadik parancs a $CertificateText-változóban tárolt információkat a **Remove-AzureRmVpnClientRootCertificate** parancsmaggal együtt a tanúsítványnak az átjáróról való eltávolítására használja.</span><span class="sxs-lookup"><span data-stu-id="8637d-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzureRmVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="8637d-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8637d-118">PARAMETERS</span></span>

### <span data-ttu-id="8637d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8637d-119">-DefaultProfile</span></span>
<span data-ttu-id="8637d-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8637d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8637d-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="8637d-121">-PublicCertData</span></span>
<span data-ttu-id="8637d-122">Az eltávolítani kívánt főtanúsítvány szöveges ábrázolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="8637d-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="8637d-123">A szöveges ábrázolás beolvasásához exportálja a tanúsítványt. cer formátumban (Base64-kódolással), majd nyissa meg az így létrejövő fájlt egy szövegszerkesztőben.</span><span class="sxs-lookup"><span data-stu-id="8637d-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="8637d-124">A következőhöz hasonló kimenetet kell látnia (ne feledje, hogy a tényleges kimenet több sornyi szöveget fog tartalmazni, mint az itt látható):-----megkezdi a tanúsítvány-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----záró TANÚSÍTVÁNYát-----a PublicCertData az első sor (-----KEZDÉSi tanúsítvány-----) és a fájl utolsó sora (-----záró tanúsítvány-----) között található.</span><span class="sxs-lookup"><span data-stu-id="8637d-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="8637d-125">A PublicCertData a következőhöz hasonló Windows PowerShell-parancsokkal lehet letölteni: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="8637d-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="8637d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8637d-126">-ResourceGroupName</span></span>
<span data-ttu-id="8637d-127">Annak az erőforráscsoportnek a neve, amelyhez a virtuális hálózati átjáró van rendelve.</span><span class="sxs-lookup"><span data-stu-id="8637d-127">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="8637d-128">Az erőforráscsoportok kategorizálják az elemeket, amelyek megkönnyítik a Készletkezelés és az Azure általános felügyelet egyszerűsítését.</span><span class="sxs-lookup"><span data-stu-id="8637d-128">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="8637d-129">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8637d-129">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8637d-130">Annak a virtuális hálózati átjárónak a neve, amelyből a tanúsítványt törölték.</span><span class="sxs-lookup"><span data-stu-id="8637d-130">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="8637d-131">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="8637d-131">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="8637d-132">Annak az ügyfél-főtanúsítványnak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="8637d-132">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8637d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8637d-133">CommonParameters</span></span>
<span data-ttu-id="8637d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8637d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8637d-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8637d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8637d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8637d-136">INPUTS</span></span>

### <span data-ttu-id="8637d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8637d-137">System.String</span></span>

## <span data-ttu-id="8637d-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8637d-138">OUTPUTS</span></span>

### <span data-ttu-id="8637d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8637d-139">System.Boolean</span></span>

## <span data-ttu-id="8637d-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8637d-140">NOTES</span></span>

## <span data-ttu-id="8637d-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8637d-141">RELATED LINKS</span></span>

[<span data-ttu-id="8637d-142">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8637d-142">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="8637d-143">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8637d-143">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="8637d-144">Új – AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8637d-144">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)


