---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: f8b9d6b981300c32badbe69ec153865c04814dd6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849961"
---
# <span data-ttu-id="9fc01-101">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9fc01-101">New-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="9fc01-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9fc01-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc01-103">Előtér-portot hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="9fc01-103">Creates a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fc01-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9fc01-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fc01-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9fc01-105">DESCRIPTION</span></span>
<span data-ttu-id="9fc01-106">A **New-AzureRmApplicationGatewayFrontendPort** parancsmag létrehoz egy előtér-portot az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="9fc01-106">The **New-AzureRmApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="9fc01-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9fc01-107">EXAMPLES</span></span>

### <span data-ttu-id="9fc01-108">Example1: előtér-port létrehozása</span><span class="sxs-lookup"><span data-stu-id="9fc01-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="9fc01-109">Ez a parancs létrehoz egy FrontEndPort01 nevű előtér-portot a 80-es porton, és az eredményt az $FrontEndPort nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="9fc01-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="9fc01-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9fc01-110">PARAMETERS</span></span>

### <span data-ttu-id="9fc01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc01-111">-DefaultProfile</span></span>
<span data-ttu-id="9fc01-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9fc01-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fc01-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9fc01-113">-Name</span></span>
<span data-ttu-id="9fc01-114">A parancsmag által létrehozott előtér-port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fc01-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9fc01-115">-Port</span><span class="sxs-lookup"><span data-stu-id="9fc01-115">-Port</span></span>
<span data-ttu-id="9fc01-116">Az előtér-port portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9fc01-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc01-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc01-117">CommonParameters</span></span>
<span data-ttu-id="9fc01-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9fc01-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc01-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fc01-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc01-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fc01-120">INPUTS</span></span>

### <span data-ttu-id="9fc01-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9fc01-121">System.String</span></span>

## <span data-ttu-id="9fc01-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fc01-122">OUTPUTS</span></span>

### <span data-ttu-id="9fc01-123">Microsoft. Azure. commands. Network. models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9fc01-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="9fc01-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9fc01-124">NOTES</span></span>

## <span data-ttu-id="9fc01-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fc01-125">RELATED LINKS</span></span>

[<span data-ttu-id="9fc01-126">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9fc01-126">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="9fc01-127">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9fc01-127">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="9fc01-128">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9fc01-128">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="9fc01-129">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9fc01-129">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


