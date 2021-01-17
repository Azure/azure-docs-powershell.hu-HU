---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 04022129d6709cf7dceea128b2813f97a5404234
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368071"
---
# <span data-ttu-id="a9d4c-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="a9d4c-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="a9d4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d4c-103">Hibrid összekapcsolást hoz létre a megadott Továbbítás névterében.</span><span class="sxs-lookup"><span data-stu-id="a9d4c-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="a9d4c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a9d4c-104">SYNTAX</span></span>

### <span data-ttu-id="a9d4c-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a9d4c-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9d4c-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="a9d4c-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9d4c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a9d4c-107">DESCRIPTION</span></span>
<span data-ttu-id="a9d4c-108">A New-AzRelayHybridConnection parancsmag hibrid összekapcsolást hoz létre a megadott Továbbítás névterében.</span><span class="sxs-lookup"><span data-stu-id="a9d4c-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="a9d4c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a9d4c-109">EXAMPLES</span></span>

### <span data-ttu-id="a9d4c-110">1. példa – InputObject</span><span class="sxs-lookup"><span data-stu-id="a9d4c-110">Example 1 - InputObject</span></span>
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

<span data-ttu-id="a9d4c-111">Létrehoz egy új HybirdConnection \` TestHybirdConnection2-t a \` megadott Relay namespace \` TestNameSpace-HybirdConnection \` fájlban.</span><span class="sxs-lookup"><span data-stu-id="a9d4c-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="a9d4c-112">2. példa – Tulajdonságok</span><span class="sxs-lookup"><span data-stu-id="a9d4c-112">Example 2 - Properties</span></span>
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

<span data-ttu-id="a9d4c-113">Létrehoz egy új HybirdConnection \` TestHybirdConnection1-et \` a megadott Relay namespace \` TestNameSpace-HybirdConnection \` fájlban.</span><span class="sxs-lookup"><span data-stu-id="a9d4c-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="a9d4c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9d4c-114">PARAMETERS</span></span>

### <span data-ttu-id="a9d4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d4c-115">-DefaultProfile</span></span>
<span data-ttu-id="a9d4c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9d4c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9d4c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9d4c-117">-InputObject</span></span>
<span data-ttu-id="a9d4c-118">HybridConnections objektum.</span><span class="sxs-lookup"><span data-stu-id="a9d4c-118">HybridConnections object.</span></span>

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

### <span data-ttu-id="a9d4c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a9d4c-119">-Name</span></span>
<span data-ttu-id="a9d4c-120">HybridConnections Name.</span><span class="sxs-lookup"><span data-stu-id="a9d4c-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="a9d4c-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a9d4c-121">-Namespace</span></span>
<span data-ttu-id="a9d4c-122">Namespace Name (Név)</span><span class="sxs-lookup"><span data-stu-id="a9d4c-122">Namespace Name.</span></span>

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

### <span data-ttu-id="a9d4c-123">-RequiresClientAuthorization</span><span class="sxs-lookup"><span data-stu-id="a9d4c-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="a9d4c-124">true, ha ügyfél-hitelesítés szükséges ehhez a HibridConnections szolgáltatáshoz; ellenkező esetben hamis</span><span class="sxs-lookup"><span data-stu-id="a9d4c-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

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

### <span data-ttu-id="a9d4c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9d4c-125">-ResourceGroupName</span></span>
<span data-ttu-id="a9d4c-126">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a9d4c-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="a9d4c-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="a9d4c-127">-UserMetadata</span></span>
<span data-ttu-id="a9d4c-128">A usermetadata függvény egy helyőrző, amely a HybridConnection végpont felhasználói karakterlánc-adatait tárolja(pl. leíró adatok tárolására használhatók, például a csoportok listája és kapcsolattartási adataik, valamint a felhasználó által definiált konfigurációs beállítások is tárolhatók.</span><span class="sxs-lookup"><span data-stu-id="a9d4c-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="a9d4c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a9d4c-129">-Confirm</span></span>
<span data-ttu-id="a9d4c-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a9d4c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9d4c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9d4c-131">-WhatIf</span></span>
<span data-ttu-id="a9d4c-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a9d4c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9d4c-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a9d4c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9d4c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d4c-134">CommonParameters</span></span>
<span data-ttu-id="a9d4c-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9d4c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d4c-136">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d4c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d4c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9d4c-137">INPUTS</span></span>

### <span data-ttu-id="a9d4c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a9d4c-138">System.String</span></span>

### <span data-ttu-id="a9d4c-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="a9d4c-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

### <span data-ttu-id="a9d4c-140">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a9d4c-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a9d4c-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9d4c-141">OUTPUTS</span></span>

### <span data-ttu-id="a9d4c-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="a9d4c-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="a9d4c-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a9d4c-143">NOTES</span></span>

## <span data-ttu-id="a9d4c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9d4c-144">RELATED LINKS</span></span>
