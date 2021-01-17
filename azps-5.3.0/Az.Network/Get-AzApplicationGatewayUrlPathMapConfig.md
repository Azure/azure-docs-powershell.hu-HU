---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 50f80f8c7a191c43bb9e8b6b4aed5f44d1ecb85a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467390"
---
# <span data-ttu-id="3d5c0-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3d5c0-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="3d5c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d5c0-102">SYNOPSIS</span></span>
<span data-ttu-id="3d5c0-103">URL-útvonal-megfeleltetések tömbjét kapja vissza egy háttérkiszolgáló-készlethez.</span><span class="sxs-lookup"><span data-stu-id="3d5c0-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="3d5c0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3d5c0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d5c0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3d5c0-105">DESCRIPTION</span></span>
<span data-ttu-id="3d5c0-106">A **Get-AzApplicationGatewayURLPathMapConfig** parancsmag URL-útvonal-megfeleltetéseket tartalmazó tömböt kap egy háttérkiszolgáló-készlethez.</span><span class="sxs-lookup"><span data-stu-id="3d5c0-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="3d5c0-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3d5c0-107">EXAMPLES</span></span>

### <span data-ttu-id="3d5c0-108">1. példa: URL-útvonal-leképezés beállítása</span><span class="sxs-lookup"><span data-stu-id="3d5c0-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="3d5c0-109">Ez a parancs az URL-útvonal-leképezés beállításait az Átjáró nevű alkalmazás-átjárón található háttérkiszolgálóról kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3d5c0-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="3d5c0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d5c0-110">PARAMETERS</span></span>

### <span data-ttu-id="3d5c0-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d5c0-111">-ApplicationGateway</span></span>
<span data-ttu-id="3d5c0-112">Azt az alkalmazás-átjárót adja meg, amelyhez ez a parancsmag URL-útvonal-leképezés-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="3d5c0-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="3d5c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d5c0-113">-DefaultProfile</span></span>
<span data-ttu-id="3d5c0-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d5c0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d5c0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3d5c0-115">-Name</span></span>
<span data-ttu-id="3d5c0-116">Megadja annak az URL-útvonal-leképezésnek a nevét, amelyben a parancsmag beállítja az útvonal-leképezés konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="3d5c0-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d5c0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d5c0-117">CommonParameters</span></span>
<span data-ttu-id="3d5c0-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d5c0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d5c0-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d5c0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d5c0-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d5c0-120">INPUTS</span></span>

### <span data-ttu-id="3d5c0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d5c0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3d5c0-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d5c0-122">OUTPUTS</span></span>

### <span data-ttu-id="3d5c0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="3d5c0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="3d5c0-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3d5c0-124">NOTES</span></span>

## <span data-ttu-id="3d5c0-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d5c0-125">RELATED LINKS</span></span>

[<span data-ttu-id="3d5c0-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3d5c0-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3d5c0-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3d5c0-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3d5c0-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3d5c0-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="3d5c0-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="3d5c0-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


