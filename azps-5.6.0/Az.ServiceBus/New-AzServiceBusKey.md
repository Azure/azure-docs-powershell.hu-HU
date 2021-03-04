---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: ac3b98089a3bbb710680269692685a32ef7adc03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918090"
---
# <span data-ttu-id="7bd2c-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="7bd2c-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="7bd2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bd2c-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd2c-103">A Szolgáltatásbusz névterében, illetve várólistában vagy témakörben található elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="7bd2c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7bd2c-104">SYNTAX</span></span>

### <span data-ttu-id="7bd2c-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7bd2c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7bd2c-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7bd2c-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7bd2c-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7bd2c-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7bd2c-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7bd2c-108">DESCRIPTION</span></span>
<span data-ttu-id="7bd2c-109">A **New-AzServiceBusKey** parancsmag új elsődleges vagy másodlagos kapcsolati karakterláncokat hoz létre a megadott névtérhez, várólistához vagy témakörhez és engedélyezési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="7bd2c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7bd2c-110">EXAMPLES</span></span>

### <span data-ttu-id="7bd2c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="7bd2c-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="7bd2c-112">A névtér elsődleges vagy másodlagos kapcsolati karakterláncának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="7bd2c-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="7bd2c-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="7bd2c-114">A névtérhez megadott kulcsértékkel újra létrehozza az elsődleges vagy másodlagos kapcsolati karakterláncokat.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="7bd2c-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="7bd2c-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="7bd2c-116">A várólistán lévő elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="7bd2c-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="7bd2c-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="7bd2c-118">A várólistához megadott kulcsértékkel újra létrehozza az elsődleges vagy másodlagos kapcsolati karakterláncokat.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="7bd2c-119">5. példa</span><span class="sxs-lookup"><span data-stu-id="7bd2c-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="7bd2c-120">A témakör elsődleges vagy másodlagos kapcsolati karakterláncának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="7bd2c-121">6. példa</span><span class="sxs-lookup"><span data-stu-id="7bd2c-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="7bd2c-122">A témakör kulcsértékével újra létrehozza az elsődleges vagy másodlagos kapcsolati karakterláncokat.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="7bd2c-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bd2c-123">PARAMETERS</span></span>

### <span data-ttu-id="7bd2c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd2c-124">-DefaultProfile</span></span>
<span data-ttu-id="7bd2c-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bd2c-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="7bd2c-126">-KeyValue</span></span>
<span data-ttu-id="7bd2c-127">Egy 256 bites, base64 kódolású kulcs az SAS-jogkivonat aláírásához és érvényességének igazolásához.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="7bd2c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="7bd2c-128">-Name</span></span>
<span data-ttu-id="7bd2c-129">AuthorizationRule Name (EngedélyezésiSzabály neve) stb.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="7bd2c-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7bd2c-130">-Namespace</span></span>
<span data-ttu-id="7bd2c-131">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="7bd2c-131">Namespace Name</span></span>

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

### <span data-ttu-id="7bd2c-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="7bd2c-132">-Queue</span></span>
<span data-ttu-id="7bd2c-133">Várólistán lévő név</span><span class="sxs-lookup"><span data-stu-id="7bd2c-133">Queue Name</span></span>

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

### <span data-ttu-id="7bd2c-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="7bd2c-134">-RegenerateKey</span></span>
<span data-ttu-id="7bd2c-135">A kulcsok újragenerálása – 'PrimaryKey'/'SecondaryKey'.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="7bd2c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd2c-136">-ResourceGroupName</span></span>
<span data-ttu-id="7bd2c-137">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7bd2c-137">Resource Group Name</span></span>

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

### <span data-ttu-id="7bd2c-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="7bd2c-138">-Topic</span></span>
<span data-ttu-id="7bd2c-139">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="7bd2c-139">Topic Name</span></span>

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

### <span data-ttu-id="7bd2c-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bd2c-140">-Confirm</span></span>
<span data-ttu-id="7bd2c-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bd2c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bd2c-142">-WhatIf</span></span>
<span data-ttu-id="7bd2c-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bd2c-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bd2c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd2c-145">CommonParameters</span></span>
<span data-ttu-id="7bd2c-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bd2c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd2c-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bd2c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd2c-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bd2c-148">INPUTS</span></span>

### <span data-ttu-id="7bd2c-149">System.String</span><span class="sxs-lookup"><span data-stu-id="7bd2c-149">System.String</span></span>

## <span data-ttu-id="7bd2c-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7bd2c-150">OUTPUTS</span></span>

### <span data-ttu-id="7bd2c-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="7bd2c-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="7bd2c-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7bd2c-152">NOTES</span></span>

## <span data-ttu-id="7bd2c-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7bd2c-153">RELATED LINKS</span></span>
