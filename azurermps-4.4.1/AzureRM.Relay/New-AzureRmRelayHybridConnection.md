---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 315c50dbbc68865058f6c5663952fe2f42bc5c85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493380"
---
# <span data-ttu-id="b4753-101">New-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="b4753-101">New-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="b4753-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b4753-102">SYNOPSIS</span></span>
<span data-ttu-id="b4753-103">Létrehoz egy HybridConnection a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="b4753-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4753-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b4753-104">SYNTAX</span></span>

### <span data-ttu-id="b4753-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b4753-105">HybridConnectionInputObjectSet</span></span>
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4753-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="b4753-106">HybridConnectionPropertiesSet</span></span>
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4753-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b4753-107">DESCRIPTION</span></span>
<span data-ttu-id="b4753-108">Az New-AzureRmRelayHybridConnection parancsmag létrehoz egy HybridConnection a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="b4753-108">The New-AzureRmRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="b4753-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b4753-109">EXAMPLES</span></span>

### <span data-ttu-id="b4753-110">Példa 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4753-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection
```

<span data-ttu-id="b4753-111">Új HybirdConnection TestHybirdConnection2 hoz \` létre \` a megadott továbbító névtér \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="b4753-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="b4753-112">Példa 2 – tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="b4753-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"
```

<span data-ttu-id="b4753-113">Új HybirdConnection TestHybirdConnection1 hoz \` létre \` a megadott továbbító névtér \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="b4753-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="b4753-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b4753-114">PARAMETERS</span></span>

### <span data-ttu-id="b4753-115">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="b4753-115">-RequiresClientAuthorization</span></span>
<span data-ttu-id="b4753-116">True, ha ügyfél-hitelesítés szükséges ehhez a HybridConnections; egyéb esetben false</span><span class="sxs-lookup"><span data-stu-id="b4753-116">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

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

### <span data-ttu-id="b4753-117">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="b4753-117">-UserMetadata</span></span>
<span data-ttu-id="b4753-118">A usermetadata beolvasása vagy beállítása helyőrző a HybridConnection végpont felhasználó által definiált karakterlánc-adatainak tárolására. használható a leíró adatok tárolására, például a csoportok listájára és a partnerek elérhetőségi adataira is, és tárolhatók a felhasználó által definiált konfigurációs beállítások is.</span><span class="sxs-lookup"><span data-stu-id="b4753-118">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="b4753-119">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b4753-119">-Confirm</span></span>
<span data-ttu-id="b4753-120">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b4753-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4753-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4753-121">-WhatIf</span></span>
<span data-ttu-id="b4753-122">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b4753-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4753-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4753-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4753-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4753-124">-InputObject</span></span>
<span data-ttu-id="b4753-125">HybridConnections objektum</span><span class="sxs-lookup"><span data-stu-id="b4753-125">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4753-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b4753-126">-Name</span></span>
<span data-ttu-id="b4753-127">HybridConnections neve</span><span class="sxs-lookup"><span data-stu-id="b4753-127">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4753-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b4753-128">-Namespace</span></span>
<span data-ttu-id="b4753-129">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="b4753-129">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4753-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4753-130">-ResourceGroupName</span></span>
<span data-ttu-id="b4753-131">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="b4753-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4753-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4753-132">-DefaultProfile</span></span>
<span data-ttu-id="b4753-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4753-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4753-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4753-134">CommonParameters</span></span>
<span data-ttu-id="b4753-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b4753-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4753-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4753-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4753-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4753-137">INPUTS</span></span>

### <span data-ttu-id="b4753-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4753-138">-ResourceGroupName</span></span>
<span data-ttu-id="b4753-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b4753-139">System.String</span></span>

### <span data-ttu-id="b4753-140">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b4753-140">-NamespaceName</span></span>
<span data-ttu-id="b4753-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b4753-141">System.String</span></span>

### <span data-ttu-id="b4753-142">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="b4753-142">-HybridConnectionsName</span></span>
<span data-ttu-id="b4753-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b4753-143">System.String</span></span>

### <span data-ttu-id="b4753-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4753-144">-InputObject</span></span>
<span data-ttu-id="b4753-145">Microsoft. Azure. Command. Relay. models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="b4753-145">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="b4753-146">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="b4753-146">-RequiresClientAuthorization</span></span>
<span data-ttu-id="b4753-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b4753-147">System.Boolean</span></span>

### <span data-ttu-id="b4753-148">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="b4753-148">-UserMetadata</span></span>
<span data-ttu-id="b4753-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b4753-149">System.String</span></span>

## <span data-ttu-id="b4753-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4753-150">OUTPUTS</span></span>

### <span data-ttu-id="b4753-151">Microsoft. Azure. Command. Relay. models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="b4753-151">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="b4753-152">Példák-1: InputObject</span><span class="sxs-lookup"><span data-stu-id="b4753-152">Examples - 1 : InputObject</span></span>
<span data-ttu-id="b4753-153">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:04:15 PM ListenerCount: RequiresClientAuthorization: true UserMetadata: user meta Data ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N2 név: TestHybirdConnection2 típus: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="b4753-153">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:04:15 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name                        : TestHybirdConnection2 Type                        : Microsoft.Relay/HybridConnections</span></span>

### <span data-ttu-id="b4753-154">Példák-2: tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="b4753-154">Examples - 2 : Properties</span></span>
<span data-ttu-id="b4753-155">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:04:15 PM ListenerCount: RequiresClientAuthorization: true UserMetadata: user meta Data ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N1 név: TestHybirdConnection1 típus: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="b4753-155">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:04:15 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name                        : TestHybirdConnection1 Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="b4753-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b4753-156">NOTES</span></span>

## <span data-ttu-id="b4753-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4753-157">RELATED LINKS</span></span>

