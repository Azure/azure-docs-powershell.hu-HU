---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 08a20958975d78a945e3e73729d5841f6dda6811
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500435"
---
# <span data-ttu-id="75655-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="75655-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="75655-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75655-102">SYNOPSIS</span></span>
<span data-ttu-id="75655-103">A továbbítási névtérben található megadott HybridConnection leírását kapja.</span><span class="sxs-lookup"><span data-stu-id="75655-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75655-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75655-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75655-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="75655-105">DESCRIPTION</span></span>
<span data-ttu-id="75655-106">A **Get-AzureRmRelayHybridConnection** parancsmag leírását kapja a megadott HybridConnection a továbbítási névtéren belül.</span><span class="sxs-lookup"><span data-stu-id="75655-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="75655-107">Példák</span><span class="sxs-lookup"><span data-stu-id="75655-107">EXAMPLES</span></span>

### <span data-ttu-id="75655-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="75655-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="75655-109">A HybridConnection leírását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="75655-109">Returns the description of the HybridConnection.</span></span> 

## <span data-ttu-id="75655-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75655-110">PARAMETERS</span></span>

### <span data-ttu-id="75655-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75655-111">-DefaultProfile</span></span>
<span data-ttu-id="75655-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75655-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75655-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="75655-113">-Name</span></span>
<span data-ttu-id="75655-114">HybridConnections neve</span><span class="sxs-lookup"><span data-stu-id="75655-114">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75655-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="75655-115">-Namespace</span></span>
<span data-ttu-id="75655-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="75655-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75655-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75655-117">-ResourceGroupName</span></span>
<span data-ttu-id="75655-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="75655-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75655-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75655-119">CommonParameters</span></span>
<span data-ttu-id="75655-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75655-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75655-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75655-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75655-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75655-122">INPUTS</span></span>

### <span data-ttu-id="75655-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75655-123">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="75655-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="75655-124">-Namespace</span></span>
    System.String

### <span data-ttu-id="75655-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="75655-125">-Name</span></span>
    System.String

## <span data-ttu-id="75655-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75655-126">OUTPUTS</span></span>

### <span data-ttu-id="75655-127">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Relay. models. HybridConnectionAttibutes, Microsoft. Azure. Command. Relay, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="75655-127">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="75655-128">CreatedAt: 4/12/2017 3:17:02 AM UpdatedAt: 4/12/2017 3:17:02 AM ListenerCount: 0 RequiresClientAuthorization: true UserMetadata: user meta Data ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection név: TestHybridConnection típus: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="75655-128">CreatedAt                   : 4/12/2017 3:17:02 AM UpdatedAt                   : 4/12/2017 3:17:02 AM ListenerCount               : 0 RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name                        : TestHybridConnection Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="75655-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75655-129">NOTES</span></span>

## <span data-ttu-id="75655-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75655-130">RELATED LINKS</span></span>

