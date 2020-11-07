---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 9398c2229b31e432e55e5c4b11e72d3360b52fbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672845"
---
# <span data-ttu-id="123c7-101">New-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="123c7-101">New-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="123c7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="123c7-102">SYNOPSIS</span></span>
<span data-ttu-id="123c7-103">Létrehoz egy HybridConnection a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="123c7-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="123c7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="123c7-104">SYNTAX</span></span>

### <span data-ttu-id="123c7-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="123c7-105">HybridConnectionInputObjectSet</span></span>
```
New-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="123c7-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="123c7-106">HybridConnectionPropertiesSet</span></span>
```
New-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="123c7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="123c7-107">DESCRIPTION</span></span>
<span data-ttu-id="123c7-108">Az New-AzureRmRelayHybridConnection parancsmag létrehoz egy HybridConnection a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="123c7-108">The New-AzureRmRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="123c7-109">Példák</span><span class="sxs-lookup"><span data-stu-id="123c7-109">EXAMPLES</span></span>

### <span data-ttu-id="123c7-110">Példa 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="123c7-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

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

<span data-ttu-id="123c7-111">Új HybirdConnection TestHybirdConnection2 hoz \` létre \` a megadott továbbító névtér \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="123c7-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="123c7-112">Példa 2 – tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="123c7-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

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

<span data-ttu-id="123c7-113">Új HybirdConnection TestHybirdConnection1 hoz \` létre \` a megadott továbbító névtér \` TestNameSpace-HybirdConnection \` .</span><span class="sxs-lookup"><span data-stu-id="123c7-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="123c7-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="123c7-114">PARAMETERS</span></span>

### <span data-ttu-id="123c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="123c7-115">-DefaultProfile</span></span>
<span data-ttu-id="123c7-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="123c7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="123c7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="123c7-117">-InputObject</span></span>
<span data-ttu-id="123c7-118">HybridConnections objektum</span><span class="sxs-lookup"><span data-stu-id="123c7-118">HybridConnections object.</span></span>

```yaml
Type: HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="123c7-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="123c7-119">-Name</span></span>
<span data-ttu-id="123c7-120">HybridConnections neve</span><span class="sxs-lookup"><span data-stu-id="123c7-120">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="123c7-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="123c7-121">-Namespace</span></span>
<span data-ttu-id="123c7-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="123c7-122">Namespace Name.</span></span>

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

### <span data-ttu-id="123c7-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="123c7-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="123c7-124">True, ha ügyfél-hitelesítés szükséges ehhez a HybridConnections; egyéb esetben false</span><span class="sxs-lookup"><span data-stu-id="123c7-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: Boolean
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="123c7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="123c7-125">-ResourceGroupName</span></span>
<span data-ttu-id="123c7-126">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="123c7-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="123c7-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="123c7-127">-UserMetadata</span></span>
<span data-ttu-id="123c7-128">A usermetadata beolvasása vagy beállítása helyőrző a HybridConnection végpont felhasználó által definiált karakterlánc-adatainak tárolására. használható a leíró adatok tárolására, például a csoportok listájára és a partnerek elérhetőségi adataira is, és tárolhatók a felhasználó által definiált konfigurációs beállítások is.</span><span class="sxs-lookup"><span data-stu-id="123c7-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="123c7-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="123c7-129">-Confirm</span></span>
<span data-ttu-id="123c7-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="123c7-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="123c7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="123c7-131">-WhatIf</span></span>
<span data-ttu-id="123c7-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="123c7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="123c7-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="123c7-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="123c7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="123c7-134">CommonParameters</span></span>
<span data-ttu-id="123c7-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="123c7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="123c7-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="123c7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="123c7-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="123c7-137">INPUTS</span></span>

### <span data-ttu-id="123c7-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="123c7-138">-ResourceGroupName</span></span>
<span data-ttu-id="123c7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="123c7-139">System.String</span></span>

### <span data-ttu-id="123c7-140">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="123c7-140">-NamespaceName</span></span>
<span data-ttu-id="123c7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="123c7-141">System.String</span></span>

### <span data-ttu-id="123c7-142">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="123c7-142">-HybridConnectionsName</span></span>
<span data-ttu-id="123c7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="123c7-143">System.String</span></span>

### <span data-ttu-id="123c7-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="123c7-144">-InputObject</span></span>
<span data-ttu-id="123c7-145">Microsoft. Azure. Command. Relay. models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="123c7-145">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="123c7-146">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="123c7-146">-RequiresClientAuthorization</span></span>
<span data-ttu-id="123c7-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="123c7-147">System.Boolean</span></span>

### <span data-ttu-id="123c7-148">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="123c7-148">-UserMetadata</span></span>
<span data-ttu-id="123c7-149">System. String</span><span class="sxs-lookup"><span data-stu-id="123c7-149">System.String</span></span>

## <span data-ttu-id="123c7-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="123c7-150">OUTPUTS</span></span>

### <span data-ttu-id="123c7-151">Microsoft. Azure. Command. Relay. models. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="123c7-151">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

## <span data-ttu-id="123c7-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="123c7-152">NOTES</span></span>

## <span data-ttu-id="123c7-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="123c7-153">RELATED LINKS</span></span>

