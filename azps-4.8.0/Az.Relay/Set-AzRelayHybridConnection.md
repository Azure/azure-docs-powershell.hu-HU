---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
ms.openlocfilehash: 2b029b2a93a063a322c11ea84cd46b787acc9960
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184691"
---
# <span data-ttu-id="ede39-101">Set-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="ede39-101">Set-AzRelayHybridConnection</span></span>

## <span data-ttu-id="ede39-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ede39-102">SYNOPSIS</span></span>
<span data-ttu-id="ede39-103">Frissíti egy HybridConnection leírását a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="ede39-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="ede39-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ede39-104">SYNTAX</span></span>

### <span data-ttu-id="ede39-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ede39-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ede39-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="ede39-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ede39-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ede39-107">DESCRIPTION</span></span>
<span data-ttu-id="ede39-108">A Set-AzRelayHybridConnection parancsmag a megadott továbbítási névtérben lévő HybridConnection leírását frissíti.</span><span class="sxs-lookup"><span data-stu-id="ede39-108">The Set-AzRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="ede39-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ede39-109">EXAMPLES</span></span>

### <span data-ttu-id="ede39-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ede39-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:08:11 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

### <span data-ttu-id="ede39-111">2. példa</span><span class="sxs-lookup"><span data-stu-id="ede39-111">Example 2</span></span>
```
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:10:25 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata updated
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="ede39-112">Frissíti a megadott HybridConnection egy új leírással a megadott névtérben.</span><span class="sxs-lookup"><span data-stu-id="ede39-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="ede39-113">Ez a példa frissíti a UserMetadata tulajdonságot új értékkel.</span><span class="sxs-lookup"><span data-stu-id="ede39-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="ede39-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ede39-114">PARAMETERS</span></span>

### <span data-ttu-id="ede39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ede39-115">-DefaultProfile</span></span>
<span data-ttu-id="ede39-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ede39-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ede39-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ede39-117">-InputObject</span></span>
<span data-ttu-id="ede39-118">HybridConnections objektum</span><span class="sxs-lookup"><span data-stu-id="ede39-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ede39-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ede39-119">-Name</span></span>
<span data-ttu-id="ede39-120">HybridConnections neve</span><span class="sxs-lookup"><span data-stu-id="ede39-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="ede39-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ede39-121">-Namespace</span></span>
<span data-ttu-id="ede39-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="ede39-122">Namespace Name.</span></span>

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

### <span data-ttu-id="ede39-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ede39-123">-ResourceGroupName</span></span>
<span data-ttu-id="ede39-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ede39-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="ede39-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="ede39-125">-UserMetadata</span></span>
<span data-ttu-id="ede39-126">A usermetadata beolvasása vagy beállítása helyőrző a HybridConnection végpont felhasználó által definiált karakterlánc-adatainak tárolására. használható a leíró adatok tárolására, például a csoportok listájára és a partnerek elérhetőségi adataira is, és tárolhatók a felhasználó által definiált konfigurációs beállítások is.</span><span class="sxs-lookup"><span data-stu-id="ede39-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ede39-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ede39-127">-Confirm</span></span>
<span data-ttu-id="ede39-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ede39-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ede39-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ede39-129">-WhatIf</span></span>
<span data-ttu-id="ede39-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ede39-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ede39-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ede39-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ede39-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede39-132">CommonParameters</span></span>
<span data-ttu-id="ede39-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ede39-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ede39-134">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ede39-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede39-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ede39-135">INPUTS</span></span>

### <span data-ttu-id="ede39-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ede39-136">System.String</span></span>

### <span data-ttu-id="ede39-137">Microsoft. Azure. Command. Relay. models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="ede39-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="ede39-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ede39-138">OUTPUTS</span></span>

### <span data-ttu-id="ede39-139">Microsoft. Azure. Command. Relay. models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="ede39-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="ede39-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ede39-140">NOTES</span></span>

## <span data-ttu-id="ede39-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ede39-141">RELATED LINKS</span></span>
