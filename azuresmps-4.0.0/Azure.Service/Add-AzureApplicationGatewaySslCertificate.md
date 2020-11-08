---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BA63476C-25CC-444D-AD2C-51BF76374FBC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76ac1f2d1ba5c64fb12bc10320efff8c34538ab8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015736"
---
# <span data-ttu-id="b688a-101">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b688a-101">Add-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b688a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b688a-102">SYNOPSIS</span></span>
<span data-ttu-id="b688a-103">SSL-tanúsítványt ad hozzá egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b688a-103">Adds an SSL certificate to an Application Gateway.</span></span>

## <span data-ttu-id="b688a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b688a-104">SYNTAX</span></span>

```
Add-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String> -Password <String>
 -CertificateFile <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b688a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b688a-105">DESCRIPTION</span></span>
<span data-ttu-id="b688a-106">Az **Add-AzureApplicationGatewaySslCertificate** parancsmag egy biztonságos szoftvercsatorna-RÉTEGET (SSL-tanúsítványt) ad az Azure Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="b688a-106">The **Add-AzureApplicationGatewaySslCertificate** cmdlet adds a Secure Sockets Layer (SSL) certificate to an Azure Application Gateway.</span></span>

## <span data-ttu-id="b688a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b688a-107">EXAMPLES</span></span>

### <span data-ttu-id="b688a-108">1. példa: SSL-tanúsítvány felvétele</span><span class="sxs-lookup"><span data-stu-id="b688a-108">Example 1: Add an SSL certificate</span></span>
```
PS C:\> Add-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13" -Password "password" -CertificateFile "c:\Certs\sslCertificate.pfx"
```

<span data-ttu-id="b688a-109">Ez a parancs hozzáadja a SslCertificate13 nevű SSL-tanúsítványt a ApplicationGateway08 nevű alkalmazási átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="b688a-109">This command adds an SSL certificate named SslCertificate13 to the Application Gateway named ApplicationGateway08.</span></span>
<span data-ttu-id="b688a-110">A parancs a tanúsítványfájl elérési útját és a tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="b688a-110">The command specifies the path of the certificate file and the password for the certificate.</span></span>

## <span data-ttu-id="b688a-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b688a-111">PARAMETERS</span></span>

### <span data-ttu-id="b688a-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b688a-112">-CertificateFile</span></span>
<span data-ttu-id="b688a-113">Az SSL-tanúsítványfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="b688a-113">Specifies the path of an SSL certificate file.</span></span>
<span data-ttu-id="b688a-114">Ez a parancsmag hozzáadja a tanúsítványt a fájlban, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="b688a-114">This cmdlet adds the certificate in the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="b688a-115">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="b688a-115">-CertificateName</span></span>
<span data-ttu-id="b688a-116">Az SSL-tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b688a-116">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="b688a-117">Ez a parancsmag hozzáadja a paramétert megadó tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="b688a-117">This cmdlet adds the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="b688a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b688a-118">-Name</span></span>
<span data-ttu-id="b688a-119">Annak az alkalmazásnak az átjárójának a neve, amelyhez a parancsmag hozzáadja az SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="b688a-119">Specifies the name of the Application Gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="b688a-120">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="b688a-120">-Password</span></span>
<span data-ttu-id="b688a-121">Annak az SSL-tanúsítványnak a jelszava, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="b688a-121">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="b688a-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="b688a-122">-Profile</span></span>
<span data-ttu-id="b688a-123">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="b688a-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b688a-124">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="b688a-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b688a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b688a-125">CommonParameters</span></span>
<span data-ttu-id="b688a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b688a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b688a-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b688a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b688a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b688a-128">INPUTS</span></span>

### <span data-ttu-id="b688a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b688a-129">System.String</span></span>

## <span data-ttu-id="b688a-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b688a-130">OUTPUTS</span></span>

### <span data-ttu-id="b688a-131">Microsoft. WindowsAzure. Management. ApplicationGateway. models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b688a-131">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="b688a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b688a-132">NOTES</span></span>

## <span data-ttu-id="b688a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b688a-133">RELATED LINKS</span></span>

[<span data-ttu-id="b688a-134">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b688a-134">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b688a-135">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b688a-135">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
