---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 28abf3ff725f5a1b124f99c96b46d03458b42f8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493368"
---
# <span data-ttu-id="6fe78-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="6fe78-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="6fe78-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6fe78-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe78-103">Az elsődleges és a másodlagos kapcsolat karakterláncát adja meg a megadott névtérhez, illetve a várólistához vagy a témakörhöz.</span><span class="sxs-lookup"><span data-stu-id="6fe78-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fe78-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6fe78-104">SYNTAX</span></span>

### <span data-ttu-id="6fe78-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6fe78-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fe78-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6fe78-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fe78-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6fe78-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fe78-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6fe78-108">DESCRIPTION</span></span>
<span data-ttu-id="6fe78-109">A **Get-AzureRmServiceBusKey** parancsmag a megadott névtér vagy várólista elsődleges és másodlagos kapcsolati karakterláncait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="6fe78-109">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span> 

## <span data-ttu-id="6fe78-110">Példák</span><span class="sxs-lookup"><span data-stu-id="6fe78-110">EXAMPLES</span></span>

### <span data-ttu-id="6fe78-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="6fe78-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="6fe78-112">Az elsődleges és másodlagos kapcsolat karakterlánca a megadott névtérhez</span><span class="sxs-lookup"><span data-stu-id="6fe78-112">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="6fe78-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="6fe78-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="6fe78-114">Az elsődleges és a másodlagos kapcsolat karakterlánca a megadott várólistához.</span><span class="sxs-lookup"><span data-stu-id="6fe78-114">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="6fe78-115">3. példa</span><span class="sxs-lookup"><span data-stu-id="6fe78-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="6fe78-116">A megadott témakör elsődleges és másodlagos kapcsolati karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="6fe78-116">Primary and secondary connection string to the specified topic.</span></span>

## <span data-ttu-id="6fe78-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6fe78-117">PARAMETERS</span></span>

### <span data-ttu-id="6fe78-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6fe78-118">-Name</span></span>
<span data-ttu-id="6fe78-119">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="6fe78-119">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="6fe78-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6fe78-120">-Namespace</span></span>
<span data-ttu-id="6fe78-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="6fe78-121">Namespace Name.</span></span>

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

### <span data-ttu-id="6fe78-122">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="6fe78-122">-Queue</span></span>
<span data-ttu-id="6fe78-123">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="6fe78-123">Queue Name.</span></span>

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

### <span data-ttu-id="6fe78-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe78-124">-ResourceGroupName</span></span>
<span data-ttu-id="6fe78-125">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="6fe78-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="6fe78-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="6fe78-126">-Topic</span></span>
<span data-ttu-id="6fe78-127">A téma neve</span><span class="sxs-lookup"><span data-stu-id="6fe78-127">Topic Name.</span></span>

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

### <span data-ttu-id="6fe78-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe78-128">-DefaultProfile</span></span>
<span data-ttu-id="6fe78-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6fe78-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fe78-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe78-130">CommonParameters</span></span>
<span data-ttu-id="6fe78-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6fe78-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe78-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fe78-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe78-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fe78-133">INPUTS</span></span>

### <span data-ttu-id="6fe78-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6fe78-134">System.String</span></span>

## <span data-ttu-id="6fe78-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6fe78-135">OUTPUTS</span></span>

### <span data-ttu-id="6fe78-136">Microsoft. Azure. Command. ServiceBus. models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="6fe78-136">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="6fe78-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6fe78-137">NOTES</span></span>

## <span data-ttu-id="6fe78-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6fe78-138">RELATED LINKS</span></span>

