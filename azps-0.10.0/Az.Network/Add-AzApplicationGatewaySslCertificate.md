---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 964e99912e4f21d48e89b725da1aa44ac32ea186
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841850"
---
# <span data-ttu-id="e4509-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4509-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e4509-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4509-102">SYNOPSIS</span></span>
<span data-ttu-id="e4509-103">SSL-tanúsítványt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e4509-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="e4509-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4509-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4509-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4509-105">DESCRIPTION</span></span>
<span data-ttu-id="e4509-106">Az **Add-AzApplicationGatewaySslCertificate** PARANCSMAG egy SSL-tanúsítványt ad az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="e4509-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="e4509-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4509-107">EXAMPLES</span></span>

### <span data-ttu-id="e4509-108">1. példa: SSL-tanúsítvány felvétele az alkalmazás-átjáróba.</span><span class="sxs-lookup"><span data-stu-id="e4509-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="e4509-109">Ez a parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja, majd hozzáadja a Cert01 nevű SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="e4509-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="e4509-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4509-110">PARAMETERS</span></span>

### <span data-ttu-id="e4509-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4509-111">-ApplicationGateway</span></span>
<span data-ttu-id="e4509-112">Annak az alkalmazás-átjárónak a nevét adja meg, amelyre a parancsmag hozzáadja az SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="e4509-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4509-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e4509-113">-CertificateFile</span></span>
<span data-ttu-id="e4509-114">A parancsmag által hozzáadott SSL-tanúsítvány. pfx fájlja.</span><span class="sxs-lookup"><span data-stu-id="e4509-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e4509-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4509-115">-DefaultProfile</span></span>
<span data-ttu-id="e4509-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e4509-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4509-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e4509-117">-Name</span></span>
<span data-ttu-id="e4509-118">Annak az SSL-tanúsítványnak a neve, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="e4509-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e4509-119">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="e4509-119">-Password</span></span>
<span data-ttu-id="e4509-120">Annak az SSL-tanúsítványnak a jelszava, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="e4509-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4509-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4509-121">CommonParameters</span></span>
<span data-ttu-id="e4509-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4509-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4509-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4509-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4509-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4509-124">INPUTS</span></span>

### <span data-ttu-id="e4509-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e4509-125">System.String</span></span>

## <span data-ttu-id="e4509-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4509-126">OUTPUTS</span></span>

### <span data-ttu-id="e4509-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e4509-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e4509-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4509-128">NOTES</span></span>

## <span data-ttu-id="e4509-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4509-129">RELATED LINKS</span></span>

[<span data-ttu-id="e4509-130">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4509-130">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e4509-131">Új – AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4509-131">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e4509-132">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4509-132">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e4509-133">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e4509-133">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


