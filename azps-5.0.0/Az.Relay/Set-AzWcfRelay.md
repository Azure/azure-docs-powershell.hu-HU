---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: f7671d35901705ef96f6c1bf13c487c688a6214c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302549"
---
# <span data-ttu-id="75b01-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="75b01-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="75b01-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="75b01-102">SYNOPSIS</span></span>
<span data-ttu-id="75b01-103">Frissíti egy WcfRelay leírását a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="75b01-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="75b01-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="75b01-104">SYNTAX</span></span>

### <span data-ttu-id="75b01-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="75b01-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75b01-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="75b01-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75b01-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="75b01-107">DESCRIPTION</span></span>
<span data-ttu-id="75b01-108">A Set-AzWcfRelay parancsmag a megadott továbbítási névtérben lévő WcfRelay leírását frissíti.</span><span class="sxs-lookup"><span data-stu-id="75b01-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="75b01-109">Példák</span><span class="sxs-lookup"><span data-stu-id="75b01-109">EXAMPLES</span></span>

### <span data-ttu-id="75b01-110">Példa 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="75b01-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:16:50 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

### <span data-ttu-id="75b01-111">Példa 2 – tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="75b01-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:26:09 PM
ListenerCount               :
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
Name                        : TestWCFRelay
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="75b01-112">Frissíti a megadott WcfRelay egy új leírással a megadott névtérben.</span><span class="sxs-lookup"><span data-stu-id="75b01-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="75b01-113">Ez a példa frissíti a UserMetadata tulajdonságot új értékkel.</span><span class="sxs-lookup"><span data-stu-id="75b01-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="75b01-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="75b01-114">PARAMETERS</span></span>

### <span data-ttu-id="75b01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75b01-115">-DefaultProfile</span></span>
<span data-ttu-id="75b01-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="75b01-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75b01-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75b01-117">-InputObject</span></span>
<span data-ttu-id="75b01-118">WcfRelay objektum</span><span class="sxs-lookup"><span data-stu-id="75b01-118">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75b01-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="75b01-119">-Name</span></span>
<span data-ttu-id="75b01-120">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="75b01-120">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75b01-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="75b01-121">-Namespace</span></span>
<span data-ttu-id="75b01-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="75b01-122">Namespace Name.</span></span>

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

### <span data-ttu-id="75b01-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75b01-123">-ResourceGroupName</span></span>
<span data-ttu-id="75b01-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="75b01-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="75b01-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="75b01-125">-UserMetadata</span></span>
<span data-ttu-id="75b01-126">A usermetadata beolvasása vagy beállítása helyőrző a WcfRelay végpont felhasználó által definiált karakterlánc-adatainak tárolására. használható a leíró adatok tárolására, például a csoportok listájára és a partnerek elérhetőségi adataira is, és tárolhatók a felhasználó által definiált konfigurációs beállítások is.</span><span class="sxs-lookup"><span data-stu-id="75b01-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75b01-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="75b01-127">-Confirm</span></span>
<span data-ttu-id="75b01-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="75b01-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b01-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75b01-129">-WhatIf</span></span>
<span data-ttu-id="75b01-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="75b01-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75b01-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75b01-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75b01-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75b01-132">CommonParameters</span></span>
<span data-ttu-id="75b01-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="75b01-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75b01-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75b01-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75b01-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="75b01-135">INPUTS</span></span>

### <span data-ttu-id="75b01-136">System. String</span><span class="sxs-lookup"><span data-stu-id="75b01-136">System.String</span></span>

### <span data-ttu-id="75b01-137">Microsoft. Azure. Command. Relay. models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="75b01-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="75b01-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75b01-138">OUTPUTS</span></span>

### <span data-ttu-id="75b01-139">Microsoft. Azure. Command. Relay. models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="75b01-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="75b01-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="75b01-140">NOTES</span></span>

## <span data-ttu-id="75b01-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75b01-141">RELATED LINKS</span></span>
