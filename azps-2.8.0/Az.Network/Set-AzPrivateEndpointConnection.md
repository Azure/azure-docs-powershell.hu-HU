---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 588402480cbd626a747208705ec59fd10c572075
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838333"
---
# <span data-ttu-id="85341-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="85341-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="85341-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="85341-102">SYNOPSIS</span></span>
<span data-ttu-id="85341-103">Privát végpont-kapcsolati állapotot frissít a privát hivatkozás szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="85341-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="85341-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="85341-104">SYNTAX</span></span>

```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85341-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="85341-105">DESCRIPTION</span></span>
<span data-ttu-id="85341-106">A **set-AzPrivateEndpointConnection** parancsmag privát végpont-kapcsolati állapotot frissít egy privát hivatkozás szolgáltatásban</span><span class="sxs-lookup"><span data-stu-id="85341-106">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="85341-107">Példák</span><span class="sxs-lookup"><span data-stu-id="85341-107">EXAMPLES</span></span>

### <span data-ttu-id="85341-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="85341-108">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="85341-109">Ez a példa egy privát végpontos kapcsolati állapotot frissít a jóváhagyásra.</span><span class="sxs-lookup"><span data-stu-id="85341-109">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="85341-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="85341-110">PARAMETERS</span></span>

### <span data-ttu-id="85341-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85341-111">-DefaultProfile</span></span>
<span data-ttu-id="85341-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="85341-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85341-113">-Leírás</span><span class="sxs-lookup"><span data-stu-id="85341-113">-Description</span></span>
<span data-ttu-id="85341-114">A tevékenység oka.</span><span class="sxs-lookup"><span data-stu-id="85341-114">The reason of action.</span></span>

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

### <span data-ttu-id="85341-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="85341-115">-Name</span></span>
<span data-ttu-id="85341-116">Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="85341-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85341-117">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="85341-117">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="85341-118">Jóváhagyta vagy visszautasította az erőforrást.</span><span class="sxs-lookup"><span data-stu-id="85341-118">Approved or rejected the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85341-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85341-119">-ResourceGroupName</span></span>
<span data-ttu-id="85341-120">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="85341-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85341-121">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="85341-121">-ServiceName</span></span>
<span data-ttu-id="85341-122">A privát hivatkozás szolgáltatás neve.</span><span class="sxs-lookup"><span data-stu-id="85341-122">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85341-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85341-123">CommonParameters</span></span>
<span data-ttu-id="85341-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="85341-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85341-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="85341-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85341-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="85341-126">INPUTS</span></span>

### <span data-ttu-id="85341-127">System. String</span><span class="sxs-lookup"><span data-stu-id="85341-127">System.String</span></span>

## <span data-ttu-id="85341-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="85341-128">OUTPUTS</span></span>

### <span data-ttu-id="85341-129">Microsoft. Azure. commands. Network. models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="85341-129">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="85341-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="85341-130">NOTES</span></span>

## <span data-ttu-id="85341-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="85341-131">RELATED LINKS</span></span>
