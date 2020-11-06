---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 897ecd66665091fd3be1f14b31c00549912a0af8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493028"
---
# <span data-ttu-id="159cf-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="159cf-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="159cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="159cf-102">SYNOPSIS</span></span>
<span data-ttu-id="159cf-103">Megkapja az elsődleges és a másodlagos kapcsolat karakterláncát az adott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="159cf-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="159cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="159cf-104">SYNTAX</span></span>

### <span data-ttu-id="159cf-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="159cf-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="159cf-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="159cf-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="159cf-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="159cf-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="159cf-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="159cf-108">DESCRIPTION</span></span>
<span data-ttu-id="159cf-109">A **Get-AzureRmRelayKey** parancsmag az elsődleges és másodlagos kapcsolati karakterláncokat adja eredményül az adott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="159cf-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="159cf-110">Példák</span><span class="sxs-lookup"><span data-stu-id="159cf-110">EXAMPLES</span></span>

### <span data-ttu-id="159cf-111">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="159cf-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

### <span data-ttu-id="159cf-112">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="159cf-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

### <span data-ttu-id="159cf-113">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="159cf-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="159cf-114">Az elsődleges és másodlagos kapcsolat karakterlánca a megadott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="159cf-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="159cf-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="159cf-115">PARAMETERS</span></span>

### <span data-ttu-id="159cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="159cf-116">-DefaultProfile</span></span>
<span data-ttu-id="159cf-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="159cf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="159cf-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="159cf-118">-HybridConnection</span></span>
<span data-ttu-id="159cf-119">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="159cf-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="159cf-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="159cf-120">-Name</span></span>
<span data-ttu-id="159cf-121">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="159cf-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="159cf-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="159cf-122">-Namespace</span></span>
<span data-ttu-id="159cf-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="159cf-123">Namespace Name.</span></span>

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

### <span data-ttu-id="159cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="159cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="159cf-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="159cf-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="159cf-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="159cf-126">-WcfRelay</span></span>
<span data-ttu-id="159cf-127">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="159cf-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="159cf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="159cf-128">CommonParameters</span></span>
<span data-ttu-id="159cf-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="159cf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="159cf-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="159cf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="159cf-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="159cf-131">INPUTS</span></span>

### <span data-ttu-id="159cf-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="159cf-132">-ResourceGroupName</span></span>
 <span data-ttu-id="159cf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="159cf-133">System.String</span></span> 

### <span data-ttu-id="159cf-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="159cf-134">-NamespaceName</span></span>
 <span data-ttu-id="159cf-135">System. String</span><span class="sxs-lookup"><span data-stu-id="159cf-135">System.String</span></span> 
 

### <span data-ttu-id="159cf-136">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="159cf-136">-HybridConnectionsName</span></span>
 <span data-ttu-id="159cf-137">System. String</span><span class="sxs-lookup"><span data-stu-id="159cf-137">System.String</span></span> 

### <span data-ttu-id="159cf-138">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="159cf-138">-WcfRelayName</span></span>
 <span data-ttu-id="159cf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="159cf-139">System.String</span></span> 

### <span data-ttu-id="159cf-140">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="159cf-140">-Name</span></span>
 <span data-ttu-id="159cf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="159cf-141">System.String</span></span>

## <span data-ttu-id="159cf-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="159cf-142">OUTPUTS</span></span>

### <span data-ttu-id="159cf-143">Microsoft. Azure. Command. Relay. models. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="159cf-143">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="159cf-144">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="159cf-144">Example 1 - Namespace</span></span>
<span data-ttu-id="159cf-145">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # PrimaryKey # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="159cf-145">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="159cf-146">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="159cf-146">Example 2 - WcfRelay</span></span>
<span data-ttu-id="159cf-147">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="159cf-147">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="159cf-148">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="159cf-148">Example 3 - HybridConnection</span></span>
<span data-ttu-id="159cf-149">PrimaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = SB://testnamespace-relay1.servicebus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="159cf-149">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="159cf-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="159cf-150">NOTES</span></span>

## <span data-ttu-id="159cf-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="159cf-151">RELATED LINKS</span></span>

