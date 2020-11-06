---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7cf1f52c8035adcb6dcb773106a77045525cf937
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496463"
---
# <span data-ttu-id="02072-101">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="02072-101">Add-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="02072-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="02072-102">SYNOPSIS</span></span>
<span data-ttu-id="02072-103">SSL-tanúsítványt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="02072-103">Adds an SSL certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02072-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="02072-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="02072-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="02072-105">DESCRIPTION</span></span>
<span data-ttu-id="02072-106">Az **Add-AzureRmApplicationGatewaySslCertificate** PARANCSMAG egy SSL-tanúsítványt ad az alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="02072-106">The **Add-AzureRmApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="02072-107">Példák</span><span class="sxs-lookup"><span data-stu-id="02072-107">EXAMPLES</span></span>

### <span data-ttu-id="02072-108">1. példa: SSL-tanúsítvány felvétele az alkalmazás-átjáróba.</span><span class="sxs-lookup"><span data-stu-id="02072-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="02072-109">Ez a parancs a ApplicationGateway01 nevű alkalmazás-átjárót kapja, majd hozzáadja a Cert01 nevű SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="02072-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="02072-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="02072-110">PARAMETERS</span></span>

### <span data-ttu-id="02072-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02072-111">-ApplicationGateway</span></span>
<span data-ttu-id="02072-112">Annak az alkalmazás-átjárónak a nevét adja meg, amelyre a parancsmag hozzáadja az SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="02072-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="02072-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="02072-113">-CertificateFile</span></span>
<span data-ttu-id="02072-114">A parancsmag által hozzáadott SSL-tanúsítvány. pfx fájlja.</span><span class="sxs-lookup"><span data-stu-id="02072-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="02072-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02072-115">-DefaultProfile</span></span>
<span data-ttu-id="02072-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02072-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02072-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="02072-117">-Name</span></span>
<span data-ttu-id="02072-118">Annak az SSL-tanúsítványnak a neve, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="02072-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="02072-119">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="02072-119">-Password</span></span>
<span data-ttu-id="02072-120">Annak az SSL-tanúsítványnak a jelszava, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="02072-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="02072-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02072-121">CommonParameters</span></span>
<span data-ttu-id="02072-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="02072-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02072-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02072-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02072-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="02072-124">INPUTS</span></span>

### <span data-ttu-id="02072-125">System. String</span><span class="sxs-lookup"><span data-stu-id="02072-125">System.String</span></span>

## <span data-ttu-id="02072-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02072-126">OUTPUTS</span></span>

### <span data-ttu-id="02072-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02072-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="02072-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="02072-128">NOTES</span></span>

## <span data-ttu-id="02072-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02072-129">RELATED LINKS</span></span>

[<span data-ttu-id="02072-130">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="02072-130">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="02072-131">Új – AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="02072-131">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="02072-132">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="02072-132">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="02072-133">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="02072-133">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


