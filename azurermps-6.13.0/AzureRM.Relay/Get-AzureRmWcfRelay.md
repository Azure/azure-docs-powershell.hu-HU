---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 342c18add7438c75babd1225722c3830c4c5c696
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492766"
---
# <span data-ttu-id="eaaaa-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="eaaaa-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="eaaaa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eaaaa-102">SYNOPSIS</span></span>
<span data-ttu-id="eaaaa-103">A megadott WcfRelay leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaaaa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eaaaa-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaaaa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eaaaa-105">DESCRIPTION</span></span>
<span data-ttu-id="eaaaa-106">A **Get-AzureRmWcfRelay** parancsmag a megadott WcfRelay leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="eaaaa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="eaaaa-107">EXAMPLES</span></span>

### <span data-ttu-id="eaaaa-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="eaaaa-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

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

<span data-ttu-id="eaaaa-109">A WcfRelay leírását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="eaaaa-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eaaaa-110">PARAMETERS</span></span>

### <span data-ttu-id="eaaaa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaaaa-111">-DefaultProfile</span></span>
<span data-ttu-id="eaaaa-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaaaa-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eaaaa-113">-Name</span></span>
<span data-ttu-id="eaaaa-114">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="eaaaa-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="eaaaa-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eaaaa-115">-Namespace</span></span>
<span data-ttu-id="eaaaa-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="eaaaa-116">Namespace Name.</span></span>

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

### <span data-ttu-id="eaaaa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaaaa-117">-ResourceGroupName</span></span>
<span data-ttu-id="eaaaa-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="eaaaa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaaaa-119">CommonParameters</span></span>
<span data-ttu-id="eaaaa-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eaaaa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="eaaaa-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaaaa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaaaa-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eaaaa-122">INPUTS</span></span>

### <span data-ttu-id="eaaaa-123">System. String</span><span class="sxs-lookup"><span data-stu-id="eaaaa-123">System.String</span></span>


## <span data-ttu-id="eaaaa-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eaaaa-124">OUTPUTS</span></span>

### <span data-ttu-id="eaaaa-125">Microsoft. Azure. Command. Relay. models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="eaaaa-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>


## <span data-ttu-id="eaaaa-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eaaaa-126">NOTES</span></span>

## <span data-ttu-id="eaaaa-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eaaaa-127">RELATED LINKS</span></span>
