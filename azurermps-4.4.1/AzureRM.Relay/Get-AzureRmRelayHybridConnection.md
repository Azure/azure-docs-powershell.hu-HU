---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 2fccb11ba45fa1d532c35140db588294895c0802
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494717"
---
# <span data-ttu-id="771ad-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="771ad-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="771ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="771ad-102">SYNOPSIS</span></span>
<span data-ttu-id="771ad-103">A továbbítási névtérben található megadott HybridConnection leírását kapja.</span><span class="sxs-lookup"><span data-stu-id="771ad-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="771ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="771ad-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="771ad-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="771ad-105">DESCRIPTION</span></span>
<span data-ttu-id="771ad-106">A **Get-AzureRmRelayHybridConnection** parancsmag leírását kapja a megadott HybridConnection a továbbítási névtéren belül.</span><span class="sxs-lookup"><span data-stu-id="771ad-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="771ad-107">Példák</span><span class="sxs-lookup"><span data-stu-id="771ad-107">EXAMPLES</span></span>

### <span data-ttu-id="771ad-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="771ad-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="771ad-109">A HybridConnection leírását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="771ad-109">Returns the description of the HybridConnection.</span></span> 

## <span data-ttu-id="771ad-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="771ad-110">PARAMETERS</span></span>

### <span data-ttu-id="771ad-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="771ad-111">-Name</span></span>
<span data-ttu-id="771ad-112">HybridConnections neve</span><span class="sxs-lookup"><span data-stu-id="771ad-112">HybridConnections Name.</span></span>

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

### <span data-ttu-id="771ad-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="771ad-113">-Namespace</span></span>
<span data-ttu-id="771ad-114">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="771ad-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771ad-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="771ad-115">-ResourceGroupName</span></span>
<span data-ttu-id="771ad-116">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="771ad-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="771ad-117">-DefaultProfile</span></span>
<span data-ttu-id="771ad-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="771ad-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="771ad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="771ad-119">CommonParameters</span></span>
<span data-ttu-id="771ad-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="771ad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="771ad-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="771ad-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="771ad-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="771ad-122">INPUTS</span></span>

### <span data-ttu-id="771ad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="771ad-123">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="771ad-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="771ad-124">-Namespace</span></span>
    System.String

### <span data-ttu-id="771ad-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="771ad-125">-Name</span></span>
    System.String

## <span data-ttu-id="771ad-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="771ad-126">OUTPUTS</span></span>

### <span data-ttu-id="771ad-127">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Relay. models. HybridConnectionAttibutes, Microsoft. Azure. Command. Relay, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="771ad-127">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="771ad-128">CreatedAt: 4/12/2017 3:17:02 AM UpdatedAt: 4/12/2017 3:17:02 AM ListenerCount: 0 RequiresClientAuthorization: true UserMetadata: user meta Data ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection név: TestHybridConnection típus: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="771ad-128">CreatedAt                   : 4/12/2017 3:17:02 AM UpdatedAt                   : 4/12/2017 3:17:02 AM ListenerCount               : 0 RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name                        : TestHybridConnection Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="771ad-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="771ad-129">NOTES</span></span>

## <span data-ttu-id="771ad-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="771ad-130">RELATED LINKS</span></span>

