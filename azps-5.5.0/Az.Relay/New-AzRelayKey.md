---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: f475d3f661d1bd1696d9ae728998bb609222816d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208598"
---
# <span data-ttu-id="e9f85-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="e9f85-101">New-AzRelayKey</span></span>

## <span data-ttu-id="e9f85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9f85-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f85-103">A megadott továbbítási entitások elsődleges vagy másodlagos kapcsolati karakterláncának újbóli létrehozása (Namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="e9f85-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="e9f85-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e9f85-104">SYNTAX</span></span>

### <span data-ttu-id="e9f85-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9f85-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9f85-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9f85-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9f85-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e9f85-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9f85-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e9f85-108">DESCRIPTION</span></span>
<span data-ttu-id="e9f85-109">A **New-AzRelayKey** parancsmag létrehozza a megadott továbbítási entitások (Namespace/WcfRelay/HybridConnection) elsődleges és másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="e9f85-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="e9f85-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e9f85-110">EXAMPLES</span></span>

### <span data-ttu-id="e9f85-111">1. példa – Névtér</span><span class="sxs-lookup"><span data-stu-id="e9f85-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="e9f85-112">Az adott entitás elsődleges vagy másodlagos kapcsolati karakterláncának újragenerálását Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="e9f85-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="e9f85-113">Example 1.1 - Namespace KeyValue Provided</span><span class="sxs-lookup"><span data-stu-id="e9f85-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="e9f85-114">létrehozza az elsődleges vagy másodlagos kapcsolati karakterláncokat az adott Relay-Namespace megadott kulcsértékkel</span><span class="sxs-lookup"><span data-stu-id="e9f85-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="e9f85-115">2. példa – WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e9f85-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="e9f85-116">Az adott entitás elsődleges vagy másodlagos kapcsolati karakterláncának újragenerálását Relay-WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="e9f85-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="e9f85-117">Example 2.1 - WcfRelay KeyValue Provided</span><span class="sxs-lookup"><span data-stu-id="e9f85-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="e9f85-118">létrehozza az elsődleges vagy másodlagos kapcsolati karakterláncokat az adott Relay-WcfRelay megadott kulcsértékkel</span><span class="sxs-lookup"><span data-stu-id="e9f85-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="e9f85-119">3. példa : Hibrid összekapcsolás</span><span class="sxs-lookup"><span data-stu-id="e9f85-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="e9f85-120">A megadott továbbítási entitások (Namespace/WcfRelay/HybridConnection) elsődleges vagy másodlagos kapcsolati karakterláncának újbóli létrehozása.</span><span class="sxs-lookup"><span data-stu-id="e9f85-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="e9f85-121">3.1. példa – A HybridConnection keyValue érték meg van téve</span><span class="sxs-lookup"><span data-stu-id="e9f85-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="e9f85-122">létrehozza az elsődleges vagy másodlagos kapcsolati karakterláncokat az adott Relay-HybridConnection megadott kulcsértékkel</span><span class="sxs-lookup"><span data-stu-id="e9f85-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="e9f85-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9f85-123">PARAMETERS</span></span>

### <span data-ttu-id="e9f85-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f85-124">-DefaultProfile</span></span>
<span data-ttu-id="e9f85-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9f85-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9f85-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="e9f85-126">-HybridConnection</span></span>
<span data-ttu-id="e9f85-127">Hibrid összekapcsolás neve.</span><span class="sxs-lookup"><span data-stu-id="e9f85-127">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f85-128">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="e9f85-128">-KeyValue</span></span>
<span data-ttu-id="e9f85-129">Egy 256 bites, base64 kódolású kulcs az SAS-jogkivonat aláírásához és érvényességének igazolásához.</span><span class="sxs-lookup"><span data-stu-id="e9f85-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f85-130">-Name</span><span class="sxs-lookup"><span data-stu-id="e9f85-130">-Name</span></span>
<span data-ttu-id="e9f85-131">AuthorizationRule Name (EngedélyezésiSzabály neve) stb.</span><span class="sxs-lookup"><span data-stu-id="e9f85-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="e9f85-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e9f85-132">-Namespace</span></span>
<span data-ttu-id="e9f85-133">Névtér neve.</span><span class="sxs-lookup"><span data-stu-id="e9f85-133">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f85-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="e9f85-134">-RegenerateKey</span></span>
<span data-ttu-id="e9f85-135">A kulcsok újragenerálása – 'PrimaryKey'/'SecondaryKey'.</span><span class="sxs-lookup"><span data-stu-id="e9f85-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9f85-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f85-136">-ResourceGroupName</span></span>
<span data-ttu-id="e9f85-137">Erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e9f85-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="e9f85-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="e9f85-138">-WcfRelay</span></span>
<span data-ttu-id="e9f85-139">WcfRelay Name.</span><span class="sxs-lookup"><span data-stu-id="e9f85-139">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9f85-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9f85-140">-Confirm</span></span>
<span data-ttu-id="e9f85-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e9f85-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9f85-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9f85-142">-WhatIf</span></span>
<span data-ttu-id="e9f85-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e9f85-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9f85-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e9f85-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9f85-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f85-145">CommonParameters</span></span>
<span data-ttu-id="e9f85-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9f85-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f85-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9f85-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f85-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9f85-148">INPUTS</span></span>

### <span data-ttu-id="e9f85-149">System.String</span><span class="sxs-lookup"><span data-stu-id="e9f85-149">System.String</span></span>

## <span data-ttu-id="e9f85-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9f85-150">OUTPUTS</span></span>

### <span data-ttu-id="e9f85-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="e9f85-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="e9f85-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e9f85-152">NOTES</span></span>

## <span data-ttu-id="e9f85-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9f85-153">RELATED LINKS</span></span>
