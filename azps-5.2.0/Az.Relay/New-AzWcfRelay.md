---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
ms.openlocfilehash: 8fa9f3e2bbded846569609d9b1bae191d9f5ad89
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359504"
---
# <span data-ttu-id="f46ec-101">New-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="f46ec-101">New-AzWcfRelay</span></span>

## <span data-ttu-id="f46ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f46ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f46ec-103">WcfRelay-t hoz létre a megadott Továbbítás névterében.</span><span class="sxs-lookup"><span data-stu-id="f46ec-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="f46ec-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f46ec-104">SYNTAX</span></span>

### <span data-ttu-id="f46ec-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f46ec-105">WcfRelayInputObjectSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f46ec-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="f46ec-106">WcfRelayPropertiesSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f46ec-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f46ec-107">DESCRIPTION</span></span>
<span data-ttu-id="f46ec-108">A New-AzWcfRelay parancsmag wcfRelayet hoz létre a megadott Továbbítás névterében.</span><span class="sxs-lookup"><span data-stu-id="f46ec-108">The New-AzWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="f46ec-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f46ec-109">EXAMPLES</span></span>

### <span data-ttu-id="f46ec-110">1. példa – InputObject</span><span class="sxs-lookup"><span data-stu-id="f46ec-110">Example 1 - InputObject</span></span>
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

<span data-ttu-id="f46ec-111">Létrehoz egy új WcfRelay \` TestWCFRelay2-t a \` megadott Relay namespace \` TestNameSpace-Relay \` mezőben.</span><span class="sxs-lookup"><span data-stu-id="f46ec-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="f46ec-112">2. példa – Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="f46ec-112">Example 2 - Properties</span></span>
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

<span data-ttu-id="f46ec-113">Létrehoz egy új WcfRelay \` TestWCFRelay-t a \` megadott Relay namespace \` TestNameSpace-Relay1 \` fájlban.</span><span class="sxs-lookup"><span data-stu-id="f46ec-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="f46ec-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f46ec-114">PARAMETERS</span></span>

### <span data-ttu-id="f46ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f46ec-115">-DefaultProfile</span></span>
<span data-ttu-id="f46ec-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f46ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f46ec-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f46ec-117">-InputObject</span></span>
<span data-ttu-id="f46ec-118">WcfRelay objektum.</span><span class="sxs-lookup"><span data-stu-id="f46ec-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="f46ec-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f46ec-119">-Name</span></span>
<span data-ttu-id="f46ec-120">WcfRelay Name.</span><span class="sxs-lookup"><span data-stu-id="f46ec-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="f46ec-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f46ec-121">-Namespace</span></span>
<span data-ttu-id="f46ec-122">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="f46ec-122">Namespace Name.</span></span>

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

### <span data-ttu-id="f46ec-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="f46ec-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="f46ec-124">true, ha ügyfélengedélyre van szükség ehhez a továbbítóhoz; ellenkező esetben hamis</span><span class="sxs-lookup"><span data-stu-id="f46ec-124">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="f46ec-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="f46ec-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="f46ec-126">true, ha átviteli biztonságra van szükség ehhez a továbbítóhoz; ellenkező esetben hamis</span><span class="sxs-lookup"><span data-stu-id="f46ec-126">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="f46ec-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f46ec-127">-ResourceGroupName</span></span>
<span data-ttu-id="f46ec-128">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f46ec-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="f46ec-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="f46ec-129">-UserMetadata</span></span>
<span data-ttu-id="f46ec-130">A usermetadata függvény egy helyőrző, amely a HybridConnection végpont felhasználói karakterlánc-adatait tárolja(pl. leíró adatok tárolására használhatók, például a csoportok listája és kapcsolattartási adataik, valamint a felhasználó által definiált konfigurációs beállítások is tárolhatók.</span><span class="sxs-lookup"><span data-stu-id="f46ec-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="f46ec-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="f46ec-131">-WcfRelayType</span></span>
<span data-ttu-id="f46ec-132">WcfRelay Type.</span><span class="sxs-lookup"><span data-stu-id="f46ec-132">WcfRelay Type.</span></span>
<span data-ttu-id="f46ec-133">Lehetséges értékek: "NetTcp" vagy "Http"</span><span class="sxs-lookup"><span data-stu-id="f46ec-133">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="f46ec-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f46ec-134">-Confirm</span></span>
<span data-ttu-id="f46ec-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f46ec-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f46ec-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f46ec-136">-WhatIf</span></span>
<span data-ttu-id="f46ec-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f46ec-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f46ec-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f46ec-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f46ec-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f46ec-139">CommonParameters</span></span>
<span data-ttu-id="f46ec-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f46ec-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f46ec-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f46ec-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f46ec-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f46ec-142">INPUTS</span></span>

### <span data-ttu-id="f46ec-143">System.String</span><span class="sxs-lookup"><span data-stu-id="f46ec-143">System.String</span></span>

### <span data-ttu-id="f46ec-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="f46ec-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

### <span data-ttu-id="f46ec-145">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f46ec-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f46ec-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f46ec-146">OUTPUTS</span></span>

### <span data-ttu-id="f46ec-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="f46ec-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="f46ec-148">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f46ec-148">NOTES</span></span>

## <span data-ttu-id="f46ec-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f46ec-149">RELATED LINKS</span></span>
