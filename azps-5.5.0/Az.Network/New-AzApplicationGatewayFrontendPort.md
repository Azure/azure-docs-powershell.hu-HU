---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: dc5a0fb99ca3ce41447cc95ebb42490b88379f83
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202943"
---
# <span data-ttu-id="6a722-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6a722-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="6a722-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a722-102">SYNOPSIS</span></span>
<span data-ttu-id="6a722-103">Előlapi portot hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="6a722-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="6a722-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6a722-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a722-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6a722-105">DESCRIPTION</span></span>
<span data-ttu-id="6a722-106">A **New-AzApplicationGatewayFrontendPort** parancsmag előtér-portot hoz létre egy Azure-alkalmazásátjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="6a722-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="6a722-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6a722-107">EXAMPLES</span></span>

### <span data-ttu-id="6a722-108">1. példa: Példa1: Előlapi port létrehozása</span><span class="sxs-lookup"><span data-stu-id="6a722-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="6a722-109">Ez a parancs létrehoz egy FrontEndPort01 nevű előlapi portot a 80-as porton, és az eredményt a következő nevű változóban $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="6a722-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="6a722-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a722-110">PARAMETERS</span></span>

### <span data-ttu-id="6a722-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a722-111">-DefaultProfile</span></span>
<span data-ttu-id="6a722-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6a722-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a722-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6a722-113">-Name</span></span>
<span data-ttu-id="6a722-114">A parancsmag által létrehozott előlapi port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a722-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6a722-115">-Port</span><span class="sxs-lookup"><span data-stu-id="6a722-115">-Port</span></span>
<span data-ttu-id="6a722-116">Az előlapi port portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6a722-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="6a722-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a722-117">CommonParameters</span></span>
<span data-ttu-id="6a722-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a722-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a722-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a722-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a722-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a722-120">INPUTS</span></span>

### <span data-ttu-id="6a722-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="6a722-121">None</span></span>

## <span data-ttu-id="6a722-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6a722-122">OUTPUTS</span></span>

### <span data-ttu-id="6a722-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6a722-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="6a722-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6a722-124">NOTES</span></span>

## <span data-ttu-id="6a722-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6a722-125">RELATED LINKS</span></span>

[<span data-ttu-id="6a722-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6a722-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6a722-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6a722-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6a722-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6a722-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="6a722-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="6a722-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


