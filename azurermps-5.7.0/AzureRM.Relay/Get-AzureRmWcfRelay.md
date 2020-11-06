---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 88d2c8f7b0bcab3faad6368070606b8a36948343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502500"
---
# <span data-ttu-id="d3dcc-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="d3dcc-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="d3dcc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="d3dcc-103">A megadott WcfRelay leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3dcc-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3dcc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3dcc-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3dcc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3dcc-105">DESCRIPTION</span></span>
<span data-ttu-id="d3dcc-106">A **Get-AzureRmWcfRelay** parancsmag a megadott WcfRelay leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3dcc-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="d3dcc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d3dcc-107">EXAMPLES</span></span>

### <span data-ttu-id="d3dcc-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d3dcc-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="d3dcc-109">A WcfRelay leírását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="d3dcc-109">Returns the description of the WcfRelay.</span></span> 

## <span data-ttu-id="d3dcc-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3dcc-110">PARAMETERS</span></span>

### <span data-ttu-id="d3dcc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3dcc-111">-DefaultProfile</span></span>
<span data-ttu-id="d3dcc-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3dcc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3dcc-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3dcc-113">-Name</span></span>
<span data-ttu-id="d3dcc-114">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="d3dcc-114">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3dcc-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d3dcc-115">-Namespace</span></span>
<span data-ttu-id="d3dcc-116">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="d3dcc-116">Namespace Name.</span></span>

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

### <span data-ttu-id="d3dcc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3dcc-117">-ResourceGroupName</span></span>
<span data-ttu-id="d3dcc-118">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d3dcc-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="d3dcc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3dcc-119">CommonParameters</span></span>
<span data-ttu-id="d3dcc-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3dcc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3dcc-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3dcc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3dcc-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3dcc-122">INPUTS</span></span>

### <span data-ttu-id="d3dcc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3dcc-123">-ResourceGroupName</span></span>
 <span data-ttu-id="d3dcc-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d3dcc-124">System.String</span></span>
 

### <span data-ttu-id="d3dcc-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d3dcc-125">-Namespace</span></span>
 <span data-ttu-id="d3dcc-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d3dcc-126">System.String</span></span>
 

### <span data-ttu-id="d3dcc-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3dcc-127">-Name</span></span>
 <span data-ttu-id="d3dcc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d3dcc-128">System.String</span></span> 

## <span data-ttu-id="d3dcc-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3dcc-129">OUTPUTS</span></span>

### <span data-ttu-id="d3dcc-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Relay. models. WcfRelayAttributes, Microsoft. Azure. Command. Relay, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d3dcc-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="d3dcc-131">RelayType: NetTcp CreatedAt: 4/12/2017 2:23:08 AM UpdatedAt: 4/12/2017 2:23:08 AM ListenerCount: 0 RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false UserMetadata: user meta Data ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 név: TestWCFRelay1 típus: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="d3dcc-131">RelayType                   : NetTcp CreatedAt                   : 4/12/2017 2:23:08 AM UpdatedAt                   : 4/12/2017 2:23:08 AM ListenerCount               : 0 RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name                        : TestWCFRelay1 Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="d3dcc-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3dcc-132">NOTES</span></span>

## <span data-ttu-id="d3dcc-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3dcc-133">RELATED LINKS</span></span>

