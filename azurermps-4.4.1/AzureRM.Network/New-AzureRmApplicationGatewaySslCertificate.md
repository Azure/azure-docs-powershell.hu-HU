---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: ad318c776662ebaeab3192ca584aa2aad7f2e20a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495546"
---
# <span data-ttu-id="cbf85-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cbf85-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="cbf85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cbf85-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf85-103">Az Azure Application Gateway rendszerhez létrehoz egy SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="cbf85-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbf85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cbf85-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbf85-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cbf85-105">DESCRIPTION</span></span>
<span data-ttu-id="cbf85-106">A **New-AzureRmApplicationGatewaySslCertificate** parancsmag létrehoz egy SSL-tanúsítványt egy Azure Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="cbf85-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="cbf85-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cbf85-107">EXAMPLES</span></span>

### <span data-ttu-id="cbf85-108">1. példa: SSL-tanúsítvány létrehozása Azure Application Gateway rendszerhez</span><span class="sxs-lookup"><span data-stu-id="cbf85-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\>$Cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="cbf85-109">Ez a parancs létrehoz egy Cert01 nevű SSL-tanúsítványt az alapértelmezett alkalmazás-átjáróhoz, és az eredményt az $Cert nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="cbf85-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="cbf85-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cbf85-110">PARAMETERS</span></span>

### <span data-ttu-id="cbf85-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cbf85-111">-CertificateFile</span></span>
<span data-ttu-id="cbf85-112">Annak az SSL-tanúsítványnak a. PFX fájljának elérési útját adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cbf85-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cbf85-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cbf85-113">-Name</span></span>
<span data-ttu-id="cbf85-114">Annak az SSL-tanúsítványnak a neve, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cbf85-114">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cbf85-115">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="cbf85-115">-Password</span></span>
<span data-ttu-id="cbf85-116">Annak az SSL-nek a jelszava, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cbf85-116">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cbf85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf85-117">-DefaultProfile</span></span>
<span data-ttu-id="cbf85-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbf85-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbf85-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf85-119">CommonParameters</span></span>
<span data-ttu-id="cbf85-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cbf85-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf85-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbf85-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf85-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbf85-122">INPUTS</span></span>

### <span data-ttu-id="cbf85-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cbf85-123">System.String</span></span>

## <span data-ttu-id="cbf85-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbf85-124">OUTPUTS</span></span>

### <span data-ttu-id="cbf85-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cbf85-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="cbf85-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cbf85-126">NOTES</span></span>

## <span data-ttu-id="cbf85-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbf85-127">RELATED LINKS</span></span>

[<span data-ttu-id="cbf85-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cbf85-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cbf85-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cbf85-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cbf85-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cbf85-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cbf85-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cbf85-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


