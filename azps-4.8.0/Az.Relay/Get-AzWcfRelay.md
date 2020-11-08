---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: 260cb8b605415137e9a9e667634ff02b8d4b3de7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024485"
---
# <span data-ttu-id="493a2-101">Get-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="493a2-101">Get-AzWcfRelay</span></span>

## <span data-ttu-id="493a2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="493a2-102">SYNOPSIS</span></span>
<span data-ttu-id="493a2-103">A megadott WcfRelay leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="493a2-103">Returns a description for the specified WcfRelay.</span></span>

## <span data-ttu-id="493a2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="493a2-104">SYNTAX</span></span>

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="493a2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="493a2-105">DESCRIPTION</span></span>
<span data-ttu-id="493a2-106">A **Get-AzWcfRelay** parancsmag a megadott WcfRelay leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="493a2-106">The **Get-AzWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="493a2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="493a2-107">EXAMPLES</span></span>

### <span data-ttu-id="493a2-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="493a2-108">Example 1</span></span>
```
PS C:\> Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

RelayType                   : NetTcp
CreatedAt                   : 4/12/2017 2:23:08 AM
UpdatedAt                   : 4/12/2017 2:23:08 AM
ListenerCount               : 0
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W
                              cfRelays/TestWCFRelay1
Name                        : TestWCFRelay1
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="493a2-109">A WcfRelay leírását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="493a2-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="493a2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="493a2-110">PARAMETERS</span></span>

### <span data-ttu-id="493a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="493a2-111">-DefaultProfile</span></span>
<span data-ttu-id="493a2-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="493a2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="493a2-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="493a2-113">-Name</span></span>
<span data-ttu-id="493a2-114">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="493a2-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="493a2-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="493a2-115">-Namespace</span></span>
<span data-ttu-id="493a2-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="493a2-116">Namespace Name.</span></span>

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

### <span data-ttu-id="493a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="493a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="493a2-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="493a2-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="493a2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493a2-119">CommonParameters</span></span>
<span data-ttu-id="493a2-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="493a2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493a2-121">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="493a2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493a2-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="493a2-122">INPUTS</span></span>

### <span data-ttu-id="493a2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="493a2-123">System.String</span></span>

## <span data-ttu-id="493a2-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="493a2-124">OUTPUTS</span></span>

### <span data-ttu-id="493a2-125">Microsoft. Azure. Command. Relay. models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="493a2-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="493a2-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="493a2-126">NOTES</span></span>

## <span data-ttu-id="493a2-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="493a2-127">RELATED LINKS</span></span>
