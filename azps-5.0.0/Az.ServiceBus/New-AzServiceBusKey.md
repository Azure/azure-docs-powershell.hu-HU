---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: c0c413918a986da4eaea8d9ef5f0f6a091b8b2e4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185873"
---
# <span data-ttu-id="ff2a5-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="ff2a5-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="ff2a5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff2a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ff2a5-103">Újragenerálja az elsődleges vagy másodlagos kapcsolati karakterláncot a szolgáltatási busz névteréhez, illetve a várólistához vagy a témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="ff2a5-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="ff2a5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff2a5-104">SYNTAX</span></span>

### <span data-ttu-id="ff2a5-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ff2a5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff2a5-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff2a5-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ff2a5-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff2a5-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff2a5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff2a5-108">DESCRIPTION</span></span>
<span data-ttu-id="ff2a5-109">A **New-AzServiceBusKey** parancsmag új elsődleges vagy másodlagos kapcsolódási karakterláncokat hoz létre a megadott névtérhez, vagy témakörhöz és engedélyezési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="ff2a5-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="ff2a5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ff2a5-110">EXAMPLES</span></span>

### <span data-ttu-id="ff2a5-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ff2a5-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="ff2a5-112">Újragenerálja a névtér elsődleges vagy másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="ff2a5-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="ff2a5-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="ff2a5-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="ff2a5-114">Az elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása a névtérhez megadott kulcs értékkel.</span><span class="sxs-lookup"><span data-stu-id="ff2a5-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="ff2a5-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="ff2a5-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="ff2a5-116">Újragenerálja a várólista elsődleges vagy másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="ff2a5-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="ff2a5-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="ff2a5-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="ff2a5-118">Az elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása a várólistához megadott kulcs értékkel.</span><span class="sxs-lookup"><span data-stu-id="ff2a5-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="ff2a5-119">Példa 5</span><span class="sxs-lookup"><span data-stu-id="ff2a5-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="ff2a5-120">Újragenerálja a témakör elsődleges vagy másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="ff2a5-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="ff2a5-121">6. példa</span><span class="sxs-lookup"><span data-stu-id="ff2a5-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="ff2a5-122">Az elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása a témakörben megadott kulcs értékkel.</span><span class="sxs-lookup"><span data-stu-id="ff2a5-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="ff2a5-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff2a5-123">PARAMETERS</span></span>

### <span data-ttu-id="ff2a5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff2a5-124">-DefaultProfile</span></span>
<span data-ttu-id="ff2a5-125">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff2a5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff2a5-126">-Érték</span><span class="sxs-lookup"><span data-stu-id="ff2a5-126">-KeyValue</span></span>
<span data-ttu-id="ff2a5-127">Base64 kódolású 256 bites kulcs a SAS-token aláírásához és érvényesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="ff2a5-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="ff2a5-128">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ff2a5-128">-Name</span></span>
<span data-ttu-id="ff2a5-129">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="ff2a5-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="ff2a5-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ff2a5-130">-Namespace</span></span>
<span data-ttu-id="ff2a5-131">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="ff2a5-131">Namespace Name</span></span>

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

### <span data-ttu-id="ff2a5-132">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="ff2a5-132">-Queue</span></span>
<span data-ttu-id="ff2a5-133">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="ff2a5-133">Queue Name</span></span>

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

### <span data-ttu-id="ff2a5-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="ff2a5-134">-RegenerateKey</span></span>
<span data-ttu-id="ff2a5-135">Regenerálódni kulcsok-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="ff2a5-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="ff2a5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff2a5-136">-ResourceGroupName</span></span>
<span data-ttu-id="ff2a5-137">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ff2a5-137">Resource Group Name</span></span>

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

### <span data-ttu-id="ff2a5-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="ff2a5-138">-Topic</span></span>
<span data-ttu-id="ff2a5-139">Téma neve</span><span class="sxs-lookup"><span data-stu-id="ff2a5-139">Topic Name</span></span>

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

### <span data-ttu-id="ff2a5-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff2a5-140">-Confirm</span></span>
<span data-ttu-id="ff2a5-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff2a5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff2a5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff2a5-142">-WhatIf</span></span>
<span data-ttu-id="ff2a5-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff2a5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff2a5-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff2a5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff2a5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff2a5-145">CommonParameters</span></span>
<span data-ttu-id="ff2a5-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff2a5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff2a5-147">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff2a5-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff2a5-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff2a5-148">INPUTS</span></span>

### <span data-ttu-id="ff2a5-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ff2a5-149">System.String</span></span>

## <span data-ttu-id="ff2a5-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff2a5-150">OUTPUTS</span></span>

### <span data-ttu-id="ff2a5-151">Microsoft. Azure. Command. ServiceBus. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="ff2a5-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="ff2a5-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff2a5-152">NOTES</span></span>

## <span data-ttu-id="ff2a5-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff2a5-153">RELATED LINKS</span></span>
