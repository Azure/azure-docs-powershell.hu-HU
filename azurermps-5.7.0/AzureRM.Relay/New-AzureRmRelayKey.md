---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 050d6477a25922236dc2d9d2e28db1228f4666fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501432"
---
# <span data-ttu-id="c4e1c-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="c4e1c-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="c4e1c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="c4e1c-103">Az elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása az adott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection)</span><span class="sxs-lookup"><span data-stu-id="c4e1c-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4e1c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4e1c-104">SYNTAX</span></span>

### <span data-ttu-id="c4e1c-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4e1c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4e1c-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4e1c-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4e1c-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4e1c-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4e1c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4e1c-108">DESCRIPTION</span></span>
<span data-ttu-id="c4e1c-109">A **New-AzureRmRelayKey** parancsmag az elsődleges és másodlagos kapcsolati karakterláncokat hozza létre a megadott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="c4e1c-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="c4e1c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c4e1c-110">EXAMPLES</span></span>

### <span data-ttu-id="c4e1c-111">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="c4e1c-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="c4e1c-112">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c4e1c-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="c4e1c-113">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c4e1c-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="c4e1c-114">Újragenerálja az elsődleges vagy másodlagos kapcsolati karakterláncot az adott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="c4e1c-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="c4e1c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4e1c-115">PARAMETERS</span></span>

### <span data-ttu-id="c4e1c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4e1c-116">-DefaultProfile</span></span>
<span data-ttu-id="c4e1c-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4e1c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4e1c-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c4e1c-118">-HybridConnection</span></span>
<span data-ttu-id="c4e1c-119">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="c4e1c-119">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4e1c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4e1c-120">-Name</span></span>
<span data-ttu-id="c4e1c-121">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="c4e1c-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="c4e1c-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c4e1c-122">-Namespace</span></span>
<span data-ttu-id="c4e1c-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="c4e1c-123">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4e1c-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="c4e1c-124">-RegenerateKey</span></span>
<span data-ttu-id="c4e1c-125">Regenerálódni kulcsok-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="c4e1c-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e1c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4e1c-126">-ResourceGroupName</span></span>
<span data-ttu-id="c4e1c-127">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c4e1c-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="c4e1c-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c4e1c-128">-WcfRelay</span></span>
<span data-ttu-id="c4e1c-129">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="c4e1c-129">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4e1c-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c4e1c-130">-Confirm</span></span>
<span data-ttu-id="c4e1c-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c4e1c-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e1c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4e1c-132">-WhatIf</span></span>
<span data-ttu-id="c4e1c-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c4e1c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4e1c-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c4e1c-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4e1c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4e1c-135">CommonParameters</span></span>
<span data-ttu-id="c4e1c-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4e1c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4e1c-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4e1c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4e1c-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4e1c-138">INPUTS</span></span>

### <span data-ttu-id="c4e1c-139">-ResourceGroupNameName</span><span class="sxs-lookup"><span data-stu-id="c4e1c-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="c4e1c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c4e1c-140">System.String</span></span> 

### <span data-ttu-id="c4e1c-141">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c4e1c-141">-NamespaceName</span></span>
 <span data-ttu-id="c4e1c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c4e1c-142">System.String</span></span> 
 

### <span data-ttu-id="c4e1c-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="c4e1c-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="c4e1c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c4e1c-144">System.String</span></span> 

### <span data-ttu-id="c4e1c-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="c4e1c-145">-WcfRelayName</span></span>
 <span data-ttu-id="c4e1c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c4e1c-146">System.String</span></span> 

### <span data-ttu-id="c4e1c-147">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c4e1c-147">-Name</span></span>
 <span data-ttu-id="c4e1c-148">System. String</span><span class="sxs-lookup"><span data-stu-id="c4e1c-148">System.String</span></span>

### <span data-ttu-id="c4e1c-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="c4e1c-149">-RegenerateKeys</span></span>
 <span data-ttu-id="c4e1c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c4e1c-150">System.String</span></span>

## <span data-ttu-id="c4e1c-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4e1c-151">OUTPUTS</span></span>

### <span data-ttu-id="c4e1c-152">Microsoft. Azure. Command. Relay. models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="c4e1c-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="c4e1c-153">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="c4e1c-153">Example 1 - Namespace</span></span>
<span data-ttu-id="c4e1c-154">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # PrimaryKey # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="c4e1c-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="c4e1c-155">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c4e1c-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="c4e1c-156">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="c4e1c-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="c4e1c-157">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c4e1c-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="c4e1c-158">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="c4e1c-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="c4e1c-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4e1c-159">NOTES</span></span>

## <span data-ttu-id="c4e1c-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4e1c-160">RELATED LINKS</span></span>

