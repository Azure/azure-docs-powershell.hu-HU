---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: f475d3f661d1bd1696d9ae728998bb609222816d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184696"
---
# <span data-ttu-id="64a02-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="64a02-101">New-AzRelayKey</span></span>

## <span data-ttu-id="64a02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64a02-102">SYNOPSIS</span></span>
<span data-ttu-id="64a02-103">Az elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása az adott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="64a02-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="64a02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64a02-104">SYNTAX</span></span>

### <span data-ttu-id="64a02-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="64a02-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64a02-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="64a02-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64a02-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="64a02-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64a02-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="64a02-108">DESCRIPTION</span></span>
<span data-ttu-id="64a02-109">A **New-AzRelayKey** parancsmag az elsődleges és másodlagos kapcsolati karakterláncokat hozza létre a megadott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="64a02-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="64a02-110">Példák</span><span class="sxs-lookup"><span data-stu-id="64a02-110">EXAMPLES</span></span>

### <span data-ttu-id="64a02-111">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="64a02-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="64a02-112">Újragenerálja az elsődleges vagy másodlagos kapcsolati karakterláncot az adott Relay-Namespace entitáshoz.</span><span class="sxs-lookup"><span data-stu-id="64a02-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="64a02-113">Példa: 1,1 – a névtér-azonosító megadott értéke</span><span class="sxs-lookup"><span data-stu-id="64a02-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="64a02-114">az elsődleges vagy másodlagos kapcsolódási karakterláncok létrehozása a megadott Relay-Namespace entitáshoz a megadott kulcs értékkel</span><span class="sxs-lookup"><span data-stu-id="64a02-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="64a02-115">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="64a02-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="64a02-116">Újragenerálja az elsődleges vagy másodlagos kapcsolati karakterláncot az adott Relay-WcfRelay entitáshoz.</span><span class="sxs-lookup"><span data-stu-id="64a02-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="64a02-117">Példa 2,1 – a WcfRelay a megadott érték</span><span class="sxs-lookup"><span data-stu-id="64a02-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="64a02-118">az elsődleges vagy másodlagos kapcsolódási karakterláncok létrehozása a megadott Relay-WcfRelay entitáshoz a megadott kulcs értékkel</span><span class="sxs-lookup"><span data-stu-id="64a02-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="64a02-119">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="64a02-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="64a02-120">Újragenerálja az elsődleges vagy másodlagos kapcsolati karakterláncot az adott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="64a02-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="64a02-121">Példa 3,1 – a HybridConnection a megadott érték</span><span class="sxs-lookup"><span data-stu-id="64a02-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="64a02-122">az elsődleges vagy másodlagos kapcsolódási karakterláncok létrehozása a megadott Relay-HybridConnection entitáshoz a megadott kulcs értékkel</span><span class="sxs-lookup"><span data-stu-id="64a02-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="64a02-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64a02-123">PARAMETERS</span></span>

### <span data-ttu-id="64a02-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a02-124">-DefaultProfile</span></span>
<span data-ttu-id="64a02-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64a02-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64a02-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="64a02-126">-HybridConnection</span></span>
<span data-ttu-id="64a02-127">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="64a02-127">HybridConnection Name.</span></span>

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

### <span data-ttu-id="64a02-128">-Érték</span><span class="sxs-lookup"><span data-stu-id="64a02-128">-KeyValue</span></span>
<span data-ttu-id="64a02-129">Base64 kódolású 256 bites kulcs a SAS-token aláírásához és érvényesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="64a02-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="64a02-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64a02-130">-Name</span></span>
<span data-ttu-id="64a02-131">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="64a02-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="64a02-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="64a02-132">-Namespace</span></span>
<span data-ttu-id="64a02-133">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="64a02-133">Namespace Name.</span></span>

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

### <span data-ttu-id="64a02-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="64a02-134">-RegenerateKey</span></span>
<span data-ttu-id="64a02-135">Regenerálódni kulcsok-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="64a02-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="64a02-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a02-136">-ResourceGroupName</span></span>
<span data-ttu-id="64a02-137">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="64a02-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="64a02-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="64a02-138">-WcfRelay</span></span>
<span data-ttu-id="64a02-139">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="64a02-139">WcfRelay Name.</span></span>

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

### <span data-ttu-id="64a02-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="64a02-140">-Confirm</span></span>
<span data-ttu-id="64a02-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64a02-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64a02-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64a02-142">-WhatIf</span></span>
<span data-ttu-id="64a02-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="64a02-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64a02-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64a02-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64a02-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a02-145">CommonParameters</span></span>
<span data-ttu-id="64a02-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64a02-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a02-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64a02-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a02-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64a02-148">INPUTS</span></span>

### <span data-ttu-id="64a02-149">System. String</span><span class="sxs-lookup"><span data-stu-id="64a02-149">System.String</span></span>

## <span data-ttu-id="64a02-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64a02-150">OUTPUTS</span></span>

### <span data-ttu-id="64a02-151">Microsoft. Azure. Command. Relay. models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="64a02-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="64a02-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64a02-152">NOTES</span></span>

## <span data-ttu-id="64a02-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64a02-153">RELATED LINKS</span></span>
