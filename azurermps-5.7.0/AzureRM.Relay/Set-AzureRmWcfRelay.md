---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: 16df81633d4265b7b52dd2678bb58c80d4a756e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494381"
---
# <span data-ttu-id="af557-101">Set-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="af557-101">Set-AzureRmWcfRelay</span></span>

## <span data-ttu-id="af557-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af557-102">SYNOPSIS</span></span>
<span data-ttu-id="af557-103">Frissíti egy WcfRelay leírását a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="af557-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af557-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af557-104">SYNTAX</span></span>

### <span data-ttu-id="af557-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="af557-105">WcfRelayInputObjectSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af557-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="af557-106">WcfRelayPropertiesSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af557-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="af557-107">DESCRIPTION</span></span>
<span data-ttu-id="af557-108">A Set-AzureRmWcfRelay parancsmag a megadott továbbítási névtérben lévő WcfRelay leírását frissíti.</span><span class="sxs-lookup"><span data-stu-id="af557-108">The Set-AzureRmWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="af557-109">Példák</span><span class="sxs-lookup"><span data-stu-id="af557-109">EXAMPLES</span></span>

### <span data-ttu-id="af557-110">Példa 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="af557-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### <span data-ttu-id="af557-111">Példa 2 – tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="af557-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

<span data-ttu-id="af557-112">Frissíti a megadott WcfRelay egy új leírással a megadott névtérben.</span><span class="sxs-lookup"><span data-stu-id="af557-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="af557-113">Ez a példa frissíti a UserMetadata tulajdonságot új értékkel.</span><span class="sxs-lookup"><span data-stu-id="af557-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="af557-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af557-114">PARAMETERS</span></span>

### <span data-ttu-id="af557-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af557-115">-DefaultProfile</span></span>
<span data-ttu-id="af557-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af557-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af557-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af557-117">-InputObject</span></span>
<span data-ttu-id="af557-118">WcfRelay objektum</span><span class="sxs-lookup"><span data-stu-id="af557-118">WcfRelay object.</span></span>

```yaml
Type: WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af557-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af557-119">-Name</span></span>
<span data-ttu-id="af557-120">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="af557-120">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af557-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="af557-121">-Namespace</span></span>
<span data-ttu-id="af557-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="af557-122">Namespace Name.</span></span>

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

### <span data-ttu-id="af557-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af557-123">-ResourceGroupName</span></span>
<span data-ttu-id="af557-124">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="af557-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="af557-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="af557-125">-UserMetadata</span></span>
<span data-ttu-id="af557-126">A usermetadata beolvasása vagy beállítása helyőrző a HybridConnection végpont felhasználó által definiált karakterlánc-adatainak tárolására. használható a leíró adatok tárolására, például a csoportok listájára és a partnerek elérhetőségi adataira is, és tárolhatók a felhasználó által definiált konfigurációs beállítások is.</span><span class="sxs-lookup"><span data-stu-id="af557-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af557-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="af557-127">-Confirm</span></span>
<span data-ttu-id="af557-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="af557-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af557-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af557-129">-WhatIf</span></span>
<span data-ttu-id="af557-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="af557-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af557-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="af557-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af557-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af557-132">CommonParameters</span></span>
<span data-ttu-id="af557-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af557-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af557-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af557-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af557-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af557-135">INPUTS</span></span>

### <span data-ttu-id="af557-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af557-136">-ResourceGroupName</span></span>
<span data-ttu-id="af557-137">System. String</span><span class="sxs-lookup"><span data-stu-id="af557-137">System.String</span></span>

### <span data-ttu-id="af557-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="af557-138">-NamespaceName</span></span>
<span data-ttu-id="af557-139">System. String</span><span class="sxs-lookup"><span data-stu-id="af557-139">System.String</span></span>

### <span data-ttu-id="af557-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="af557-140">-WcfRelayName</span></span>
<span data-ttu-id="af557-141">System. String</span><span class="sxs-lookup"><span data-stu-id="af557-141">System.String</span></span>

### <span data-ttu-id="af557-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af557-142">-InputObject</span></span>
<span data-ttu-id="af557-143">Microsoft. Azure. Command. Relay. models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="af557-143">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="af557-144">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="af557-144">-WcfRelayType</span></span>
<span data-ttu-id="af557-145">System. String</span><span class="sxs-lookup"><span data-stu-id="af557-145">System.String</span></span>

### <span data-ttu-id="af557-146">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="af557-146">-UserMetadata</span></span>
<span data-ttu-id="af557-147">System. String</span><span class="sxs-lookup"><span data-stu-id="af557-147">System.String</span></span>

## <span data-ttu-id="af557-148">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af557-148">OUTPUTS</span></span>

### <span data-ttu-id="af557-149">Microsoft. Azure. Command. Relay. models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="af557-149">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="af557-150">Példa 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="af557-150">Example 1 - InputObject</span></span>

### <span data-ttu-id="af557-151">Microsoft. Azure. Command. Relay. models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="af557-151">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="af557-152">RelayType: http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:16:50 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true IsDynamic: false UserMetadata: UserMetadata a felhasználó által definiált karakterlánc-adatok tárolása a HybridConnection végponthoz. a desc riptive-adatok (például a csoportok listája és a kapcsolati adatok) tárolására használhatók, a felhasználói konfigurációs beállítások is tárolhatók.</span><span class="sxs-lookup"><span data-stu-id="af557-152">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:16:50 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>
<span data-ttu-id="af557-153">ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/Namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 név: TestWCFRelay2 típus: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="af557-153">Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="af557-154">Példa 2 – tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="af557-154">Example 2 - Properties</span></span>

### <span data-ttu-id="af557-155">Microsoft. Azure. Command. Relay. models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="af557-155">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="af557-156">RelayType: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:26:09 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false UserMetadata: user meta Data ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/Namespaces/TestNameSpace-Relay1</span><span class="sxs-lookup"><span data-stu-id="af557-156">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:26:09 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="af557-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af557-157">NOTES</span></span>

## <span data-ttu-id="af557-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af557-158">RELATED LINKS</span></span>

