---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 60d46a3d61f0799618107e9bc0727a3ff31fc337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841382"
---
# <span data-ttu-id="b5285-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5285-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b5285-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b5285-102">SYNOPSIS</span></span>
<span data-ttu-id="b5285-103">Az Azure Application Gateway rendszerhez létrehoz egy SSL-tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="b5285-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b5285-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b5285-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> -CertificateFile <String> -Password <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5285-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b5285-105">DESCRIPTION</span></span>
<span data-ttu-id="b5285-106">A **New-AzApplicationGatewaySslCertificate** parancsmag létrehoz egy SSL-tanúsítványt egy Azure Application Gateway-nek.</span><span class="sxs-lookup"><span data-stu-id="b5285-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="b5285-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b5285-107">EXAMPLES</span></span>

### <span data-ttu-id="b5285-108">1. példa: SSL-tanúsítvány létrehozása Azure Application Gateway rendszerhez</span><span class="sxs-lookup"><span data-stu-id="b5285-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="b5285-109">Ez a parancs létrehoz egy Cert01 nevű SSL-tanúsítványt az alapértelmezett alkalmazás-átjáróhoz, és az eredményt az $Cert nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="b5285-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

## <span data-ttu-id="b5285-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b5285-110">PARAMETERS</span></span>

### <span data-ttu-id="b5285-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b5285-111">-CertificateFile</span></span>
<span data-ttu-id="b5285-112">Annak az SSL-tanúsítványnak a. PFX fájljának elérési útját adja meg, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5285-112">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b5285-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5285-113">-DefaultProfile</span></span>
<span data-ttu-id="b5285-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5285-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5285-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b5285-115">-Name</span></span>
<span data-ttu-id="b5285-116">Annak az SSL-tanúsítványnak a neve, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5285-116">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b5285-117">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="b5285-117">-Password</span></span>
<span data-ttu-id="b5285-118">Annak az SSL-nek a jelszava, amelyet a parancsmag hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b5285-118">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b5285-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5285-119">CommonParameters</span></span>
<span data-ttu-id="b5285-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b5285-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5285-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5285-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5285-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5285-122">INPUTS</span></span>

### <span data-ttu-id="b5285-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b5285-123">System.String</span></span>

## <span data-ttu-id="b5285-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5285-124">OUTPUTS</span></span>

### <span data-ttu-id="b5285-125">Microsoft. Azure. commands. Network. models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5285-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="b5285-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b5285-126">NOTES</span></span>

## <span data-ttu-id="b5285-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5285-127">RELATED LINKS</span></span>

[<span data-ttu-id="b5285-128">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5285-128">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b5285-129">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5285-129">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b5285-130">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5285-130">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="b5285-131">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5285-131">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


