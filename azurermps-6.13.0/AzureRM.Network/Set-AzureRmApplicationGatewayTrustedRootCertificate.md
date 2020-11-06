---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 0505f7452c20c0bdb3ccf3a9bc203380479083ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491908"
---
# <span data-ttu-id="2e3e8-101">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2e3e8-101">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="2e3e8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2e3e8-102">SYNOPSIS</span></span>
<span data-ttu-id="2e3e8-103">Egy alkalmazás-átjáró megbízható főtanúsítványát frissíti.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e3e8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2e3e8-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e3e8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2e3e8-105">DESCRIPTION</span></span>
<span data-ttu-id="2e3e8-106">A **set-AzureRmApplicationGatewayTrustedRootCertificate** parancsmag módosította az alkalmazás-átjárók meglévő megbízható főtanúsítványát.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-106">The **Set-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="2e3e8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2e3e8-107">EXAMPLES</span></span>

### <span data-ttu-id="2e3e8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2e3e8-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="2e3e8-109">A fenti példa szerint az esetek azt mutatják be, hogy miként frissíthet egy meglévő megbízható főtanúsítványt a főtanúsítvány bedobásakor.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="2e3e8-110">Az első parancs beolvassa az Application Gatewayt, és a $gw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="2e3e8-111">A második parancs módosította a meglévő megbízható főtanúsítványot egy új főtanúsítványsal.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="2e3e8-112">A harmadik parancs az Azure rendszerhez frissíti az Application Gatewayt.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="2e3e8-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2e3e8-113">PARAMETERS</span></span>

### <span data-ttu-id="2e3e8-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e3e8-114">-ApplicationGateway</span></span>
<span data-ttu-id="2e3e8-115">A applicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e3e8-115">The applicationGateway</span></span>

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

### <span data-ttu-id="2e3e8-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="2e3e8-116">-CertificateFile</span></span>
<span data-ttu-id="2e3e8-117">A bizonyítvány CER-fájljának elérési útja</span><span class="sxs-lookup"><span data-stu-id="2e3e8-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="2e3e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e3e8-118">-DefaultProfile</span></span>
<span data-ttu-id="2e3e8-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e3e8-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2e3e8-120">-Name</span></span>
<span data-ttu-id="2e3e8-121">A TrustedRoot tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="2e3e8-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="2e3e8-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2e3e8-122">-Confirm</span></span>
<span data-ttu-id="2e3e8-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3e8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e3e8-124">-WhatIf</span></span>
<span data-ttu-id="2e3e8-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e3e8-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2e3e8-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e3e8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e3e8-127">CommonParameters</span></span>
<span data-ttu-id="2e3e8-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2e3e8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e3e8-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e3e8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e3e8-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e3e8-130">INPUTS</span></span>

### <span data-ttu-id="2e3e8-131">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e3e8-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2e3e8-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2e3e8-132">OUTPUTS</span></span>

### <span data-ttu-id="2e3e8-133">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e3e8-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2e3e8-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2e3e8-134">NOTES</span></span>

## <span data-ttu-id="2e3e8-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2e3e8-135">RELATED LINKS</span></span>
