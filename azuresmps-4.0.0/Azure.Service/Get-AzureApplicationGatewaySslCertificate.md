---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D2CE5D4B-8F1F-41FF-9E65-8956FEDD35AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4fad7ae6eab4b71febbd2ffe1f6c9002186ee8d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015664"
---
# <span data-ttu-id="ae776-101">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ae776-101">Get-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="ae776-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ae776-102">SYNOPSIS</span></span>
<span data-ttu-id="ae776-103">Az alkalmazás-átjáró tanúsítványait kapja.</span><span class="sxs-lookup"><span data-stu-id="ae776-103">Gets Application Gateway certificates.</span></span>

## <span data-ttu-id="ae776-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ae776-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewaySslCertificate -Name <String> [-CertificateName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ae776-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ae776-105">DESCRIPTION</span></span>
<span data-ttu-id="ae776-106">A **Get-AzureApplicationGatewaySslCertificate** parancsmag Secure Sockets Layer (SSL) tanúsítványokat kap az Azure Application Gateway rendszerhez.</span><span class="sxs-lookup"><span data-stu-id="ae776-106">The **Get-AzureApplicationGatewaySslCertificate** cmdlet gets Secure Sockets Layer (SSL) certificates for an Azure Application Gateway.</span></span>

## <span data-ttu-id="ae776-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ae776-107">EXAMPLES</span></span>

### <span data-ttu-id="ae776-108">Példa 1: SSL-tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="ae776-108">Example 1: Get an SSL certificate</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="ae776-109">Ez a parancs egy SslCertificate13 nevű SSL-tanúsítványt kap a ApplicationGateway08 nevű alkalmazás-átjáróban.</span><span class="sxs-lookup"><span data-stu-id="ae776-109">This command gets an SSL certificate named SslCertificate13 on the Application Gateway named ApplicationGateway08.</span></span>

### <span data-ttu-id="ae776-110">2. példa: az összes SSL-tanúsítvány beszerzése</span><span class="sxs-lookup"><span data-stu-id="ae776-110">Example 2: Get all SSL certificates</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08"
```

<span data-ttu-id="ae776-111">Ez a parancs a ApplicationGateway08 nevű alkalmazás-átjáró összes SSL-tanúsítványát lekapja.</span><span class="sxs-lookup"><span data-stu-id="ae776-111">This command gets all the SSL certificates on the Application Gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="ae776-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ae776-112">PARAMETERS</span></span>

### <span data-ttu-id="ae776-113">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ae776-113">-CertificateName</span></span>
<span data-ttu-id="ae776-114">Az SSL-tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ae776-114">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="ae776-115">Ez a parancsmag a paraméter által megadott tanúsítványt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ae776-115">This cmdlet gets the certificate that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae776-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ae776-116">-Name</span></span>
<span data-ttu-id="ae776-117">Annak az alkalmazás-átjárónak a neve, amelyből a parancsmag az SSL-tanúsítványt kapja.</span><span class="sxs-lookup"><span data-stu-id="ae776-117">Specifies the name of the Application Gateway from which this cmdlet gets an SSL certificate.</span></span>

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

### <span data-ttu-id="ae776-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="ae776-118">-Profile</span></span>
<span data-ttu-id="ae776-119">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="ae776-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae776-120">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="ae776-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae776-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae776-121">CommonParameters</span></span>
<span data-ttu-id="ae776-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ae776-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae776-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae776-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae776-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae776-124">INPUTS</span></span>

### <span data-ttu-id="ae776-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ae776-125">System.String</span></span>

## <span data-ttu-id="ae776-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae776-126">OUTPUTS</span></span>

### <span data-ttu-id="ae776-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate, List<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate></span><span class="sxs-lookup"><span data-stu-id="ae776-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate, List<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate></span></span>

## <span data-ttu-id="ae776-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ae776-128">NOTES</span></span>

## <span data-ttu-id="ae776-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae776-129">RELATED LINKS</span></span>

[<span data-ttu-id="ae776-130">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ae776-130">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ae776-131">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ae776-131">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
