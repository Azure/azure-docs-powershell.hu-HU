---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 44e1571dbd6da015e163a69716f06d3ed3cebde5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672415"
---
# <span data-ttu-id="ea10b-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="ea10b-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="ea10b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea10b-102">SYNOPSIS</span></span>
<span data-ttu-id="ea10b-103">Megkapja az elsődleges és a másodlagos kapcsolat karakterláncát az adott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ea10b-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea10b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea10b-104">SYNTAX</span></span>

### <span data-ttu-id="ea10b-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ea10b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea10b-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ea10b-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea10b-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ea10b-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea10b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea10b-108">DESCRIPTION</span></span>
<span data-ttu-id="ea10b-109">A **Get-AzureRmRelayKey** parancsmag az elsődleges és másodlagos kapcsolati karakterláncokat adja eredményül az adott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ea10b-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="ea10b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ea10b-110">EXAMPLES</span></span>

### <span data-ttu-id="ea10b-111">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="ea10b-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

### <span data-ttu-id="ea10b-112">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ea10b-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

### <span data-ttu-id="ea10b-113">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ea10b-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="ea10b-114">Az elsődleges és másodlagos kapcsolat karakterlánca a megadott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ea10b-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="ea10b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea10b-115">PARAMETERS</span></span>

### <span data-ttu-id="ea10b-116">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ea10b-116">-HybridConnection</span></span>
<span data-ttu-id="ea10b-117">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="ea10b-117">HybridConnection Name.</span></span>

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

### <span data-ttu-id="ea10b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ea10b-118">-Name</span></span>
<span data-ttu-id="ea10b-119">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="ea10b-119">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="ea10b-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ea10b-120">-Namespace</span></span>
<span data-ttu-id="ea10b-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="ea10b-121">Namespace Name.</span></span>

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

### <span data-ttu-id="ea10b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea10b-122">-ResourceGroupName</span></span>
<span data-ttu-id="ea10b-123">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="ea10b-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="ea10b-124">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ea10b-124">-WcfRelay</span></span>
<span data-ttu-id="ea10b-125">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="ea10b-125">WcfRelay Name.</span></span>

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

### <span data-ttu-id="ea10b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea10b-126">-DefaultProfile</span></span>
<span data-ttu-id="ea10b-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea10b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea10b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea10b-128">CommonParameters</span></span>
<span data-ttu-id="ea10b-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea10b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea10b-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea10b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea10b-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea10b-131">INPUTS</span></span>

### <span data-ttu-id="ea10b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea10b-132">-ResourceGroupName</span></span>
 <span data-ttu-id="ea10b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ea10b-133">System.String</span></span> 

### <span data-ttu-id="ea10b-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ea10b-134">-NamespaceName</span></span>
 <span data-ttu-id="ea10b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ea10b-135">System.String</span></span> 
 

### <span data-ttu-id="ea10b-136">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="ea10b-136">-HybridConnectionsName</span></span>
 <span data-ttu-id="ea10b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ea10b-137">System.String</span></span> 

### <span data-ttu-id="ea10b-138">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="ea10b-138">-WcfRelayName</span></span>
 <span data-ttu-id="ea10b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ea10b-139">System.String</span></span> 

### <span data-ttu-id="ea10b-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ea10b-140">-Name</span></span>
 <span data-ttu-id="ea10b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ea10b-141">System.String</span></span>

## <span data-ttu-id="ea10b-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea10b-142">OUTPUTS</span></span>

### <span data-ttu-id="ea10b-143">Microsoft. Azure. Command. Relay. models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="ea10b-143">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="ea10b-144">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="ea10b-144">Example 1 - Namespace</span></span>
<span data-ttu-id="ea10b-145">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # PrimaryKey # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="ea10b-145">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="ea10b-146">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ea10b-146">Example 2 - WcfRelay</span></span>
<span data-ttu-id="ea10b-147">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="ea10b-147">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="ea10b-148">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ea10b-148">Example 3 - HybridConnection</span></span>
<span data-ttu-id="ea10b-149">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="ea10b-149">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="ea10b-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea10b-150">NOTES</span></span>

## <span data-ttu-id="ea10b-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea10b-151">RELATED LINKS</span></span>

