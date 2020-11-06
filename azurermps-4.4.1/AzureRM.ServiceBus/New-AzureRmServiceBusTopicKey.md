---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: ed31934a75d9d6826a7e0464dccd43fd2d853daa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494685"
---
# <span data-ttu-id="a3384-101">New-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="a3384-101">New-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="a3384-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a3384-102">SYNOPSIS</span></span>
<span data-ttu-id="a3384-103">Az elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása a szolgáltatás busza témakörben.</span><span class="sxs-lookup"><span data-stu-id="a3384-103">Regenerates the primary or secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3384-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a3384-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3384-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a3384-105">DESCRIPTION</span></span>
<span data-ttu-id="a3384-106">A **New-AzureRmServiceBusTopicKey** parancsmag új elsődleges vagy másodlagos kapcsolati karakterláncot hoz létre a megadott buszjárati témakörhöz és engedélyezési szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="a3384-106">The **New-AzureRmServiceBusTopicKey** cmdlet generates a new primary or secondary connection string for the specified Service Bus topic and authorization rule.</span></span>

## <span data-ttu-id="a3384-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a3384-107">EXAMPLES</span></span>

### <span data-ttu-id="a3384-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a3384-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="a3384-109">Újragenerálja a névtér elsődleges kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="a3384-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="a3384-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="a3384-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="a3384-111">Újragenerálja a névtér másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="a3384-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="a3384-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a3384-112">PARAMETERS</span></span>

### <span data-ttu-id="a3384-113">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="a3384-113">-RegenerateKeys</span></span>
<span data-ttu-id="a3384-114">Itt adhatja meg, hogy az elsődleges vagy másodlagos kulcsokat szeretné-e újragenerálni.</span><span class="sxs-lookup"><span data-stu-id="a3384-114">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3384-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a3384-115">-ResourceGroup</span></span>
<span data-ttu-id="a3384-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="a3384-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="a3384-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a3384-117">-Confirm</span></span>
<span data-ttu-id="a3384-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a3384-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3384-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3384-119">-WhatIf</span></span>
<span data-ttu-id="a3384-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a3384-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3384-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a3384-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3384-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3384-122">-DefaultProfile</span></span>
<span data-ttu-id="a3384-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3384-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3384-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a3384-124">-Name</span></span>
<span data-ttu-id="a3384-125">Engedélyezési szabály neve.</span><span class="sxs-lookup"><span data-stu-id="a3384-125">Authorization Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3384-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a3384-126">-Namespace</span></span>
<span data-ttu-id="a3384-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="a3384-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3384-128">-Topic</span><span class="sxs-lookup"><span data-stu-id="a3384-128">-Topic</span></span>
<span data-ttu-id="a3384-129">A téma neve</span><span class="sxs-lookup"><span data-stu-id="a3384-129">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3384-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3384-130">CommonParameters</span></span>
<span data-ttu-id="a3384-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a3384-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3384-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3384-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3384-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3384-133">INPUTS</span></span>

### <span data-ttu-id="a3384-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a3384-134">-ResourceGroup</span></span>
 <span data-ttu-id="a3384-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a3384-135">System.String</span></span>
 

### <span data-ttu-id="a3384-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a3384-136">-NamespaceName</span></span>
 <span data-ttu-id="a3384-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a3384-137">System.String</span></span>
 

### <span data-ttu-id="a3384-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="a3384-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="a3384-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a3384-139">System.String</span></span>
 

### <span data-ttu-id="a3384-140">-TopicName</span><span class="sxs-lookup"><span data-stu-id="a3384-140">-TopicName</span></span>
 <span data-ttu-id="a3384-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a3384-141">System.String</span></span>
 

### <span data-ttu-id="a3384-142">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="a3384-142">-RegenerateKeys</span></span>
 <span data-ttu-id="a3384-143">System. String</span><span class="sxs-lookup"><span data-stu-id="a3384-143">System.String</span></span>

## <span data-ttu-id="a3384-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3384-144">OUTPUTS</span></span>

### <span data-ttu-id="a3384-145">Microsoft. Azure. Command. ServiceBus. models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="a3384-145">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="a3384-146">PrimaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-érték}; EntityPath = SB-Topi c_exampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.servicebus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-érték}; EntityPath = SB-Topi c_exampl1 PrimaryKey: {PrimaryKey Value} SecondaryKey: {SecondaryKey Value} kulcsnév: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="a3384-146">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="a3384-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a3384-147">NOTES</span></span>

## <span data-ttu-id="a3384-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3384-148">RELATED LINKS</span></span>

