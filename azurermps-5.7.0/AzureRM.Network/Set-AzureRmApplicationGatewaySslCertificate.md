---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 1af7ef3b60fa296a5fb8190675393a0726d0502b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493728"
---
# <span data-ttu-id="a9168-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a9168-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="a9168-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9168-102">SYNOPSIS</span></span>
<span data-ttu-id="a9168-103">Az SSL-tanúsítványok cél állapotának beállítására.</span><span class="sxs-lookup"><span data-stu-id="a9168-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9168-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9168-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9168-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9168-105">DESCRIPTION</span></span>
<span data-ttu-id="a9168-106">A **set-AzureRmApplicationGatewaySslCertificate** PARANCSMAG egy SSL-tanúsítvány cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="a9168-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="a9168-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a9168-107">EXAMPLES</span></span>

### <span data-ttu-id="a9168-108">Példa 1: az SSL-tanúsítványok célérték-állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="a9168-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="a9168-109">Ez a parancs a ApplicationGateway01 nevű alkalmazás-átjáróból állítja be az SSL-tanúsítványok céljának állapotát.</span><span class="sxs-lookup"><span data-stu-id="a9168-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="a9168-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9168-110">PARAMETERS</span></span>

### <span data-ttu-id="a9168-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a9168-111">-ApplicationGateway</span></span>
<span data-ttu-id="a9168-112">Annak az alkalmazásnak az átjáróját adja meg, amelyhez a Secure Socket Layer (SSL) tanúsítvány van társítva.</span><span class="sxs-lookup"><span data-stu-id="a9168-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="a9168-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a9168-113">-CertificateFile</span></span>
<span data-ttu-id="a9168-114">Az SSL-tanúsítvány elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9168-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="a9168-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9168-115">-DefaultProfile</span></span>
<span data-ttu-id="a9168-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9168-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9168-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a9168-117">-Name</span></span>
<span data-ttu-id="a9168-118">Az SSL-tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9168-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="a9168-119">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="a9168-119">-Password</span></span>
<span data-ttu-id="a9168-120">Az SSL-tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a9168-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="a9168-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9168-121">CommonParameters</span></span>
<span data-ttu-id="a9168-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9168-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9168-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9168-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9168-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9168-124">INPUTS</span></span>

### <span data-ttu-id="a9168-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a9168-125">System.String</span></span>

## <span data-ttu-id="a9168-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9168-126">OUTPUTS</span></span>

### <span data-ttu-id="a9168-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a9168-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a9168-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9168-128">NOTES</span></span>

## <span data-ttu-id="a9168-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9168-129">RELATED LINKS</span></span>

[<span data-ttu-id="a9168-130">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a9168-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a9168-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a9168-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a9168-132">Új – AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a9168-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a9168-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a9168-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


