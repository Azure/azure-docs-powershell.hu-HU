---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: bcc7335076a0f74c89cede8c6fed66f55d88ec9d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919586"
---
# <span data-ttu-id="83ca7-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="83ca7-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="83ca7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="83ca7-103">Előlapi portot hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="83ca7-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="83ca7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="83ca7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83ca7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="83ca7-105">DESCRIPTION</span></span>
<span data-ttu-id="83ca7-106">A **New-AzApplicationGatewayFrontendPort** parancsmag előtér-portot hoz létre egy Azure-alkalmazásátjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="83ca7-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="83ca7-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="83ca7-107">EXAMPLES</span></span>

### <span data-ttu-id="83ca7-108">1. példa: Példa1: Előlapi port létrehozása</span><span class="sxs-lookup"><span data-stu-id="83ca7-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="83ca7-109">Ez a parancs létrehoz egy FrontEndPort01 nevű előlapi portot a 80-as porton, és az eredményt a következő nevű változóban $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="83ca7-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="83ca7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83ca7-110">PARAMETERS</span></span>

### <span data-ttu-id="83ca7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83ca7-111">-DefaultProfile</span></span>
<span data-ttu-id="83ca7-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83ca7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83ca7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="83ca7-113">-Name</span></span>
<span data-ttu-id="83ca7-114">A parancsmag által létrehozott előlapi port nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="83ca7-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="83ca7-115">-Port</span><span class="sxs-lookup"><span data-stu-id="83ca7-115">-Port</span></span>
<span data-ttu-id="83ca7-116">Az előlapi port portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="83ca7-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="83ca7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83ca7-117">CommonParameters</span></span>
<span data-ttu-id="83ca7-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83ca7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83ca7-119">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83ca7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83ca7-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83ca7-120">INPUTS</span></span>

### <span data-ttu-id="83ca7-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="83ca7-121">None</span></span>

## <span data-ttu-id="83ca7-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83ca7-122">OUTPUTS</span></span>

### <span data-ttu-id="83ca7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="83ca7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="83ca7-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="83ca7-124">NOTES</span></span>

## <span data-ttu-id="83ca7-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83ca7-125">RELATED LINKS</span></span>

[<span data-ttu-id="83ca7-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="83ca7-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="83ca7-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="83ca7-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="83ca7-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="83ca7-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="83ca7-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="83ca7-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


