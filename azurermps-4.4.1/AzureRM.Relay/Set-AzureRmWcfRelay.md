---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: af4927631b126f068495b3b130dfc560874834cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672199"
---
# <span data-ttu-id="288ba-101">Set-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="288ba-101">Set-AzureRmWcfRelay</span></span>

## <span data-ttu-id="288ba-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="288ba-102">SYNOPSIS</span></span>
<span data-ttu-id="288ba-103">Frissíti egy WcfRelay leírását a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="288ba-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="288ba-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="288ba-104">SYNTAX</span></span>

### <span data-ttu-id="288ba-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="288ba-105">WcfRelayInputObjectSet</span></span>
```
Set-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="288ba-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="288ba-106">WcfRelayPropertiesSet</span></span>
```
Set-AzureRmWcfRelay -ResourceGroupName <String> -Namespace <String> -Name <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="288ba-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="288ba-107">DESCRIPTION</span></span>
<span data-ttu-id="288ba-108">A Set-AzureRmWcfRelay parancsmag a megadott továbbítási névtérben lévő WcfRelay leírását frissíti.</span><span class="sxs-lookup"><span data-stu-id="288ba-108">The Set-AzureRmWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="288ba-109">Példák</span><span class="sxs-lookup"><span data-stu-id="288ba-109">EXAMPLES</span></span>

### <span data-ttu-id="288ba-110">Példa 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="288ba-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### <span data-ttu-id="288ba-111">Példa 2 – tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="288ba-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

<span data-ttu-id="288ba-112">Frissíti a megadott WcfRelay egy új leírással a megadott névtérben.</span><span class="sxs-lookup"><span data-stu-id="288ba-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="288ba-113">Ez a példa frissíti a UserMetadata tulajdonságot új értékkel.</span><span class="sxs-lookup"><span data-stu-id="288ba-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="288ba-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="288ba-114">PARAMETERS</span></span>

### <span data-ttu-id="288ba-115">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="288ba-115">-UserMetadata</span></span>
<span data-ttu-id="288ba-116">A usermetadata beolvasása vagy beállítása helyőrző a HybridConnection végpont felhasználó által definiált karakterlánc-adatainak tárolására. használható a leíró adatok tárolására, például a csoportok listájára és a partnerek elérhetőségi adataira is, és tárolhatók a felhasználó által definiált konfigurációs beállítások is.</span><span class="sxs-lookup"><span data-stu-id="288ba-116">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="288ba-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="288ba-117">-Confirm</span></span>
<span data-ttu-id="288ba-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="288ba-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="288ba-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="288ba-119">-WhatIf</span></span>
<span data-ttu-id="288ba-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="288ba-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="288ba-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="288ba-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="288ba-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="288ba-122">-InputObject</span></span>
<span data-ttu-id="288ba-123">WcfRelay objektum</span><span class="sxs-lookup"><span data-stu-id="288ba-123">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="288ba-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="288ba-124">-Name</span></span>
<span data-ttu-id="288ba-125">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="288ba-125">WcfRelay Name.</span></span>

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

### <span data-ttu-id="288ba-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="288ba-126">-Namespace</span></span>
<span data-ttu-id="288ba-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="288ba-127">Namespace Name.</span></span>

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

### <span data-ttu-id="288ba-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="288ba-128">-ResourceGroupName</span></span>
<span data-ttu-id="288ba-129">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="288ba-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="288ba-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="288ba-130">-DefaultProfile</span></span>
<span data-ttu-id="288ba-131">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="288ba-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="288ba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="288ba-132">CommonParameters</span></span>
<span data-ttu-id="288ba-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="288ba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="288ba-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="288ba-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="288ba-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="288ba-135">INPUTS</span></span>

### <span data-ttu-id="288ba-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="288ba-136">-ResourceGroupName</span></span>
<span data-ttu-id="288ba-137">System. String</span><span class="sxs-lookup"><span data-stu-id="288ba-137">System.String</span></span>

### <span data-ttu-id="288ba-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="288ba-138">-NamespaceName</span></span>
<span data-ttu-id="288ba-139">System. String</span><span class="sxs-lookup"><span data-stu-id="288ba-139">System.String</span></span>

### <span data-ttu-id="288ba-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="288ba-140">-WcfRelayName</span></span>
<span data-ttu-id="288ba-141">System. String</span><span class="sxs-lookup"><span data-stu-id="288ba-141">System.String</span></span>

### <span data-ttu-id="288ba-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="288ba-142">-InputObject</span></span>
<span data-ttu-id="288ba-143">Microsoft. Azure. Command. Relay. models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="288ba-143">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="288ba-144">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="288ba-144">-WcfRelayType</span></span>
<span data-ttu-id="288ba-145">System. String</span><span class="sxs-lookup"><span data-stu-id="288ba-145">System.String</span></span>

### <span data-ttu-id="288ba-146">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="288ba-146">-UserMetadata</span></span>
<span data-ttu-id="288ba-147">System. String</span><span class="sxs-lookup"><span data-stu-id="288ba-147">System.String</span></span>

## <span data-ttu-id="288ba-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="288ba-148">OUTPUTS</span></span>

### <span data-ttu-id="288ba-149">Microsoft. Azure. Command. Relay. models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="288ba-149">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="288ba-150">Példa 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="288ba-150">Example 1 - InputObject</span></span>

### <span data-ttu-id="288ba-151">Microsoft. Azure. Command. Relay. models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="288ba-151">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="288ba-152">RelayType: http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:16:50 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true IsDynamic: false UserMetadata: UserMetadata a felhasználó által definiált karakterlánc-adatok tárolása a HybridConnection végponthoz. a desc riptive-adatok (például a csoportok listája és a kapcsolati adatok) tárolására használhatók, a felhasználói konfigurációs beállítások is tárolhatók.</span><span class="sxs-lookup"><span data-stu-id="288ba-152">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:16:50 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>
<span data-ttu-id="288ba-153">ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 név: TestWCFRelay2 típus: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="288ba-153">Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="288ba-154">Példa 2 – tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="288ba-154">Example 2 - Properties</span></span>

### <span data-ttu-id="288ba-155">Microsoft. Azure. Command. Relay. models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="288ba-155">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="288ba-156">RelayType: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:26:09 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false UserMetadata: user meta Data ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/Namespaces/TestNameSpace-Relay1</span><span class="sxs-lookup"><span data-stu-id="288ba-156">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:26:09 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="288ba-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="288ba-157">NOTES</span></span>

## <span data-ttu-id="288ba-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="288ba-158">RELATED LINKS</span></span>

