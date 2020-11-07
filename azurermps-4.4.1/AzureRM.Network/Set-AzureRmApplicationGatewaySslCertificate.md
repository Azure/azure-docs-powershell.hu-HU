---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: cec5a6aa0b61889e7923ebce67d1247f99d215e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679976"
---
# <span data-ttu-id="f3586-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f3586-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="f3586-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f3586-102">SYNOPSIS</span></span>
<span data-ttu-id="f3586-103">Az SSL-tanúsítványok cél állapotának beállítására.</span><span class="sxs-lookup"><span data-stu-id="f3586-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3586-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f3586-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3586-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f3586-105">DESCRIPTION</span></span>
<span data-ttu-id="f3586-106">A **set-AzureRmApplicationGatewaySslCertificate** PARANCSMAG egy SSL-tanúsítvány cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="f3586-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="f3586-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f3586-107">EXAMPLES</span></span>

### <span data-ttu-id="f3586-108">Példa 1: az SSL-tanúsítványok célérték-állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="f3586-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="f3586-109">Ez a parancs a ApplicationGateway01 nevű alkalmazás-átjáróból állítja be az SSL-tanúsítványok céljának állapotát.</span><span class="sxs-lookup"><span data-stu-id="f3586-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="f3586-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f3586-110">PARAMETERS</span></span>

### <span data-ttu-id="f3586-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3586-111">-ApplicationGateway</span></span>
<span data-ttu-id="f3586-112">Annak az alkalmazásnak az átjáróját adja meg, amelyhez a Secure Socket Layer (SSL) tanúsítvány van társítva.</span><span class="sxs-lookup"><span data-stu-id="f3586-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3586-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f3586-113">-CertificateFile</span></span>
<span data-ttu-id="f3586-114">Az SSL-tanúsítvány elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3586-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="f3586-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f3586-115">-Name</span></span>
<span data-ttu-id="f3586-116">Az SSL-tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3586-116">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="f3586-117">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="f3586-117">-Password</span></span>
<span data-ttu-id="f3586-118">Az SSL-tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f3586-118">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="f3586-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3586-119">-DefaultProfile</span></span>
<span data-ttu-id="f3586-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f3586-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3586-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3586-121">CommonParameters</span></span>
<span data-ttu-id="f3586-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f3586-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3586-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3586-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3586-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3586-124">INPUTS</span></span>

### <span data-ttu-id="f3586-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f3586-125">System.String</span></span>

## <span data-ttu-id="f3586-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f3586-126">OUTPUTS</span></span>

### <span data-ttu-id="f3586-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f3586-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f3586-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f3586-128">NOTES</span></span>

## <span data-ttu-id="f3586-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f3586-129">RELATED LINKS</span></span>

[<span data-ttu-id="f3586-130">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f3586-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f3586-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f3586-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f3586-132">Új – AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f3586-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="f3586-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="f3586-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


