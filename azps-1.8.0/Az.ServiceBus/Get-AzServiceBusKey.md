---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: c9d6e262acd20616cf070ab061b48a61ccfbba48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669208"
---
# <span data-ttu-id="222f9-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="222f9-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="222f9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="222f9-102">SYNOPSIS</span></span>
<span data-ttu-id="222f9-103">Megkapja az elsődleges és a másodlagos kapcsolódási karakterláncot az adott névtérhez vagy a várólistához, illetve a témakörhöz vagy aliashoz (GeoDR-konfigurációk).</span><span class="sxs-lookup"><span data-stu-id="222f9-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="222f9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="222f9-104">SYNTAX</span></span>

### <span data-ttu-id="222f9-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="222f9-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="222f9-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="222f9-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="222f9-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="222f9-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="222f9-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="222f9-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="222f9-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="222f9-109">DESCRIPTION</span></span>
<span data-ttu-id="222f9-110">A **Get-AzServiceBusKey** parancsmag a megadott névtér vagy várólista (GeoDR-konfigurációk) elsődleges és másodlagos kapcsolati karakterláncát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="222f9-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="222f9-111">Példák</span><span class="sxs-lookup"><span data-stu-id="222f9-111">EXAMPLES</span></span>

### <span data-ttu-id="222f9-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="222f9-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="222f9-113">Az elsődleges és másodlagos kapcsolat karakterlánca a megadott névtérhez</span><span class="sxs-lookup"><span data-stu-id="222f9-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="222f9-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="222f9-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="222f9-115">Az elsődleges és a másodlagos kapcsolat karakterlánca a megadott várólistához.</span><span class="sxs-lookup"><span data-stu-id="222f9-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="222f9-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="222f9-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="222f9-117">A megadott témakör elsődleges és másodlagos kapcsolati karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="222f9-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="222f9-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="222f9-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="222f9-119">Az elsődleges és másodlagos kapcsolat karakterlánca a megadott névtérhez és aliashoz.</span><span class="sxs-lookup"><span data-stu-id="222f9-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="222f9-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="222f9-120">PARAMETERS</span></span>

### <span data-ttu-id="222f9-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="222f9-121">-AliasName</span></span>
<span data-ttu-id="222f9-122">Alias neve</span><span class="sxs-lookup"><span data-stu-id="222f9-122">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="222f9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="222f9-123">-DefaultProfile</span></span>
<span data-ttu-id="222f9-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="222f9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="222f9-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="222f9-125">-Name</span></span>
<span data-ttu-id="222f9-126">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="222f9-126">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="222f9-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="222f9-127">-Namespace</span></span>
<span data-ttu-id="222f9-128">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="222f9-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="222f9-129">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="222f9-129">-Queue</span></span>
<span data-ttu-id="222f9-130">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="222f9-130">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="222f9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="222f9-131">-ResourceGroupName</span></span>
<span data-ttu-id="222f9-132">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="222f9-132">Resource Group Name</span></span>

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

### <span data-ttu-id="222f9-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="222f9-133">-Topic</span></span>
<span data-ttu-id="222f9-134">Téma neve</span><span class="sxs-lookup"><span data-stu-id="222f9-134">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="222f9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="222f9-135">CommonParameters</span></span>
<span data-ttu-id="222f9-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="222f9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="222f9-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="222f9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="222f9-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="222f9-138">INPUTS</span></span>

### <span data-ttu-id="222f9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="222f9-139">System.String</span></span>

## <span data-ttu-id="222f9-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="222f9-140">OUTPUTS</span></span>

### <span data-ttu-id="222f9-141">Microsoft. Azure. Command. ServiceBus. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="222f9-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="222f9-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="222f9-142">NOTES</span></span>

## <span data-ttu-id="222f9-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="222f9-143">RELATED LINKS</span></span>
