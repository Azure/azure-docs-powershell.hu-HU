---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 68ba115bb74bf0eae780944037532b0d37424704
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669521"
---
# <span data-ttu-id="c690c-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="c690c-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="c690c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c690c-102">SYNOPSIS</span></span>
<span data-ttu-id="c690c-103">Megkapja az elsődleges és a másodlagos kapcsolat karakterláncát az adott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="c690c-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="c690c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c690c-104">SYNTAX</span></span>

### <span data-ttu-id="c690c-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c690c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c690c-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c690c-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c690c-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c690c-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c690c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c690c-108">DESCRIPTION</span></span>
<span data-ttu-id="c690c-109">A **Get-AzRelayKey** parancsmag az elsődleges és másodlagos kapcsolati karakterláncokat adja eredményül az adott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="c690c-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="c690c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c690c-110">EXAMPLES</span></span>

### <span data-ttu-id="c690c-111">Példa 1 – névtér</span><span class="sxs-lookup"><span data-stu-id="c690c-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="c690c-112">Példa 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c690c-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="c690c-113">Példa: 3 – HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c690c-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="c690c-114">Az elsődleges és másodlagos kapcsolat karakterlánca a megadott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="c690c-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="c690c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c690c-115">PARAMETERS</span></span>

### <span data-ttu-id="c690c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c690c-116">-DefaultProfile</span></span>
<span data-ttu-id="c690c-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c690c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c690c-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="c690c-118">-HybridConnection</span></span>
<span data-ttu-id="c690c-119">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="c690c-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="c690c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c690c-120">-Name</span></span>
<span data-ttu-id="c690c-121">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="c690c-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="c690c-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c690c-122">-Namespace</span></span>
<span data-ttu-id="c690c-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="c690c-123">Namespace Name.</span></span>

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

### <span data-ttu-id="c690c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c690c-124">-ResourceGroupName</span></span>
<span data-ttu-id="c690c-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="c690c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c690c-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="c690c-126">-WcfRelay</span></span>
<span data-ttu-id="c690c-127">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="c690c-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="c690c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c690c-128">CommonParameters</span></span>
<span data-ttu-id="c690c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c690c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c690c-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c690c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c690c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c690c-131">INPUTS</span></span>

### <span data-ttu-id="c690c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c690c-132">System.String</span></span>

## <span data-ttu-id="c690c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c690c-133">OUTPUTS</span></span>

### <span data-ttu-id="c690c-134">Microsoft. Azure. Command. Relay. models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="c690c-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="c690c-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c690c-135">NOTES</span></span>

## <span data-ttu-id="c690c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c690c-136">RELATED LINKS</span></span>
