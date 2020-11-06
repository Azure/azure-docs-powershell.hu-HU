---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3bd06ea2534298ba81cd546e8fa6e8de02fa5928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505011"
---
# <span data-ttu-id="d627a-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="d627a-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="d627a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d627a-102">SYNOPSIS</span></span>
<span data-ttu-id="d627a-103">Új elsődleges vagy másodlagos kulcs létrehozása a megadott esemény-hubok engedélyezési szabályához.</span><span class="sxs-lookup"><span data-stu-id="d627a-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d627a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d627a-104">SYNTAX</span></span>

### <span data-ttu-id="d627a-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d627a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> -Namespace <String> -Name <String> -RegenerateKey <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d627a-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d627a-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> [-Namespace <String>] -EventHub <String> -Name <String>
 -RegenerateKey <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d627a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d627a-107">DESCRIPTION</span></span>
<span data-ttu-id="d627a-108">Az New-AzureRmEventHubKey parancsmag újragenerálja az elsődleges vagy másodlagos biztonsági társítási kulcsot a megadott esemény-hubok engedélyezési szabályához.</span><span class="sxs-lookup"><span data-stu-id="d627a-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="d627a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d627a-109">EXAMPLES</span></span>

### <span data-ttu-id="d627a-110">Példa 1,1</span><span class="sxs-lookup"><span data-stu-id="d627a-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="d627a-111">Újragenerálja az elsődleges kulcsot az engedélyezési szabály \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="d627a-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="d627a-112">Példa 1,2</span><span class="sxs-lookup"><span data-stu-id="d627a-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="d627a-113">Újragenerálja az elsődleges kulcsot az engedélyezési szabály \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="d627a-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="d627a-114">Példa 2,1</span><span class="sxs-lookup"><span data-stu-id="d627a-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="d627a-115">Példa 2,2</span><span class="sxs-lookup"><span data-stu-id="d627a-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="d627a-116">Újragenerálja az engedélyezési szabály MyAuthRuleName másodlagos kulcsát \` \` .</span><span class="sxs-lookup"><span data-stu-id="d627a-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="d627a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d627a-117">PARAMETERS</span></span>

### <span data-ttu-id="d627a-118">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="d627a-118">-RegenerateKey</span></span>
<span data-ttu-id="d627a-119">Kulcs a regenerálódni: \` PrimaryKey \` vagy \` SecondaryKey \` .</span><span class="sxs-lookup"><span data-stu-id="d627a-119">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d627a-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d627a-120">-Confirm</span></span>
<span data-ttu-id="d627a-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d627a-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d627a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d627a-122">-WhatIf</span></span>
<span data-ttu-id="d627a-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d627a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d627a-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d627a-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d627a-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d627a-125">-EventHub</span></span>
<span data-ttu-id="d627a-126">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="d627a-126">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d627a-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d627a-127">-Name</span></span>
<span data-ttu-id="d627a-128">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="d627a-128">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d627a-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d627a-129">-Namespace</span></span>
<span data-ttu-id="d627a-130">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="d627a-130">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d627a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d627a-131">-ResourceGroupName</span></span>
<span data-ttu-id="d627a-132">Erőforráscsoporthoz tartozó név.</span><span class="sxs-lookup"><span data-stu-id="d627a-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="d627a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d627a-133">INPUTS</span></span>

### <span data-ttu-id="d627a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d627a-134">System.String</span></span>

## <span data-ttu-id="d627a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d627a-135">OUTPUTS</span></span>

### <span data-ttu-id="d627a-136">Microsoft. Azure. Command. EventHub. models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="d627a-136">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="d627a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d627a-137">NOTES</span></span>

## <span data-ttu-id="d627a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d627a-138">RELATED LINKS</span></span>

