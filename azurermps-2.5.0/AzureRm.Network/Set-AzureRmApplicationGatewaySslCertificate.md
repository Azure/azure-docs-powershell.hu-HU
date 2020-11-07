---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: bb295ba9f1b7c446e8f8fd6e80d8445774bf8852
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849086"
---
# <span data-ttu-id="80a92-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="80a92-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="80a92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="80a92-102">SYNOPSIS</span></span>
<span data-ttu-id="80a92-103">Az SSL-tanúsítványok cél állapotának beállítására.</span><span class="sxs-lookup"><span data-stu-id="80a92-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80a92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="80a92-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80a92-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="80a92-105">DESCRIPTION</span></span>
<span data-ttu-id="80a92-106">A **set-AzureRmApplicationGatewaySslCertificate** PARANCSMAG egy SSL-tanúsítvány cél állapotát állítja be.</span><span class="sxs-lookup"><span data-stu-id="80a92-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="80a92-107">Példák</span><span class="sxs-lookup"><span data-stu-id="80a92-107">EXAMPLES</span></span>

### <span data-ttu-id="80a92-108">Példa 1: az SSL-tanúsítványok célérték-állapotának beállítása</span><span class="sxs-lookup"><span data-stu-id="80a92-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="80a92-109">Ez a parancs a ApplicationGateway01 nevű alkalmazás-átjáróból állítja be az SSL-tanúsítványok céljának állapotát.</span><span class="sxs-lookup"><span data-stu-id="80a92-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="80a92-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="80a92-110">PARAMETERS</span></span>

### <span data-ttu-id="80a92-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80a92-111">-ApplicationGateway</span></span>
<span data-ttu-id="80a92-112">Annak az alkalmazásnak az átjáróját adja meg, amelyhez a Secure Socket Layer (SSL) tanúsítvány van társítva.</span><span class="sxs-lookup"><span data-stu-id="80a92-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="80a92-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="80a92-113">-CertificateFile</span></span>
<span data-ttu-id="80a92-114">Az SSL-tanúsítvány elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="80a92-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="80a92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a92-115">-DefaultProfile</span></span>
<span data-ttu-id="80a92-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="80a92-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80a92-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="80a92-117">-Name</span></span>
<span data-ttu-id="80a92-118">Az SSL-tanúsítvány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="80a92-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="80a92-119">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="80a92-119">-Password</span></span>
<span data-ttu-id="80a92-120">Az SSL-tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="80a92-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="80a92-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a92-121">CommonParameters</span></span>
<span data-ttu-id="80a92-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="80a92-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a92-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80a92-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a92-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="80a92-124">INPUTS</span></span>

### <span data-ttu-id="80a92-125">System. String</span><span class="sxs-lookup"><span data-stu-id="80a92-125">System.String</span></span>

## <span data-ttu-id="80a92-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="80a92-126">OUTPUTS</span></span>

### <span data-ttu-id="80a92-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80a92-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="80a92-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="80a92-128">NOTES</span></span>

## <span data-ttu-id="80a92-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="80a92-129">RELATED LINKS</span></span>

[<span data-ttu-id="80a92-130">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="80a92-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="80a92-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="80a92-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="80a92-132">Új – AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="80a92-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="80a92-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="80a92-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


