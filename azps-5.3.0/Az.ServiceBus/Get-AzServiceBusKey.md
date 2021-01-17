---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: ffe220510f3046ea10b6374eb48c3c74730e4bc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479677"
---
# <span data-ttu-id="9b2da-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="9b2da-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="9b2da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b2da-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2da-103">A megadott Névtér, Várólista, Témakör vagy Alias (GeoDR-konfigurációk) elsődleges és másodlagos kapcsolati karakterláncának lekérte.</span><span class="sxs-lookup"><span data-stu-id="9b2da-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="9b2da-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9b2da-104">SYNTAX</span></span>

### <span data-ttu-id="9b2da-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9b2da-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2da-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9b2da-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2da-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="9b2da-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b2da-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="9b2da-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b2da-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9b2da-109">DESCRIPTION</span></span>
<span data-ttu-id="9b2da-110">A **Get-AzServiceBusKey** parancsmag visszaadja a megadott Névtér vagy Várólista, Témakör vagy Alias (GeoDR-konfigurációk) elsődleges és másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="9b2da-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="9b2da-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9b2da-111">EXAMPLES</span></span>

### <span data-ttu-id="9b2da-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="9b2da-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="9b2da-113">Elsődleges és másodlagos kapcsolati karakterlánc a megadott névtérhez.</span><span class="sxs-lookup"><span data-stu-id="9b2da-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="9b2da-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="9b2da-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="9b2da-115">Elsődleges és másodlagos kapcsolati karakterlánc a megadott várólistához.</span><span class="sxs-lookup"><span data-stu-id="9b2da-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="9b2da-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="9b2da-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="9b2da-117">A megadott témakörre vonatkozó elsődleges és másodlagos kapcsolati karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="9b2da-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="9b2da-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="9b2da-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="9b2da-119">Elsődleges és másodlagos kapcsolati karakterlánc a megadott névtérhez és aliashoz.</span><span class="sxs-lookup"><span data-stu-id="9b2da-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="9b2da-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b2da-120">PARAMETERS</span></span>

### <span data-ttu-id="9b2da-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="9b2da-121">-AliasName</span></span>
<span data-ttu-id="9b2da-122">Alias Name</span><span class="sxs-lookup"><span data-stu-id="9b2da-122">Alias Name</span></span>

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

### <span data-ttu-id="9b2da-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2da-123">-DefaultProfile</span></span>
<span data-ttu-id="9b2da-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9b2da-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b2da-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9b2da-125">-Name</span></span>
<span data-ttu-id="9b2da-126">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="9b2da-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="9b2da-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9b2da-127">-Namespace</span></span>
<span data-ttu-id="9b2da-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="9b2da-128">Namespace Name</span></span>

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

### <span data-ttu-id="9b2da-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="9b2da-129">-Queue</span></span>
<span data-ttu-id="9b2da-130">Várólistán lévő név</span><span class="sxs-lookup"><span data-stu-id="9b2da-130">Queue Name</span></span>

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

### <span data-ttu-id="9b2da-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b2da-131">-ResourceGroupName</span></span>
<span data-ttu-id="9b2da-132">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="9b2da-132">Resource Group Name</span></span>

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

### <span data-ttu-id="9b2da-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="9b2da-133">-Topic</span></span>
<span data-ttu-id="9b2da-134">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="9b2da-134">Topic Name</span></span>

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

### <span data-ttu-id="9b2da-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2da-135">CommonParameters</span></span>
<span data-ttu-id="9b2da-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b2da-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2da-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b2da-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2da-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b2da-138">INPUTS</span></span>

### <span data-ttu-id="9b2da-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9b2da-139">System.String</span></span>

## <span data-ttu-id="9b2da-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9b2da-140">OUTPUTS</span></span>

### <span data-ttu-id="9b2da-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="9b2da-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="9b2da-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9b2da-142">NOTES</span></span>

## <span data-ttu-id="9b2da-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9b2da-143">RELATED LINKS</span></span>
