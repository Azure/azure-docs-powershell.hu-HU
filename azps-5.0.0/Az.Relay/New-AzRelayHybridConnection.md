---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 04022129d6709cf7dceea128b2813f97a5404234
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302596"
---
# <span data-ttu-id="51fb8-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="51fb8-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="51fb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="51fb8-103">Létrehoz egy HybridConnection a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="51fb8-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="51fb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51fb8-104">SYNTAX</span></span>

### <span data-ttu-id="51fb8-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="51fb8-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51fb8-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="51fb8-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51fb8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="51fb8-107">DESCRIPTION</span></span>
<span data-ttu-id="51fb8-108">Az New-AzRelayHybridConnection parancsmag létrehoz egy HybridConnection a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="51fb8-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="51fb8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="51fb8-109">EXAMPLES</span></span>

### <span data-ttu-id="51fb8-110">Példa 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="51fb8-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="51fb8-111">Új HybirdConnection TestHybirdConnection2 hoz \` létre \` a megadott továbbító névtér \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="51fb8-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="51fb8-112">Példa 2 – tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="51fb8-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="51fb8-113">Új HybirdConnection TestHybirdConnection1 hoz \` létre \` a megadott továbbító névtér \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="51fb8-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="51fb8-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51fb8-114">PARAMETERS</span></span>

### <span data-ttu-id="51fb8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51fb8-115">-DefaultProfile</span></span>
<span data-ttu-id="51fb8-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51fb8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51fb8-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51fb8-117">-InputObject</span></span>
<span data-ttu-id="51fb8-118">HybridConnections objektum</span><span class="sxs-lookup"><span data-stu-id="51fb8-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fb8-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51fb8-119">-Name</span></span>
<span data-ttu-id="51fb8-120">HybridConnections neve</span><span class="sxs-lookup"><span data-stu-id="51fb8-120">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fb8-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="51fb8-121">-Namespace</span></span>
<span data-ttu-id="51fb8-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="51fb8-122">Namespace Name.</span></span>

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

### <span data-ttu-id="51fb8-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="51fb8-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="51fb8-124">True, ha ügyfél-hitelesítés szükséges ehhez a HybridConnections; egyéb esetben false</span><span class="sxs-lookup"><span data-stu-id="51fb8-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51fb8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51fb8-125">-ResourceGroupName</span></span>
<span data-ttu-id="51fb8-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="51fb8-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="51fb8-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="51fb8-127">-UserMetadata</span></span>
<span data-ttu-id="51fb8-128">A usermetadata beolvasása vagy beállítása helyőrző a HybridConnection végpont felhasználó által definiált karakterlánc-adatainak tárolására. használható a leíró adatok tárolására, például a csoportok listájára és a partnerek elérhetőségi adataira is, és tárolhatók a felhasználó által definiált konfigurációs beállítások is.</span><span class="sxs-lookup"><span data-stu-id="51fb8-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="51fb8-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="51fb8-129">-Confirm</span></span>
<span data-ttu-id="51fb8-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51fb8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51fb8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51fb8-131">-WhatIf</span></span>
<span data-ttu-id="51fb8-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="51fb8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51fb8-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51fb8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51fb8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51fb8-134">CommonParameters</span></span>
<span data-ttu-id="51fb8-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51fb8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51fb8-136">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51fb8-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51fb8-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51fb8-137">INPUTS</span></span>

### <span data-ttu-id="51fb8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="51fb8-138">System.String</span></span>

### <span data-ttu-id="51fb8-139">Microsoft. Azure. Command. Relay. models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="51fb8-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

### <span data-ttu-id="51fb8-140">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="51fb8-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="51fb8-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51fb8-141">OUTPUTS</span></span>

### <span data-ttu-id="51fb8-142">Microsoft. Azure. Command. Relay. models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="51fb8-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="51fb8-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51fb8-143">NOTES</span></span>

## <span data-ttu-id="51fb8-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51fb8-144">RELATED LINKS</span></span>
