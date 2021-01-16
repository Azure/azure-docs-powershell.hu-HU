---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: c0c413918a986da4eaea8d9ef5f0f6a091b8b2e4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479653"
---
# <span data-ttu-id="c9695-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="c9695-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="c9695-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9695-102">SYNOPSIS</span></span>
<span data-ttu-id="c9695-103">A Szolgáltatásbusz névterében, illetve várólistában vagy témakörben található elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="c9695-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="c9695-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c9695-104">SYNTAX</span></span>

### <span data-ttu-id="c9695-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c9695-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9695-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9695-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9695-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c9695-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9695-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c9695-108">DESCRIPTION</span></span>
<span data-ttu-id="c9695-109">A **New-AzServiceBusKey** parancsmag új elsődleges vagy másodlagos kapcsolati karakterláncokat hoz létre a megadott névtérhez, várólistához vagy témakörhez és engedélyezési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="c9695-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="c9695-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c9695-110">EXAMPLES</span></span>

### <span data-ttu-id="c9695-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c9695-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="c9695-112">A névtér elsődleges vagy másodlagos kapcsolati karakterláncának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="c9695-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="c9695-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c9695-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="c9695-114">A névtérhez megadott kulcsértékkel újra létrehozza az elsődleges vagy másodlagos kapcsolati karakterláncokat.</span><span class="sxs-lookup"><span data-stu-id="c9695-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="c9695-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="c9695-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="c9695-116">A várólistán lévő elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="c9695-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="c9695-117">4. példa</span><span class="sxs-lookup"><span data-stu-id="c9695-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="c9695-118">A várólistához megadott kulcsértékkel újra létrehozza az elsődleges vagy másodlagos kapcsolati karakterláncokat.</span><span class="sxs-lookup"><span data-stu-id="c9695-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="c9695-119">5. példa</span><span class="sxs-lookup"><span data-stu-id="c9695-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="c9695-120">A témakör elsődleges vagy másodlagos kapcsolati karakterláncának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="c9695-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="c9695-121">6. példa</span><span class="sxs-lookup"><span data-stu-id="c9695-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="c9695-122">A témakör kulcsértékével újra létrehozza az elsődleges vagy másodlagos kapcsolati karakterláncokat.</span><span class="sxs-lookup"><span data-stu-id="c9695-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="c9695-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9695-123">PARAMETERS</span></span>

### <span data-ttu-id="c9695-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9695-124">-DefaultProfile</span></span>
<span data-ttu-id="c9695-125">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c9695-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9695-126">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="c9695-126">-KeyValue</span></span>
<span data-ttu-id="c9695-127">Egy 256 bites, base64 kódolású kulcs az SAS-jogkivonat aláírásához és érvényességének igazolásához.</span><span class="sxs-lookup"><span data-stu-id="c9695-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="c9695-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c9695-128">-Name</span></span>
<span data-ttu-id="c9695-129">AuthorizationRule Name (EngedélyezésiSzabály neve) stb.</span><span class="sxs-lookup"><span data-stu-id="c9695-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="c9695-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c9695-130">-Namespace</span></span>
<span data-ttu-id="c9695-131">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="c9695-131">Namespace Name</span></span>

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

### <span data-ttu-id="c9695-132">-Queue</span><span class="sxs-lookup"><span data-stu-id="c9695-132">-Queue</span></span>
<span data-ttu-id="c9695-133">Várólistán lévő név</span><span class="sxs-lookup"><span data-stu-id="c9695-133">Queue Name</span></span>

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

### <span data-ttu-id="c9695-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="c9695-134">-RegenerateKey</span></span>
<span data-ttu-id="c9695-135">A kulcsok újragenerálása – 'PrimaryKey'/'SecondaryKey'.</span><span class="sxs-lookup"><span data-stu-id="c9695-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="c9695-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9695-136">-ResourceGroupName</span></span>
<span data-ttu-id="c9695-137">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c9695-137">Resource Group Name</span></span>

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

### <span data-ttu-id="c9695-138">-Topic</span><span class="sxs-lookup"><span data-stu-id="c9695-138">-Topic</span></span>
<span data-ttu-id="c9695-139">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="c9695-139">Topic Name</span></span>

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

### <span data-ttu-id="c9695-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9695-140">-Confirm</span></span>
<span data-ttu-id="c9695-141">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="c9695-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9695-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9695-142">-WhatIf</span></span>
<span data-ttu-id="c9695-143">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="c9695-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9695-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c9695-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9695-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9695-145">CommonParameters</span></span>
<span data-ttu-id="c9695-146">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9695-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9695-147">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9695-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9695-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9695-148">INPUTS</span></span>

### <span data-ttu-id="c9695-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c9695-149">System.String</span></span>

## <span data-ttu-id="c9695-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c9695-150">OUTPUTS</span></span>

### <span data-ttu-id="c9695-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="c9695-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="c9695-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c9695-152">NOTES</span></span>

## <span data-ttu-id="c9695-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c9695-153">RELATED LINKS</span></span>
