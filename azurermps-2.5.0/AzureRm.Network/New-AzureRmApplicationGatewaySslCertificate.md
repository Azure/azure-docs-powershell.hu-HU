---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: e22760c2838cf0b4fb0597dbd45532374b604b79
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848434"
---
# <span data-ttu-id="e5590-101">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5590-101">New-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e5590-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e5590-102">SYNOPSIS</span></span>
<span data-ttu-id="e5590-103">Az Azure Application Gateway rendszerhez létrehoz egy SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="e5590-103">Creates an SSL certificate for an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5590-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e5590-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5590-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e5590-105">DESCRIPTION</span></span>
<span data-ttu-id="e5590-106">A **New-AzureRmApplicationGatewaySslCertificate** parancsmag létrehoz egy SSL-tanúsítványt egy Azure Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="e5590-106">The **New-AzureRmApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="e5590-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e5590-107">EXAMPLES</span></span>

### <span data-ttu-id="e5590-108">1. példa: SSL-tanúsítvány létrehozása Azure Application Gateway rendszerhez</span><span class="sxs-lookup"><span data-stu-id="e5590-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="e5590-109">Ez a parancs létrehoz egy Cert01 nevű SSL-tanúsítványt az alapértelmezett alkalmazás-átjáróhoz, és az eredményt az $Cert nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="e5590-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="e5590-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e5590-110">PARAMETERS</span></span>

### <span data-ttu-id="e5590-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e5590-111">-CertificateFile</span></span>
<span data-ttu-id="e5590-112">Annak az SSL-tanúsítványnak a. PFX fájljának elérési útját adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e5590-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e5590-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5590-113">-DefaultProfile</span></span>
<span data-ttu-id="e5590-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e5590-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5590-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e5590-115">-Name</span></span>
<span data-ttu-id="e5590-116">Annak az SSL-tanúsítványnak a neve, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e5590-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e5590-117">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="e5590-117">-Password</span></span>
<span data-ttu-id="e5590-118">Annak az SSL-nek a jelszava, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e5590-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="e5590-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5590-119">CommonParameters</span></span>
<span data-ttu-id="e5590-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e5590-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5590-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5590-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5590-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5590-122">INPUTS</span></span>

### <span data-ttu-id="e5590-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e5590-123">System.String</span></span>

## <span data-ttu-id="e5590-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e5590-124">OUTPUTS</span></span>

### <span data-ttu-id="e5590-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5590-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e5590-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e5590-126">NOTES</span></span>

## <span data-ttu-id="e5590-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e5590-127">RELATED LINKS</span></span>

[<span data-ttu-id="e5590-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5590-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e5590-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5590-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e5590-130">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5590-130">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e5590-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e5590-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


