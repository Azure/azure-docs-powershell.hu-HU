---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
ms.openlocfilehash: ff836268c92b575db05e05b1843c57af2bc6dca7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503712"
---
# <span data-ttu-id="99e04-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99e04-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="99e04-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99e04-102">SYNOPSIS</span></span>
<span data-ttu-id="99e04-103">Az alkalmazás-átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="99e04-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99e04-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99e04-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99e04-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="99e04-105">DESCRIPTION</span></span>
<span data-ttu-id="99e04-106">A **set-AzureRmApplicationGateway** parancsmag az Azure Application Gatewayt frissíti.</span><span class="sxs-lookup"><span data-stu-id="99e04-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="99e04-107">Példák</span><span class="sxs-lookup"><span data-stu-id="99e04-107">EXAMPLES</span></span>

### <span data-ttu-id="99e04-108">1. példa: az alkalmazás-átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="99e04-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="99e04-109">Ez a parancs frissíti az alkalmazás átjáróját a $AppGw változóban lévő beállításokkal, és a $UpdatedAppGw változóban tárolja a frissített átjárót.</span><span class="sxs-lookup"><span data-stu-id="99e04-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="99e04-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99e04-110">PARAMETERS</span></span>

### <span data-ttu-id="99e04-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99e04-111">-ApplicationGateway</span></span>
<span data-ttu-id="99e04-112">Az a beállítás, amely azt az államot adja meg, amelybe az alkalmazás átjáróját be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="99e04-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="99e04-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99e04-113">-AsJob</span></span>
<span data-ttu-id="99e04-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="99e04-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e04-115">-DefaultProfile</span></span>
<span data-ttu-id="99e04-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99e04-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99e04-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e04-117">CommonParameters</span></span>
<span data-ttu-id="99e04-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99e04-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e04-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99e04-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e04-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99e04-120">INPUTS</span></span>

### <span data-ttu-id="99e04-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99e04-121">PSApplicationGateway</span></span>
<span data-ttu-id="99e04-122">A ' ApplicationGateway ' paraméter az "PSApplicationGateway" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="99e04-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="99e04-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99e04-123">OUTPUTS</span></span>

### <span data-ttu-id="99e04-124">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99e04-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="99e04-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99e04-125">NOTES</span></span>

## <span data-ttu-id="99e04-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99e04-126">RELATED LINKS</span></span>

[<span data-ttu-id="99e04-127">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="99e04-127">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


