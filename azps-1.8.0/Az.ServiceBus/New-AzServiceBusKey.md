---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: 46a3551e309504d9938359a0fed4d37860fcb524
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669185"
---
# <span data-ttu-id="6bfed-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="6bfed-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="6bfed-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6bfed-102">SYNOPSIS</span></span>
<span data-ttu-id="6bfed-103">Újragenerálja az elsődleges vagy másodlagos kapcsolati karakterláncot a szolgáltatási busz névteréhez, illetve a várólistához vagy a témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="6bfed-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="6bfed-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6bfed-104">SYNTAX</span></span>

### <span data-ttu-id="6bfed-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6bfed-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6bfed-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6bfed-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6bfed-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6bfed-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6bfed-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6bfed-108">DESCRIPTION</span></span>
<span data-ttu-id="6bfed-109">A **New-AzServiceBusKey** parancsmag új elsődleges vagy másodlagos kapcsolódási karakterláncokat hoz létre a megadott névtérhez, vagy témakörhöz és engedélyezési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="6bfed-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="6bfed-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6bfed-110">EXAMPLES</span></span>

### <span data-ttu-id="6bfed-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6bfed-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="6bfed-112">Újragenerálja a névtér elsődleges vagy másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="6bfed-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="6bfed-113">Példa 1,1</span><span class="sxs-lookup"><span data-stu-id="6bfed-113">Example 1.1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="6bfed-114">Az elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása a névtérhez megadott kulcs értékkel.</span><span class="sxs-lookup"><span data-stu-id="6bfed-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="6bfed-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="6bfed-115">Example 2</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="6bfed-116">Újragenerálja a várólista elsődleges vagy másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="6bfed-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="6bfed-117">Példa 2,2</span><span class="sxs-lookup"><span data-stu-id="6bfed-117">Example 2.2</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="6bfed-118">Az elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása a várólistához megadott kulcs értékkel.</span><span class="sxs-lookup"><span data-stu-id="6bfed-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="6bfed-119">3. példa</span><span class="sxs-lookup"><span data-stu-id="6bfed-119">Example 3</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="6bfed-120">Újragenerálja a témakör elsődleges vagy másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="6bfed-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="6bfed-121">Példa 3,1</span><span class="sxs-lookup"><span data-stu-id="6bfed-121">Example 3.1</span></span>
```
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="6bfed-122">Az elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása a témakörben megadott kulcs értékkel.</span><span class="sxs-lookup"><span data-stu-id="6bfed-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="6bfed-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6bfed-123">PARAMETERS</span></span>

### <span data-ttu-id="6bfed-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bfed-124">-DefaultProfile</span></span>
<span data-ttu-id="6bfed-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6bfed-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bfed-126">-Érték</span><span class="sxs-lookup"><span data-stu-id="6bfed-126">-KeyValue</span></span>
<span data-ttu-id="6bfed-127">Base64 kódolású 256 bites kulcs a SAS-token aláírásához és érvényesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="6bfed-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="6bfed-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6bfed-128">-Name</span></span>
<span data-ttu-id="6bfed-129">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="6bfed-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="6bfed-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6bfed-130">-Namespace</span></span>
<span data-ttu-id="6bfed-131">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="6bfed-131">Namespace Name</span></span>

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

### <span data-ttu-id="6bfed-132">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="6bfed-132">-Queue</span></span>
<span data-ttu-id="6bfed-133">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="6bfed-133">Queue Name</span></span>

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

### <span data-ttu-id="6bfed-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="6bfed-134">-RegenerateKey</span></span>
<span data-ttu-id="6bfed-135">Regenerálódni kulcsok-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="6bfed-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bfed-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bfed-136">-ResourceGroupName</span></span>
<span data-ttu-id="6bfed-137">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="6bfed-137">Resource Group Name</span></span>

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

### <span data-ttu-id="6bfed-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="6bfed-138">-Topic</span></span>
<span data-ttu-id="6bfed-139">Téma neve</span><span class="sxs-lookup"><span data-stu-id="6bfed-139">Topic Name</span></span>

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

### <span data-ttu-id="6bfed-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6bfed-140">-Confirm</span></span>
<span data-ttu-id="6bfed-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6bfed-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bfed-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bfed-142">-WhatIf</span></span>
<span data-ttu-id="6bfed-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6bfed-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bfed-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6bfed-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bfed-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bfed-145">CommonParameters</span></span>
<span data-ttu-id="6bfed-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6bfed-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bfed-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bfed-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bfed-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bfed-148">INPUTS</span></span>

### <span data-ttu-id="6bfed-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6bfed-149">System.String</span></span>

## <span data-ttu-id="6bfed-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6bfed-150">OUTPUTS</span></span>

### <span data-ttu-id="6bfed-151">Microsoft. Azure. Command. ServiceBus. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="6bfed-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="6bfed-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6bfed-152">NOTES</span></span>

## <span data-ttu-id="6bfed-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6bfed-153">RELATED LINKS</span></span>
