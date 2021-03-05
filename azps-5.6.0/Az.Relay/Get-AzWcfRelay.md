---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: e998bb09435abc787df78050ab25888d0e6651a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000582"
---
# <span data-ttu-id="b6a25-101">Get-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="b6a25-101">Get-AzWcfRelay</span></span>

## <span data-ttu-id="b6a25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6a25-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a25-103">A megadott WcfRelay leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b6a25-103">Returns a description for the specified WcfRelay.</span></span>

## <span data-ttu-id="b6a25-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b6a25-104">SYNTAX</span></span>

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6a25-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b6a25-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a25-106">A **Get-AzWcfRelay** parancsmag visszaadja a megadott WcfRelay leírását.</span><span class="sxs-lookup"><span data-stu-id="b6a25-106">The **Get-AzWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="b6a25-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b6a25-107">EXAMPLES</span></span>

### <span data-ttu-id="b6a25-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b6a25-108">Example 1</span></span>
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

<span data-ttu-id="b6a25-109">A WcfRelay leírását adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="b6a25-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="b6a25-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6a25-110">PARAMETERS</span></span>

### <span data-ttu-id="b6a25-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a25-111">-DefaultProfile</span></span>
<span data-ttu-id="b6a25-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b6a25-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6a25-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b6a25-113">-Name</span></span>
<span data-ttu-id="b6a25-114">WcfRelay Name.</span><span class="sxs-lookup"><span data-stu-id="b6a25-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="b6a25-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b6a25-115">-Namespace</span></span>
<span data-ttu-id="b6a25-116">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="b6a25-116">Namespace Name.</span></span>

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

### <span data-ttu-id="b6a25-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6a25-117">-ResourceGroupName</span></span>
<span data-ttu-id="b6a25-118">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b6a25-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="b6a25-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a25-119">CommonParameters</span></span>
<span data-ttu-id="b6a25-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a25-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a25-121">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a25-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a25-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6a25-122">INPUTS</span></span>

### <span data-ttu-id="b6a25-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b6a25-123">System.String</span></span>

## <span data-ttu-id="b6a25-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b6a25-124">OUTPUTS</span></span>

### <span data-ttu-id="b6a25-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="b6a25-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="b6a25-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b6a25-126">NOTES</span></span>

## <span data-ttu-id="b6a25-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b6a25-127">RELATED LINKS</span></span>
