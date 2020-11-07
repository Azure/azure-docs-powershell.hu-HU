---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b68f0bf3b0112587256fddc3dbb6c31605f811b7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843665"
---
# <span data-ttu-id="944cb-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="944cb-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="944cb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="944cb-102">SYNOPSIS</span></span>
<span data-ttu-id="944cb-103">Az SSL-tanúsítványok cél állapotának beállítására.</span><span class="sxs-lookup"><span data-stu-id="944cb-103">Sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="944cb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="944cb-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="944cb-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="944cb-105">DESCRIPTION</span></span>
<span data-ttu-id="944cb-106">A **set-AzApplicationGatewaySslCertificate** PARANCSMAG egy SSL-tanúsítvány cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="944cb-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="944cb-107">Példák</span><span class="sxs-lookup"><span data-stu-id="944cb-107">EXAMPLES</span></span>

### <span data-ttu-id="944cb-108">Példa 1: az SSL-tanúsítványok célérték-állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="944cb-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="944cb-109">Ez a parancs a ApplicationGateway01 nevű alkalmazás-átjáróból állítja be az SSL-tanúsítványok céljának állapotát.</span><span class="sxs-lookup"><span data-stu-id="944cb-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="944cb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="944cb-110">PARAMETERS</span></span>

### <span data-ttu-id="944cb-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="944cb-111">-ApplicationGateway</span></span>
<span data-ttu-id="944cb-112">Annak az alkalmazásnak az átjáróját adja meg, amelyhez a Secure Socket Layer (SSL) tanúsítvány van társítva.</span><span class="sxs-lookup"><span data-stu-id="944cb-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="944cb-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="944cb-113">-CertificateFile</span></span>
<span data-ttu-id="944cb-114">Az SSL-tanúsítvány elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="944cb-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="944cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="944cb-115">-DefaultProfile</span></span>
<span data-ttu-id="944cb-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="944cb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="944cb-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="944cb-117">-Name</span></span>
<span data-ttu-id="944cb-118">Az SSL-tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="944cb-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="944cb-119">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="944cb-119">-Password</span></span>
<span data-ttu-id="944cb-120">Az SSL-tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="944cb-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="944cb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="944cb-121">CommonParameters</span></span>
<span data-ttu-id="944cb-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="944cb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="944cb-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="944cb-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="944cb-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="944cb-124">INPUTS</span></span>

### <span data-ttu-id="944cb-125">System. String</span><span class="sxs-lookup"><span data-stu-id="944cb-125">System.String</span></span>

## <span data-ttu-id="944cb-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="944cb-126">OUTPUTS</span></span>

### <span data-ttu-id="944cb-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="944cb-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="944cb-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="944cb-128">NOTES</span></span>

## <span data-ttu-id="944cb-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="944cb-129">RELATED LINKS</span></span>

[<span data-ttu-id="944cb-130">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="944cb-130">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="944cb-131">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="944cb-131">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="944cb-132">Új – AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="944cb-132">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="944cb-133">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="944cb-133">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


