---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: d701e563e05f33b3cb0ed99a2e62fbcd54935987
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188092"
---
# <span data-ttu-id="a4f62-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4f62-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="a4f62-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a4f62-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f62-103">Az alkalmazás-átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="a4f62-103">Updates an application gateway.</span></span>

## <span data-ttu-id="a4f62-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a4f62-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4f62-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a4f62-105">DESCRIPTION</span></span>
<span data-ttu-id="a4f62-106">A **set-AzApplicationGateway** parancsmag az Azure Application Gatewayt frissíti.</span><span class="sxs-lookup"><span data-stu-id="a4f62-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="a4f62-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a4f62-107">EXAMPLES</span></span>

### <span data-ttu-id="a4f62-108">1. példa: az alkalmazás-átjáró frissítése</span><span class="sxs-lookup"><span data-stu-id="a4f62-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name Test -ResourceGroupName Appgwtest
PS C:\>$AppGw.Tag = @{"key"="value"}
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="a4f62-109">Ezek a parancsok frissítik az alkalmazás átjáróját a $AppGw változóban lévő beállításokkal, és a módosított átjárót a $UpdatedAppGw változóban tárolják.</span><span class="sxs-lookup"><span data-stu-id="a4f62-109">These commands update the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="a4f62-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a4f62-110">PARAMETERS</span></span>

### <span data-ttu-id="a4f62-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4f62-111">-ApplicationGateway</span></span>
<span data-ttu-id="a4f62-112">Az a beállítás, amely azt az államot adja meg, amelybe az alkalmazás átjáróját be kell állítani.</span><span class="sxs-lookup"><span data-stu-id="a4f62-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="a4f62-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4f62-113">-AsJob</span></span>
<span data-ttu-id="a4f62-114">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="a4f62-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4f62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f62-115">-DefaultProfile</span></span>
<span data-ttu-id="a4f62-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a4f62-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f62-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f62-117">CommonParameters</span></span>
<span data-ttu-id="a4f62-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a4f62-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f62-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a4f62-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f62-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4f62-120">INPUTS</span></span>

### <span data-ttu-id="a4f62-121">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4f62-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a4f62-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a4f62-122">OUTPUTS</span></span>

### <span data-ttu-id="a4f62-123">Microsoft. Azure. commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4f62-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a4f62-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a4f62-124">NOTES</span></span>

## <span data-ttu-id="a4f62-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a4f62-125">RELATED LINKS</span></span>

[<span data-ttu-id="a4f62-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a4f62-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


