---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 26b6bc0128929efda2baf52979e1b6c2ecdbd714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837508"
---
# <span data-ttu-id="90a8f-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="90a8f-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="90a8f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="90a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="90a8f-103">Előtér-portot hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="90a8f-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="90a8f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="90a8f-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90a8f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="90a8f-105">DESCRIPTION</span></span>
<span data-ttu-id="90a8f-106">A **New-AzApplicationGatewayFrontendPort** parancsmag létrehoz egy előtér-portot az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="90a8f-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="90a8f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="90a8f-107">EXAMPLES</span></span>

### <span data-ttu-id="90a8f-108">Example1: előtér-port létrehozása</span><span class="sxs-lookup"><span data-stu-id="90a8f-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="90a8f-109">Ez a parancs létrehoz egy FrontEndPort01 nevű előtér-portot a 80-es porton, és az eredményt az $FrontEndPort nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="90a8f-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="90a8f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="90a8f-110">PARAMETERS</span></span>

### <span data-ttu-id="90a8f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90a8f-111">-DefaultProfile</span></span>
<span data-ttu-id="90a8f-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90a8f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a8f-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="90a8f-113">-Name</span></span>
<span data-ttu-id="90a8f-114">A parancsmag által létrehozott előtér-port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a8f-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="90a8f-115">-Port</span><span class="sxs-lookup"><span data-stu-id="90a8f-115">-Port</span></span>
<span data-ttu-id="90a8f-116">Az előtér-port portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="90a8f-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90a8f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90a8f-117">CommonParameters</span></span>
<span data-ttu-id="90a8f-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="90a8f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90a8f-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90a8f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90a8f-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="90a8f-120">INPUTS</span></span>

### <span data-ttu-id="90a8f-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="90a8f-121">None</span></span>

## <span data-ttu-id="90a8f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90a8f-122">OUTPUTS</span></span>

### <span data-ttu-id="90a8f-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="90a8f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="90a8f-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="90a8f-124">NOTES</span></span>

## <span data-ttu-id="90a8f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90a8f-125">RELATED LINKS</span></span>

[<span data-ttu-id="90a8f-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="90a8f-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="90a8f-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="90a8f-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="90a8f-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="90a8f-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="90a8f-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="90a8f-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


