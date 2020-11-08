---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 87682e5aa7b3c6ab5f7cc5ba4200d73f45960001
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181445"
---
# <span data-ttu-id="d687c-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="d687c-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="d687c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d687c-102">SYNOPSIS</span></span>
<span data-ttu-id="d687c-103">Megkapja az elsődleges és a másodlagos kapcsolat karakterláncát az adott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="d687c-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="d687c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d687c-104">SYNTAX</span></span>

### <span data-ttu-id="d687c-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d687c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d687c-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d687c-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d687c-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d687c-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d687c-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d687c-108">DESCRIPTION</span></span>
<span data-ttu-id="d687c-109">A **Get-AzRelayKey** parancsmag az elsődleges és másodlagos kapcsolati karakterláncokat adja eredményül az adott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="d687c-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="d687c-110">Példák</span><span class="sxs-lookup"><span data-stu-id="d687c-110">EXAMPLES</span></span>

### <span data-ttu-id="d687c-111">Példa 1: Namespace</span><span class="sxs-lookup"><span data-stu-id="d687c-111">Example 1: Namespace</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="d687c-112">2. példa: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="d687c-112">Example 2: WcfRelay</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="d687c-113">3. példa: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="d687c-113">Example 3: HybridConnection</span></span>
```powershell
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="d687c-114">Az elsődleges és másodlagos kapcsolat karakterlánca a megadott továbbítóügynök számára (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="d687c-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="d687c-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d687c-115">PARAMETERS</span></span>

### <span data-ttu-id="d687c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d687c-116">-DefaultProfile</span></span>
<span data-ttu-id="d687c-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d687c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d687c-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="d687c-118">-HybridConnection</span></span>
<span data-ttu-id="d687c-119">HybridConnection neve</span><span class="sxs-lookup"><span data-stu-id="d687c-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="d687c-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d687c-120">-Name</span></span>
<span data-ttu-id="d687c-121">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="d687c-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="d687c-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d687c-122">-Namespace</span></span>
<span data-ttu-id="d687c-123">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="d687c-123">Namespace Name.</span></span>

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

### <span data-ttu-id="d687c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d687c-124">-ResourceGroupName</span></span>
<span data-ttu-id="d687c-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d687c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="d687c-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="d687c-126">-WcfRelay</span></span>
<span data-ttu-id="d687c-127">WcfRelay neve</span><span class="sxs-lookup"><span data-stu-id="d687c-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="d687c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d687c-128">CommonParameters</span></span>
<span data-ttu-id="d687c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d687c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d687c-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d687c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d687c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d687c-131">INPUTS</span></span>

### <span data-ttu-id="d687c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d687c-132">System.String</span></span>

## <span data-ttu-id="d687c-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d687c-133">OUTPUTS</span></span>

### <span data-ttu-id="d687c-134">Microsoft. Azure. Command. Relay. models. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="d687c-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="d687c-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d687c-135">NOTES</span></span>

## <span data-ttu-id="d687c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d687c-136">RELATED LINKS</span></span>
