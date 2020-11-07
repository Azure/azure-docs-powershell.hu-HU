---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
ms.openlocfilehash: 3d15269f525047677c20c679311cde877f25fbe4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669503"
---
# <span data-ttu-id="f46e1-101">New-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="f46e1-101">New-AzWcfRelay</span></span>

## <span data-ttu-id="f46e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f46e1-102">SYNOPSIS</span></span>
<span data-ttu-id="f46e1-103">Létrehoz egy WcfRelay a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="f46e1-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="f46e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f46e1-104">SYNTAX</span></span>

### <span data-ttu-id="f46e1-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f46e1-105">WcfRelayInputObjectSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f46e1-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="f46e1-106">WcfRelayPropertiesSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f46e1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f46e1-107">DESCRIPTION</span></span>
<span data-ttu-id="f46e1-108">Az New-AzWcfRelay parancsmag létrehoz egy WcfRelay a megadott továbbító névtérben.</span><span class="sxs-lookup"><span data-stu-id="f46e1-108">The New-AzWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="f46e1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f46e1-109">EXAMPLES</span></span>

### <span data-ttu-id="f46e1-110">Példa 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="f46e1-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:14:46 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : TestWCFRelay2
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="f46e1-111">Új WcfRelay \` -TestWCFRelay2 hoz létre \` a megadott továbbítási névtér \` TestNameSpace – továbbítóban \` .</span><span class="sxs-lookup"><span data-stu-id="f46e1-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="f46e1-112">Példa 2 – tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="f46e1-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:20:08 PM
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

<span data-ttu-id="f46e1-113">Új WcfRelay TestWCFRelay hoz \` létre \` a megadott továbbító névtér \` TestNameSpace-Relay1 \` .</span><span class="sxs-lookup"><span data-stu-id="f46e1-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="f46e1-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f46e1-114">PARAMETERS</span></span>

### <span data-ttu-id="f46e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46e1-115">-DefaultProfile</span></span>
<span data-ttu-id="f46e1-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f46e1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f46e1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f46e1-117">-InputObject</span></span>
<span data-ttu-id="f46e1-118">WcfRelay objektum</span><span class="sxs-lookup"><span data-stu-id="f46e1-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="f46e1-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f46e1-119">-Name</span></span>
<span data-ttu-id="f46e1-120">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="f46e1-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="f46e1-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f46e1-121">-Namespace</span></span>
<span data-ttu-id="f46e1-122">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="f46e1-122">Namespace Name.</span></span>

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

### <span data-ttu-id="f46e1-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="f46e1-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="f46e1-124">True, ha az ügyfél engedélye szükséges ehhez a továbbításhoz; egyéb esetben false</span><span class="sxs-lookup"><span data-stu-id="f46e1-124">true if client authorization is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f46e1-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="f46e1-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="f46e1-126">igaz, ha a továbbításhoz átviteli biztonságra van szükség; egyéb esetben false</span><span class="sxs-lookup"><span data-stu-id="f46e1-126">true if transport security is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f46e1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f46e1-127">-ResourceGroupName</span></span>
<span data-ttu-id="f46e1-128">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="f46e1-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="f46e1-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="f46e1-129">-UserMetadata</span></span>
<span data-ttu-id="f46e1-130">A usermetadata beolvasása vagy beállítása helyőrző a HybridConnection végpont felhasználó által definiált karakterlánc-adatainak tárolására. használható a leíró adatok tárolására, például a csoportok listájára és a partnerek elérhetőségi adataira is, és tárolhatók a felhasználó által definiált konfigurációs beállítások is.</span><span class="sxs-lookup"><span data-stu-id="f46e1-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="f46e1-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="f46e1-131">-WcfRelayType</span></span>
<span data-ttu-id="f46e1-132">WcfRelay típusa</span><span class="sxs-lookup"><span data-stu-id="f46e1-132">WcfRelay Type.</span></span>
<span data-ttu-id="f46e1-133">A lehetséges értékek a következők: "NetTcp" vagy "http"</span><span class="sxs-lookup"><span data-stu-id="f46e1-133">Possible values include: 'NetTcp' or 'Http'</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:
Accepted values: NetTcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f46e1-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f46e1-134">-Confirm</span></span>
<span data-ttu-id="f46e1-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f46e1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f46e1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f46e1-136">-WhatIf</span></span>
<span data-ttu-id="f46e1-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f46e1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f46e1-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f46e1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f46e1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46e1-139">CommonParameters</span></span>
<span data-ttu-id="f46e1-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f46e1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46e1-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f46e1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46e1-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f46e1-142">INPUTS</span></span>

### <span data-ttu-id="f46e1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f46e1-143">System.String</span></span>

### <span data-ttu-id="f46e1-144">Microsoft. Azure. Command. Relay. models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="f46e1-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

### <span data-ttu-id="f46e1-145">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f46e1-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f46e1-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f46e1-146">OUTPUTS</span></span>

### <span data-ttu-id="f46e1-147">Microsoft. Azure. Command. Relay. models. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="f46e1-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="f46e1-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f46e1-148">NOTES</span></span>

## <span data-ttu-id="f46e1-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f46e1-149">RELATED LINKS</span></span>
