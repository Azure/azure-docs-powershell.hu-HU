---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 81463fc5202c9b5990e5d73d81c7bc2cbeadcca0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496935"
---
# <span data-ttu-id="13c19-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="13c19-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="13c19-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="13c19-102">SYNOPSIS</span></span>
<span data-ttu-id="13c19-103">A megadott WcfRelay leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="13c19-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13c19-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="13c19-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13c19-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="13c19-105">DESCRIPTION</span></span>
<span data-ttu-id="13c19-106">A **Get-AzureRmWcfRelay** parancsmag a megadott WcfRelay leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="13c19-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="13c19-107">Példák</span><span class="sxs-lookup"><span data-stu-id="13c19-107">EXAMPLES</span></span>

### <span data-ttu-id="13c19-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="13c19-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="13c19-109">A WcfRelay leírását számítja ki.</span><span class="sxs-lookup"><span data-stu-id="13c19-109">Returns the description of the WcfRelay.</span></span> 

## <span data-ttu-id="13c19-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="13c19-110">PARAMETERS</span></span>

### <span data-ttu-id="13c19-111">-Namespace</span><span class="sxs-lookup"><span data-stu-id="13c19-111">-Namespace</span></span>
<span data-ttu-id="13c19-112">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="13c19-112">Namespace Name.</span></span>

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

### <span data-ttu-id="13c19-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13c19-113">-ResourceGroupName</span></span>
<span data-ttu-id="13c19-114">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="13c19-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="13c19-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13c19-115">-Name</span></span>
<span data-ttu-id="13c19-116">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="13c19-116">WcfRelay Name.</span></span>

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

### <span data-ttu-id="13c19-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13c19-117">-DefaultProfile</span></span>
<span data-ttu-id="13c19-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="13c19-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13c19-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13c19-119">CommonParameters</span></span>
<span data-ttu-id="13c19-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="13c19-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13c19-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13c19-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13c19-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="13c19-122">INPUTS</span></span>

### <span data-ttu-id="13c19-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13c19-123">-ResourceGroupName</span></span>
 <span data-ttu-id="13c19-124">System. String</span><span class="sxs-lookup"><span data-stu-id="13c19-124">System.String</span></span>
 

### <span data-ttu-id="13c19-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="13c19-125">-Namespace</span></span>
 <span data-ttu-id="13c19-126">System. String</span><span class="sxs-lookup"><span data-stu-id="13c19-126">System.String</span></span>
 

### <span data-ttu-id="13c19-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="13c19-127">-Name</span></span>
 <span data-ttu-id="13c19-128">System. String</span><span class="sxs-lookup"><span data-stu-id="13c19-128">System.String</span></span> 

## <span data-ttu-id="13c19-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="13c19-129">OUTPUTS</span></span>

### <span data-ttu-id="13c19-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Relay. models. WcfRelayAttributes, Microsoft. Azure. Command. Relay, Version = 0.1.0.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="13c19-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="13c19-131">RelayType: NetTcp CreatedAt: 4/12/2017 2:23:08 AM UpdatedAt: 4/12/2017 2:23:08 AM ListenerCount: 0 RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false UserMetadata: user meta Data ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 név: TestWCFRelay1 típus: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="13c19-131">RelayType                   : NetTcp CreatedAt                   : 4/12/2017 2:23:08 AM UpdatedAt                   : 4/12/2017 2:23:08 AM ListenerCount               : 0 RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name                        : TestWCFRelay1 Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="13c19-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="13c19-132">NOTES</span></span>

## <span data-ttu-id="13c19-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="13c19-133">RELATED LINKS</span></span>

