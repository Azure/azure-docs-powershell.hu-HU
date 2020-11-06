---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 8434893dd3661bbfb1f78a4973dc206f44e9f400
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492734"
---
# <span data-ttu-id="52513-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="52513-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="52513-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="52513-102">SYNOPSIS</span></span>
<span data-ttu-id="52513-103">A megadott szolgáltatási busz névtérből eltávolítja a témakört.</span><span class="sxs-lookup"><span data-stu-id="52513-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52513-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="52513-104">SYNTAX</span></span>

### <span data-ttu-id="52513-105">TopicPropertiesSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="52513-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52513-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="52513-106">TopicInputObjectSet</span></span>
```
Remove-AzureRmServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52513-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="52513-107">TopicResourceIdSet</span></span>
```
Remove-AzureRmServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52513-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="52513-108">DESCRIPTION</span></span>
<span data-ttu-id="52513-109">A **Remove-AzureRmServiceBusTopic** parancsmag eltávolítja a témakört a megadott szolgáltatási busz névteréről.</span><span class="sxs-lookup"><span data-stu-id="52513-109">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="52513-110">Példák</span><span class="sxs-lookup"><span data-stu-id="52513-110">EXAMPLES</span></span>

### <span data-ttu-id="52513-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="52513-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="52513-112">Eltávolítja a témakört `SB-Topic_exampl1` a névtérből `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="52513-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="52513-113">Példa 2,1-InputObject – változó használata:</span><span class="sxs-lookup"><span data-stu-id="52513-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusTopic <parmas>
PS C:\> Remove-AzureRmServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="52513-114">Példa 2,2-InputObject:</span><span class="sxs-lookup"><span data-stu-id="52513-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic <parmas> | Remove-AzureRmServiceBusTopic
```

### <span data-ttu-id="52513-115">Példa 3,1-ResourceId változó használatával:</span><span class="sxs-lookup"><span data-stu-id="52513-115">Example 3.1 - ResourceId Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusTopic <params>
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="52513-116">Példa 3,2-ResourceId karakterlánc-érték használatával</span><span class="sxs-lookup"><span data-stu-id="52513-116">Example 3.2 - ResourceId Using String value</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="52513-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="52513-117">PARAMETERS</span></span>

### <span data-ttu-id="52513-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52513-118">-AsJob</span></span>
<span data-ttu-id="52513-119">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="52513-119">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52513-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52513-120">-DefaultProfile</span></span>
<span data-ttu-id="52513-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="52513-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52513-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52513-122">-InputObject</span></span>
<span data-ttu-id="52513-123">A szolgáltatás busz témakör objektuma</span><span class="sxs-lookup"><span data-stu-id="52513-123">Service Bus Topic Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52513-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="52513-124">-Name</span></span>
<span data-ttu-id="52513-125">Téma neve</span><span class="sxs-lookup"><span data-stu-id="52513-125">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52513-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="52513-126">-Namespace</span></span>
<span data-ttu-id="52513-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="52513-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52513-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52513-128">-PassThru</span></span>
<span data-ttu-id="52513-129">Ez a beállítás akkor igaz, ha a parancs sikeres.</span><span class="sxs-lookup"><span data-stu-id="52513-129">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52513-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52513-130">-ResourceGroupName</span></span>
<span data-ttu-id="52513-131">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="52513-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52513-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52513-132">-ResourceId</span></span>
<span data-ttu-id="52513-133">A szolgáltatás busz témakörének erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="52513-133">Service Bus Topic Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52513-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="52513-134">-Confirm</span></span>
<span data-ttu-id="52513-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="52513-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52513-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52513-136">-WhatIf</span></span>
<span data-ttu-id="52513-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="52513-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52513-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="52513-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52513-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52513-139">CommonParameters</span></span>
<span data-ttu-id="52513-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="52513-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52513-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52513-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52513-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="52513-142">INPUTS</span></span>

### <span data-ttu-id="52513-143">System. String</span><span class="sxs-lookup"><span data-stu-id="52513-143">System.String</span></span>

### <span data-ttu-id="52513-144">Microsoft. Azure. Command. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="52513-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="52513-145">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="52513-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="52513-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="52513-146">OUTPUTS</span></span>

### <span data-ttu-id="52513-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52513-147">System.Boolean</span></span>

## <span data-ttu-id="52513-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="52513-148">NOTES</span></span>

## <span data-ttu-id="52513-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="52513-149">RELATED LINKS</span></span>
