---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 96b95a4a6641e3bcfc2c1a18653da4231bee5c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492735"
---
# <span data-ttu-id="08e7c-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="08e7c-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="08e7c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="08e7c-103">Megkapja az elsődleges és a másodlagos kapcsolódási karakterláncot az adott névtérhez vagy a várólistához, illetve a témakörhöz vagy aliashoz (GeoDR-konfigurációk).</span><span class="sxs-lookup"><span data-stu-id="08e7c-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08e7c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08e7c-104">SYNTAX</span></span>

### <span data-ttu-id="08e7c-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="08e7c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08e7c-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="08e7c-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08e7c-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="08e7c-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08e7c-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="08e7c-108">AliasAuthoRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08e7c-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="08e7c-109">DESCRIPTION</span></span>
<span data-ttu-id="08e7c-110">A **Get-AzureRmServiceBusKey** parancsmag a megadott névtér vagy várólista (GeoDR-konfigurációk) elsődleges és másodlagos kapcsolati karakterláncát adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="08e7c-110">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="08e7c-111">Példák</span><span class="sxs-lookup"><span data-stu-id="08e7c-111">EXAMPLES</span></span>

### <span data-ttu-id="08e7c-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="08e7c-112">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="08e7c-113">Az elsődleges és másodlagos kapcsolat karakterlánca a megadott névtérhez</span><span class="sxs-lookup"><span data-stu-id="08e7c-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="08e7c-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="08e7c-114">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="08e7c-115">Az elsődleges és a másodlagos kapcsolat karakterlánca a megadott várólistához.</span><span class="sxs-lookup"><span data-stu-id="08e7c-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="08e7c-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="08e7c-116">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="08e7c-117">A megadott témakör elsődleges és másodlagos kapcsolati karakterlánca.</span><span class="sxs-lookup"><span data-stu-id="08e7c-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="08e7c-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="08e7c-118">Example 4</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="08e7c-119">Az elsődleges és másodlagos kapcsolat karakterlánca a megadott névtérhez és aliashoz.</span><span class="sxs-lookup"><span data-stu-id="08e7c-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="08e7c-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08e7c-120">PARAMETERS</span></span>

### <span data-ttu-id="08e7c-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="08e7c-121">-AliasName</span></span>
<span data-ttu-id="08e7c-122">Alias neve</span><span class="sxs-lookup"><span data-stu-id="08e7c-122">Alias Name</span></span>

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

### <span data-ttu-id="08e7c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e7c-123">-DefaultProfile</span></span>
<span data-ttu-id="08e7c-124">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08e7c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08e7c-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08e7c-125">-Name</span></span>
<span data-ttu-id="08e7c-126">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="08e7c-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="08e7c-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="08e7c-127">-Namespace</span></span>
<span data-ttu-id="08e7c-128">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="08e7c-128">Namespace Name</span></span>

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

### <span data-ttu-id="08e7c-129">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="08e7c-129">-Queue</span></span>
<span data-ttu-id="08e7c-130">Várólista neve</span><span class="sxs-lookup"><span data-stu-id="08e7c-130">Queue Name</span></span>

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

### <span data-ttu-id="08e7c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e7c-131">-ResourceGroupName</span></span>
<span data-ttu-id="08e7c-132">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="08e7c-132">Resource Group Name</span></span>

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

### <span data-ttu-id="08e7c-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="08e7c-133">-Topic</span></span>
<span data-ttu-id="08e7c-134">Téma neve</span><span class="sxs-lookup"><span data-stu-id="08e7c-134">Topic Name</span></span>

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

### <span data-ttu-id="08e7c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e7c-135">CommonParameters</span></span>
<span data-ttu-id="08e7c-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08e7c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e7c-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08e7c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e7c-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08e7c-138">INPUTS</span></span>

### <span data-ttu-id="08e7c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="08e7c-139">System.String</span></span>

## <span data-ttu-id="08e7c-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08e7c-140">OUTPUTS</span></span>

### <span data-ttu-id="08e7c-141">Microsoft. Azure. Command. ServiceBus. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="08e7c-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="08e7c-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08e7c-142">NOTES</span></span>

## <span data-ttu-id="08e7c-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08e7c-143">RELATED LINKS</span></span>
