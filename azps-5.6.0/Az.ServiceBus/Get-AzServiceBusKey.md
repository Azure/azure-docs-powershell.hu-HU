---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusKey.md
ms.openlocfilehash: 28ecd68167a7db2f41ee64a38a4616548707096c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932249"
---
# <span data-ttu-id="3eb7e-101">Get-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="3eb7e-101">Get-AzServiceBusKey</span></span>

## <span data-ttu-id="3eb7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eb7e-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb7e-103">A megadott Névtér, Várólista vagy Témakör vagy Alias (GeoDR-konfigurációk) elsődleges és másodlagos kapcsolati karakterláncát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="3eb7e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3eb7e-104">SYNTAX</span></span>

### <span data-ttu-id="3eb7e-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3eb7e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3eb7e-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3eb7e-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3eb7e-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="3eb7e-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3eb7e-108">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="3eb7e-108">AliasAuthoRuleSet</span></span>
```
Get-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3eb7e-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3eb7e-109">DESCRIPTION</span></span>
<span data-ttu-id="3eb7e-110">A **Get-AzServiceBusKey** parancsmag visszaadja a megadott Névtér vagy Várólista, Témakör vagy Alias (GeoDR-konfigurációk) elsődleges és másodlagos kapcsolati karakterláncát.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-110">The **Get-AzServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic or Alias (GeoDR Configurations).</span></span>

## <span data-ttu-id="3eb7e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3eb7e-111">EXAMPLES</span></span>

### <span data-ttu-id="3eb7e-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="3eb7e-112">Example 1</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="3eb7e-113">Elsődleges és másodlagos kapcsolati karakterlánc a megadott névtérhez.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-113">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="3eb7e-114">2. példa</span><span class="sxs-lookup"><span data-stu-id="3eb7e-114">Example 2</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="3eb7e-115">Elsődleges és másodlagos kapcsolati karakterlánc a megadott várólistához.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-115">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="3eb7e-116">3. példa</span><span class="sxs-lookup"><span data-stu-id="3eb7e-116">Example 3</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="3eb7e-117">A megadott témakörre vonatkozó elsődleges és másodlagos kapcsolati karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-117">Primary and secondary connection string to the specified topic.</span></span>

### <span data-ttu-id="3eb7e-118">4. példa</span><span class="sxs-lookup"><span data-stu-id="3eb7e-118">Example 4</span></span>
```
PS C:\> Get-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -AliasName SBAlias -Name AuthoRule1
```

<span data-ttu-id="3eb7e-119">Elsődleges és másodlagos kapcsolati karakterlánc a megadott névtérhez és aliashoz.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-119">Primary and secondary connection string to the specified namespace and alias.</span></span>

## <span data-ttu-id="3eb7e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3eb7e-120">PARAMETERS</span></span>

### <span data-ttu-id="3eb7e-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="3eb7e-121">-AliasName</span></span>
<span data-ttu-id="3eb7e-122">Alias Name</span><span class="sxs-lookup"><span data-stu-id="3eb7e-122">Alias Name</span></span>

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

### <span data-ttu-id="3eb7e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb7e-123">-DefaultProfile</span></span>
<span data-ttu-id="3eb7e-124">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3eb7e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3eb7e-125">-Name</span></span>
<span data-ttu-id="3eb7e-126">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="3eb7e-126">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="3eb7e-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3eb7e-127">-Namespace</span></span>
<span data-ttu-id="3eb7e-128">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="3eb7e-128">Namespace Name</span></span>

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

### <span data-ttu-id="3eb7e-129">-Queue</span><span class="sxs-lookup"><span data-stu-id="3eb7e-129">-Queue</span></span>
<span data-ttu-id="3eb7e-130">Várólistán lévő név</span><span class="sxs-lookup"><span data-stu-id="3eb7e-130">Queue Name</span></span>

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

### <span data-ttu-id="3eb7e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb7e-131">-ResourceGroupName</span></span>
<span data-ttu-id="3eb7e-132">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="3eb7e-132">Resource Group Name</span></span>

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

### <span data-ttu-id="3eb7e-133">-Topic</span><span class="sxs-lookup"><span data-stu-id="3eb7e-133">-Topic</span></span>
<span data-ttu-id="3eb7e-134">Témakör neve</span><span class="sxs-lookup"><span data-stu-id="3eb7e-134">Topic Name</span></span>

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

### <span data-ttu-id="3eb7e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb7e-135">CommonParameters</span></span>
<span data-ttu-id="3eb7e-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb7e-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb7e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb7e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3eb7e-138">INPUTS</span></span>

### <span data-ttu-id="3eb7e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3eb7e-139">System.String</span></span>

## <span data-ttu-id="3eb7e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3eb7e-140">OUTPUTS</span></span>

### <span data-ttu-id="3eb7e-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="3eb7e-141">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="3eb7e-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3eb7e-142">NOTES</span></span>

## <span data-ttu-id="3eb7e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3eb7e-143">RELATED LINKS</span></span>
