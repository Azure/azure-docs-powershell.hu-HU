---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: c70c5459f87925d04291f4d5ead15f44ef681bb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501428"
---
# <span data-ttu-id="70666-101">New-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="70666-101">New-AzureRmWcfRelay</span></span>

## <span data-ttu-id="70666-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="70666-102">SYNOPSIS</span></span>
<span data-ttu-id="70666-103">Létrehoz egy WcfRelay a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="70666-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70666-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="70666-104">SYNTAX</span></span>

### <span data-ttu-id="70666-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="70666-105">WcfRelayInputObjectSet</span></span>
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70666-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="70666-106">WcfRelayPropertiesSet</span></span>
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-WcfRelayType <String>] [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>]
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70666-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="70666-107">DESCRIPTION</span></span>
<span data-ttu-id="70666-108">Az New-AzureRmWcfRelay parancsmag létrehoz egy WcfRelay a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="70666-108">The New-AzureRmWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="70666-109">Példák</span><span class="sxs-lookup"><span data-stu-id="70666-109">EXAMPLES</span></span>

### <span data-ttu-id="70666-110">Példa 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="70666-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject
```

<span data-ttu-id="70666-111">Új WcfRelay \` -TestWCFRelay2 hoz létre \` a megadott továbbítási névtér \` TestNameSpace – továbbítóban \` .</span><span class="sxs-lookup"><span data-stu-id="70666-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="70666-112">Példa 2 – tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="70666-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"
```

<span data-ttu-id="70666-113">Új WcfRelay TestWCFRelay hoz \` létre \` a megadott továbbító névtér \` TestNameSpace-Relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="70666-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="70666-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="70666-114">PARAMETERS</span></span>

### <span data-ttu-id="70666-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70666-115">-DefaultProfile</span></span>
<span data-ttu-id="70666-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="70666-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70666-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70666-117">-InputObject</span></span>
<span data-ttu-id="70666-118">WcfRelay objektum</span><span class="sxs-lookup"><span data-stu-id="70666-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="70666-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="70666-119">-Name</span></span>
<span data-ttu-id="70666-120">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="70666-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="70666-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="70666-121">-Namespace</span></span>
<span data-ttu-id="70666-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="70666-122">Namespace Name.</span></span>

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

### <span data-ttu-id="70666-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="70666-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="70666-124">True, ha az ügyfél engedélye szükséges ehhez a továbbításhoz; egyéb esetben false</span><span class="sxs-lookup"><span data-stu-id="70666-124">true if client authorization is needed for this relay; otherwise, false</span></span>

```yaml
Type: Boolean
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70666-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="70666-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="70666-126">igaz, ha a továbbításhoz átviteli biztonságra van szükség; egyéb esetben false</span><span class="sxs-lookup"><span data-stu-id="70666-126">true if transport security is needed for this relay; otherwise, false</span></span>

```yaml
Type: Boolean
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70666-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70666-127">-ResourceGroupName</span></span>
<span data-ttu-id="70666-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="70666-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="70666-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="70666-129">-UserMetadata</span></span>
<span data-ttu-id="70666-130">A usermetadata beolvasása vagy beállítása helyőrző a HybridConnection végpont felhasználó által definiált karakterlánc-adatainak tárolására. használható a leíró adatok tárolására, például a csoportok listájára és a partnerek elérhetőségi adataira is, és tárolhatók a felhasználó által definiált konfigurációs beállítások is.</span><span class="sxs-lookup"><span data-stu-id="70666-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="70666-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="70666-131">-WcfRelayType</span></span>
<span data-ttu-id="70666-132">WcfRelay típusa</span><span class="sxs-lookup"><span data-stu-id="70666-132">WcfRelay Type.</span></span>
<span data-ttu-id="70666-133">A lehetséges értékek a következők: "NetTcp" vagy "http"</span><span class="sxs-lookup"><span data-stu-id="70666-133">Possible values include: 'NetTcp' or 'Http'</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 
Accepted values: NetTcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70666-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="70666-134">-Confirm</span></span>
<span data-ttu-id="70666-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="70666-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70666-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70666-136">-WhatIf</span></span>
<span data-ttu-id="70666-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="70666-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70666-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="70666-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70666-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70666-139">CommonParameters</span></span>
<span data-ttu-id="70666-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="70666-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70666-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70666-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70666-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="70666-142">INPUTS</span></span>

### <span data-ttu-id="70666-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70666-143">-ResourceGroupName</span></span>
<span data-ttu-id="70666-144">System. String</span><span class="sxs-lookup"><span data-stu-id="70666-144">System.String</span></span>

### <span data-ttu-id="70666-145">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="70666-145">-NamespaceName</span></span>
<span data-ttu-id="70666-146">System. String</span><span class="sxs-lookup"><span data-stu-id="70666-146">System.String</span></span>

### <span data-ttu-id="70666-147">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="70666-147">-WcfRelayName</span></span>
<span data-ttu-id="70666-148">System. String</span><span class="sxs-lookup"><span data-stu-id="70666-148">System.String</span></span>

### <span data-ttu-id="70666-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70666-149">-InputObject</span></span>
<span data-ttu-id="70666-150">Microsoft. Azure. Command. Relay. models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="70666-150">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="70666-151">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="70666-151">-WcfRelayType</span></span>
<span data-ttu-id="70666-152">System. String</span><span class="sxs-lookup"><span data-stu-id="70666-152">System.String</span></span>

### <span data-ttu-id="70666-153">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="70666-153">-RequiresClientAuthorization</span></span>
<span data-ttu-id="70666-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70666-154">System.Boolean</span></span>

### <span data-ttu-id="70666-155">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="70666-155">-RequiresTransportSecurity</span></span>
<span data-ttu-id="70666-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="70666-156">System.Boolean</span></span>

### <span data-ttu-id="70666-157">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="70666-157">-UserMetadata</span></span>
<span data-ttu-id="70666-158">System. String</span><span class="sxs-lookup"><span data-stu-id="70666-158">System.String</span></span>

## <span data-ttu-id="70666-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="70666-159">OUTPUTS</span></span>

### <span data-ttu-id="70666-160">Példa 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="70666-160">Example 1 - InputObject</span></span>

### <span data-ttu-id="70666-161">Microsoft. Azure. Command. Relay. models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="70666-161">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="70666-162">RelayType: http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:14:46 PM ListenerCount: RequiresClientAuthorization: false RequiresTransportSecurity: true IsDynamic: false UserMetadata: TestWCFRelay2-azonosító:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel: TestNameSpace, Relay1, WcfRelays, TestWCFRelay2</span><span class="sxs-lookup"><span data-stu-id="70666-162">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:14:46 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : TestWCFRelay2 Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="70666-163">Példa 2 – tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="70666-163">Example 2 - Properties</span></span>

### <span data-ttu-id="70666-164">Microsoft. Azure. Command. Relay. models. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="70666-164">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="70666-165">RelayType: NetTcp CreatedAt: 4/26/2017 5:20:08 PM UpdatedAt: 4/26/2017 5:20:08 PM ListenerCount: RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false UserMetadata: user meta Data ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/Namespaces/TestNameSpace-Relay1</span><span class="sxs-lookup"><span data-stu-id="70666-165">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:20:08 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="70666-166">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="70666-166">NOTES</span></span>

## <span data-ttu-id="70666-167">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="70666-167">RELATED LINKS</span></span>

