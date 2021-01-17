---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
ms.openlocfilehash: 8fa9f3e2bbded846569609d9b1bae191d9f5ad89
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468617"
---
# <span data-ttu-id="376f9-101">New-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="376f9-101">New-AzWcfRelay</span></span>

## <span data-ttu-id="376f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="376f9-102">SYNOPSIS</span></span>
<span data-ttu-id="376f9-103">WcfRelay-t hoz létre a megadott Továbbítás névterében.</span><span class="sxs-lookup"><span data-stu-id="376f9-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="376f9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="376f9-104">SYNTAX</span></span>

### <span data-ttu-id="376f9-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="376f9-105">WcfRelayInputObjectSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="376f9-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="376f9-106">WcfRelayPropertiesSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="376f9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="376f9-107">DESCRIPTION</span></span>
<span data-ttu-id="376f9-108">A New-AzWcfRelay parancsmag wcfRelayet hoz létre a megadott Továbbítás névterében.</span><span class="sxs-lookup"><span data-stu-id="376f9-108">The New-AzWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="376f9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="376f9-109">EXAMPLES</span></span>

### <span data-ttu-id="376f9-110">1. példa – InputObject</span><span class="sxs-lookup"><span data-stu-id="376f9-110">Example 1 - InputObject</span></span>
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

<span data-ttu-id="376f9-111">Létrehoz egy új WcfRelay \` TestWCFRelay2-t a \` megadott Relay namespace \` TestNameSpace-Relay \` mezőben.</span><span class="sxs-lookup"><span data-stu-id="376f9-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="376f9-112">2. példa – Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="376f9-112">Example 2 - Properties</span></span>
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

<span data-ttu-id="376f9-113">Létrehoz egy új WcfRelay \` TestWCFRelay-t a \` megadott Relay namespace \` TestNameSpace-Relay1 \` fájlban.</span><span class="sxs-lookup"><span data-stu-id="376f9-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="376f9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="376f9-114">PARAMETERS</span></span>

### <span data-ttu-id="376f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376f9-115">-DefaultProfile</span></span>
<span data-ttu-id="376f9-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="376f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="376f9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="376f9-117">-InputObject</span></span>
<span data-ttu-id="376f9-118">WcfRelay objektum.</span><span class="sxs-lookup"><span data-stu-id="376f9-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="376f9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="376f9-119">-Name</span></span>
<span data-ttu-id="376f9-120">WcfRelay Name.</span><span class="sxs-lookup"><span data-stu-id="376f9-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="376f9-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="376f9-121">-Namespace</span></span>
<span data-ttu-id="376f9-122">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="376f9-122">Namespace Name.</span></span>

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

### <span data-ttu-id="376f9-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="376f9-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="376f9-124">true, ha ügyfélengedélyre van szükség ehhez a továbbítóhoz; ellenkező esetben hamis</span><span class="sxs-lookup"><span data-stu-id="376f9-124">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="376f9-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="376f9-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="376f9-126">true, ha átviteli biztonságra van szükség ehhez a továbbítóhoz; ellenkező esetben hamis</span><span class="sxs-lookup"><span data-stu-id="376f9-126">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="376f9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="376f9-127">-ResourceGroupName</span></span>
<span data-ttu-id="376f9-128">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="376f9-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="376f9-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="376f9-129">-UserMetadata</span></span>
<span data-ttu-id="376f9-130">A usermetadata függvény egy helyőrző, amely a HybridConnection végpont felhasználói karakterlánc-adatait tárolja(pl. leíró adatok tárolására használhatók, például a csoportok listája és kapcsolattartási adataik, valamint a felhasználó által definiált konfigurációs beállítások is tárolhatók.</span><span class="sxs-lookup"><span data-stu-id="376f9-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="376f9-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="376f9-131">-WcfRelayType</span></span>
<span data-ttu-id="376f9-132">WcfRelay Type.</span><span class="sxs-lookup"><span data-stu-id="376f9-132">WcfRelay Type.</span></span>
<span data-ttu-id="376f9-133">Lehetséges értékek: "NetTcp" vagy "Http"</span><span class="sxs-lookup"><span data-stu-id="376f9-133">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="376f9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="376f9-134">-Confirm</span></span>
<span data-ttu-id="376f9-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="376f9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="376f9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="376f9-136">-WhatIf</span></span>
<span data-ttu-id="376f9-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="376f9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="376f9-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="376f9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="376f9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376f9-139">CommonParameters</span></span>
<span data-ttu-id="376f9-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="376f9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376f9-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="376f9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376f9-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="376f9-142">INPUTS</span></span>

### <span data-ttu-id="376f9-143">System.String</span><span class="sxs-lookup"><span data-stu-id="376f9-143">System.String</span></span>

### <span data-ttu-id="376f9-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="376f9-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

### <span data-ttu-id="376f9-145">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="376f9-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="376f9-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="376f9-146">OUTPUTS</span></span>

### <span data-ttu-id="376f9-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="376f9-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="376f9-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="376f9-148">NOTES</span></span>

## <span data-ttu-id="376f9-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="376f9-149">RELATED LINKS</span></span>
