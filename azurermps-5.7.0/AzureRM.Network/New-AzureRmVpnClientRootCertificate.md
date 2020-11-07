---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: b83af7bc0242ddf1c1ed5c182cd0be7c2b7d8a23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680138"
---
# <span data-ttu-id="632d6-101">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="632d6-101">New-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="632d6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="632d6-102">SYNOPSIS</span></span>
<span data-ttu-id="632d6-103">Létrehoz egy új VPN-ügyfél főtanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="632d6-103">Creates a new VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="632d6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="632d6-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="632d6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="632d6-105">DESCRIPTION</span></span>
<span data-ttu-id="632d6-106">A **New-AzureRmVpnClientRootCertificate** parancsmag létrehoz egy új virtuális magánhálózati tanúsítványt a virtuális hálózati átjárón való használatra.</span><span class="sxs-lookup"><span data-stu-id="632d6-106">The **New-AzureRmVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="632d6-107">A legfelső szintű tanúsítványok olyan X. 509 tanúsítványok, amelyek a legfelső szintű hitelesítésszolgáltatót használják: az átjárón használt összes többi tanúsítvány meghatalmazza a főtanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="632d6-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="632d6-108">Ez a parancsmag olyan különálló tanúsítványt hoz létre, amely nem egy virtuális átjáróhoz van társítva.</span><span class="sxs-lookup"><span data-stu-id="632d6-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="632d6-109">Ehelyett az **új AzureRmVpnClientRootCertificate** által létrehozott tanúsítványt az New-AzureRmVirtualNetworkGateway parancsmaggal együtt használják új átjáró létrehozásakor.</span><span class="sxs-lookup"><span data-stu-id="632d6-109">Instead, the certificate created by **New-AzureRmVpnClientRootCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="632d6-110">Tegyük fel például, hogy létrehoz egy új tanúsítványt, és egy $Certificate nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="632d6-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="632d6-111">Ezt a objektumtípust akkor használhatja, ha új virtuális átjárót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="632d6-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="632d6-112">Például</span><span class="sxs-lookup"><span data-stu-id="632d6-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`

<span data-ttu-id="632d6-113">További információt az New-AzureRmVirtualNetworkGateway parancsmag dokumentációjában talál.</span><span class="sxs-lookup"><span data-stu-id="632d6-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="632d6-114">Példák</span><span class="sxs-lookup"><span data-stu-id="632d6-114">EXAMPLES</span></span>

### <span data-ttu-id="632d6-115">1. példa: aclient-főtanúsítvány létrehozása</span><span class="sxs-lookup"><span data-stu-id="632d6-115">Example 1: Create aclient root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="632d6-116">Ez a példa létrehoz egy ügyfélalkalmazás főtanúsítványát, és a tanúsítvány-objektumot egy $Certificate nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="632d6-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="632d6-117">Ezt a változót a **New-AzureRmVirtualNetworkGateway** parancsmag használhatja a root tanúsítvány új virtuális hálózati átjáróhoz való hozzáadására.</span><span class="sxs-lookup"><span data-stu-id="632d6-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>

<span data-ttu-id="632d6-118">Az első parancs a **Get-Content** parancsmagot használva kapja meg a legfelső szintű tanúsítvány korábban exportált szövegét. a program a szöveges adatot egy $Text nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="632d6-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>

<span data-ttu-id="632d6-119">A második parancs ezután az a – Loop függvénnyel Kinyeri a szöveget az első és az utolsó sor kivételével, a kibontott szöveget a $CertificateText nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="632d6-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>

<span data-ttu-id="632d6-120">A harmadik parancs a **New-AzureRmVpnClientRootCertificate** parancsmagot használja a tanúsítvány létrehozásához, és a létrehozott objektumot a $Certificate nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="632d6-120">The third command uses the **New-AzureRmVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="632d6-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="632d6-121">PARAMETERS</span></span>

### <span data-ttu-id="632d6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="632d6-122">-DefaultProfile</span></span>
<span data-ttu-id="632d6-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="632d6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="632d6-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="632d6-124">-Name</span></span>
<span data-ttu-id="632d6-125">Az új ügyfél főtanúsítványának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="632d6-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="632d6-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="632d6-126">-PublicCertData</span></span>
<span data-ttu-id="632d6-127">A hozzáadni kívánt főtanúsítvány szöveges ábrázolását adja meg.</span><span class="sxs-lookup"><span data-stu-id="632d6-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="632d6-128">A szöveges ábrázolás beolvasásához exportálja a tanúsítványt. cer formátumban (Base64 kódolással), majd nyissa meg az így létrejövő fájlt egy szövegszerkesztőben.</span><span class="sxs-lookup"><span data-stu-id="632d6-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="632d6-129">Ehhez hasonló kimenetet kell látnia (Megjegyzendő, hogy a tényleges kimenet több sornyi szöveget fog tartalmazni, mint az itt látható rövidített minta):</span><span class="sxs-lookup"><span data-stu-id="632d6-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="632d6-130">----------MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w megkezdése-----a záró tanúsítvány-----</span><span class="sxs-lookup"><span data-stu-id="632d6-130">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="632d6-131">A PublicCertData az első sor (-----KEZDÉSi-----) és az utolsó sor (-----záró tanúsítvány-----) közötti minden sorból áll.</span><span class="sxs-lookup"><span data-stu-id="632d6-131">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="632d6-132">A PublicCertData a következőhöz hasonló Windows PowerShell-parancsokkal lehet letölteni:</span><span class="sxs-lookup"><span data-stu-id="632d6-132">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="632d6-133">$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. hossza-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="632d6-133">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="632d6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="632d6-134">CommonParameters</span></span>
<span data-ttu-id="632d6-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="632d6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="632d6-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="632d6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="632d6-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="632d6-137">INPUTS</span></span>

###  
<span data-ttu-id="632d6-138">Ez a parancsmag nem fogadja el a csővezetékes bevitelt.</span><span class="sxs-lookup"><span data-stu-id="632d6-138">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="632d6-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="632d6-139">OUTPUTS</span></span>

###  
<span data-ttu-id="632d6-140">Ez a parancsmag a **Microsoft. Azure. commands. Network. models. PSVpnClientRootCertificate** objektum új példányait hozza létre.</span><span class="sxs-lookup"><span data-stu-id="632d6-140">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="632d6-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="632d6-141">NOTES</span></span>

## <span data-ttu-id="632d6-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="632d6-142">RELATED LINKS</span></span>

[<span data-ttu-id="632d6-143">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="632d6-143">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="632d6-144">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="632d6-144">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="632d6-145">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="632d6-145">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


