---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 77CDEE77-FD5D-4C2D-B027-FF1F6FF6618E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGateway.md
ms.openlocfilehash: e8a395306c7df773792390c71aa7a8b9d894f77b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497340"
---
# <span data-ttu-id="3ea61-101">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ea61-101">Get-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="3ea61-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3ea61-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea61-103">Bekerül egy alkalmazás-átjáróba.</span><span class="sxs-lookup"><span data-stu-id="3ea61-103">Gets an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ea61-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3ea61-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGateway [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ea61-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3ea61-105">DESCRIPTION</span></span>
<span data-ttu-id="3ea61-106">A **Get-AzureRmApplicationGateway** parancsmag alkalmazás-átjárót kap.</span><span class="sxs-lookup"><span data-stu-id="3ea61-106">The **Get-AzureRmApplicationGateway** cmdlet gets an application gateway.</span></span>

## <span data-ttu-id="3ea61-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3ea61-107">EXAMPLES</span></span>

### <span data-ttu-id="3ea61-108">1. példa: megadott alkalmazásspecifikus átjáró beszerzése</span><span class="sxs-lookup"><span data-stu-id="3ea61-108">Example 1: Get a specified application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3ea61-109">Ez a parancs beolvassa a ApplicationGateway01 nevű alkalmazás-átjárót, amely a ResourceGroup01 nevű erőforráscsoport csoportjába tartozik, és a $AppGw változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3ea61-109">This command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

### <span data-ttu-id="3ea61-110">2. példa: az alkalmazás-átjárók listájának beszerzése egy erőforrás csoportban</span><span class="sxs-lookup"><span data-stu-id="3ea61-110">Example 2: Get a list of application gateways in a resource group</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3ea61-111">Ez a parancs felsorolja a ResourceGroup01 nevű erőforráscsoport összes alkalmazás-átjáróját, és a $AppGwList változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3ea61-111">This command gets a list of all the application gateways in the resource group named ResourceGroup01 and stores it in the $AppGwList variable.</span></span>

### <span data-ttu-id="3ea61-112">3. példa: az alkalmazás-átjárók listájának beszerzése az előfizetésben</span><span class="sxs-lookup"><span data-stu-id="3ea61-112">Example 3: Get a list of application gateways in a subscription</span></span>
```
PS C:\>$AppGwList = Get-AzureRmApplicationGateway
```

<span data-ttu-id="3ea61-113">Ez a parancs felsorolja az előfizetésben szereplő összes alkalmazás-átjárót, és a $AppGwList változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3ea61-113">This command gets a list of all the application gateways in the subscription and stores it in the $AppGwList variable.</span></span>

## <span data-ttu-id="3ea61-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3ea61-114">PARAMETERS</span></span>

### <span data-ttu-id="3ea61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea61-115">-DefaultProfile</span></span>
<span data-ttu-id="3ea61-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3ea61-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ea61-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3ea61-117">-Name</span></span>
<span data-ttu-id="3ea61-118">Annak az alkalmazás-átjárónak a nevét adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="3ea61-118">Specifies the name of the application gateway that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ea61-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ea61-119">-ResourceGroupName</span></span>
<span data-ttu-id="3ea61-120">Az alkalmazás-átjárót tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3ea61-120">Specifies the name of the resource group that contains the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ea61-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea61-121">CommonParameters</span></span>
<span data-ttu-id="3ea61-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3ea61-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea61-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ea61-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea61-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ea61-124">INPUTS</span></span>

### <span data-ttu-id="3ea61-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3ea61-125">System.String</span></span>

## <span data-ttu-id="3ea61-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3ea61-126">OUTPUTS</span></span>

### <span data-ttu-id="3ea61-127">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ea61-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3ea61-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3ea61-128">NOTES</span></span>

## <span data-ttu-id="3ea61-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3ea61-129">RELATED LINKS</span></span>

[<span data-ttu-id="3ea61-130">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3ea61-130">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


