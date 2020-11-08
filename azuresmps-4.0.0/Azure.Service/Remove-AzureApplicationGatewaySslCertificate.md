---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 98AC0FAA-4786-4172-908E-FEB8588B0D74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da9e9af2e96ee177a91dae7b7ccd12f7e588517
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016494"
---
# <span data-ttu-id="40a31-101">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="40a31-101">Remove-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="40a31-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40a31-102">SYNOPSIS</span></span>
<span data-ttu-id="40a31-103">Egy alkalmazás-átjárótól származó SSL-tanúsítvány eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="40a31-103">Removes an SSL certificate from an application gateway.</span></span>

## <span data-ttu-id="40a31-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40a31-104">SYNTAX</span></span>

```
Remove-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="40a31-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="40a31-105">DESCRIPTION</span></span>
<span data-ttu-id="40a31-106">A **Remove-AzureApplicationGatewaySslCertificate** parancsmag az alkalmazás-átjárók SSL-tanúsítványát távolítja el.</span><span class="sxs-lookup"><span data-stu-id="40a31-106">The **Remove-AzureApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an application gateway.</span></span>

## <span data-ttu-id="40a31-107">Példák</span><span class="sxs-lookup"><span data-stu-id="40a31-107">EXAMPLES</span></span>

### <span data-ttu-id="40a31-108">1. példa: SSL-tanúsítvány eltávolítása</span><span class="sxs-lookup"><span data-stu-id="40a31-108">Example 1: Remove an SSL certificate</span></span>
```
PS C:\> Remove-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="40a31-109">Ez a parancs eltávolítja a SslCertificate13 nevű SSL-tanúsítványt a ApplicationGateway08 nevű alkalmazás-átjáróból.</span><span class="sxs-lookup"><span data-stu-id="40a31-109">This command removes an SSL certificate named SslCertificate13 from the application gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="40a31-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40a31-110">PARAMETERS</span></span>

### <span data-ttu-id="40a31-111">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="40a31-111">-CertificateName</span></span>
<span data-ttu-id="40a31-112">Az SSL-tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40a31-112">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="40a31-113">Ez a parancsmag eltávolítja a paraméter által megadott tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="40a31-113">This cmdlet removes the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="40a31-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="40a31-114">-Name</span></span>
<span data-ttu-id="40a31-115">Annak az alkalmazás-átjárónak a neve, amelyből a parancsmag eltávolítja az SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="40a31-115">Specifies the name of the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="40a31-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="40a31-116">-Profile</span></span>
<span data-ttu-id="40a31-117">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="40a31-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="40a31-118">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="40a31-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40a31-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40a31-119">CommonParameters</span></span>
<span data-ttu-id="40a31-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40a31-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40a31-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40a31-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40a31-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40a31-122">INPUTS</span></span>

### <span data-ttu-id="40a31-123">System. String</span><span class="sxs-lookup"><span data-stu-id="40a31-123">System.String</span></span>

## <span data-ttu-id="40a31-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40a31-124">OUTPUTS</span></span>

### <span data-ttu-id="40a31-125">Microsoft. WindowsAzure. Management. ApplicationGateway. models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="40a31-125">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="40a31-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40a31-126">NOTES</span></span>

## <span data-ttu-id="40a31-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40a31-127">RELATED LINKS</span></span>

[<span data-ttu-id="40a31-128">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="40a31-128">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="40a31-129">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="40a31-129">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)
