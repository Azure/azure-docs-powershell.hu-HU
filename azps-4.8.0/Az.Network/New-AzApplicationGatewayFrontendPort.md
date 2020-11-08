---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: dc5a0fb99ca3ce41447cc95ebb42490b88379f83
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183027"
---
# <span data-ttu-id="66b9e-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="66b9e-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="66b9e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66b9e-102">SYNOPSIS</span></span>
<span data-ttu-id="66b9e-103">Előtér-portot hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="66b9e-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="66b9e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66b9e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="66b9e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66b9e-105">DESCRIPTION</span></span>
<span data-ttu-id="66b9e-106">A **New-AzApplicationGatewayFrontendPort** parancsmag létrehoz egy előtér-portot az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="66b9e-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="66b9e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="66b9e-107">EXAMPLES</span></span>

### <span data-ttu-id="66b9e-108">Példa 1: Example1: előtér-végpont létrehozása</span><span class="sxs-lookup"><span data-stu-id="66b9e-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="66b9e-109">Ez a parancs létrehoz egy FrontEndPort01 nevű előtér-portot a 80-es porton, és az eredményt az $FrontEndPort nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="66b9e-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="66b9e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66b9e-110">PARAMETERS</span></span>

### <span data-ttu-id="66b9e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b9e-111">-DefaultProfile</span></span>
<span data-ttu-id="66b9e-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66b9e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66b9e-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="66b9e-113">-Name</span></span>
<span data-ttu-id="66b9e-114">A parancsmag által létrehozott előtér-port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="66b9e-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="66b9e-115">-Port</span><span class="sxs-lookup"><span data-stu-id="66b9e-115">-Port</span></span>
<span data-ttu-id="66b9e-116">Az előtér-port portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="66b9e-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="66b9e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b9e-117">CommonParameters</span></span>
<span data-ttu-id="66b9e-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66b9e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b9e-119">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66b9e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b9e-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66b9e-120">INPUTS</span></span>

### <span data-ttu-id="66b9e-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="66b9e-121">None</span></span>

## <span data-ttu-id="66b9e-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66b9e-122">OUTPUTS</span></span>

### <span data-ttu-id="66b9e-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="66b9e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="66b9e-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66b9e-124">NOTES</span></span>

## <span data-ttu-id="66b9e-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66b9e-125">RELATED LINKS</span></span>

[<span data-ttu-id="66b9e-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="66b9e-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="66b9e-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="66b9e-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="66b9e-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="66b9e-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="66b9e-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="66b9e-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


