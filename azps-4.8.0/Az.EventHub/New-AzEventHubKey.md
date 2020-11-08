---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: 477884e676118f461578be500715fd3698957003
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183587"
---
# <span data-ttu-id="693e5-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="693e5-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="693e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="693e5-102">SYNOPSIS</span></span>
<span data-ttu-id="693e5-103">Új elsődleges vagy másodlagos kulcs létrehozása a megadott esemény-hubok engedélyezési szabályához.</span><span class="sxs-lookup"><span data-stu-id="693e5-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="693e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="693e5-104">SYNTAX</span></span>

### <span data-ttu-id="693e5-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="693e5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="693e5-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="693e5-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="693e5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="693e5-107">DESCRIPTION</span></span>
<span data-ttu-id="693e5-108">Az New-AzEventHubKey parancsmag újragenerálja az elsődleges vagy másodlagos biztonsági társítási kulcsot a megadott esemény-hubok engedélyezési szabályához.</span><span class="sxs-lookup"><span data-stu-id="693e5-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="693e5-109">Példák</span><span class="sxs-lookup"><span data-stu-id="693e5-109">EXAMPLES</span></span>

### <span data-ttu-id="693e5-110">Példa 1: Namespace-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="693e5-110">Example 1: Namespace - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="693e5-111">Újragenerálja az elsődleges kulcsot az engedélyezési szabály \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="693e5-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="693e5-112">2. példa: EventHub-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="693e5-112">Example 2: EventHub - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="693e5-113">Újragenerálja az elsődleges kulcsot az engedélyezési szabály \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="693e5-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="693e5-114">Example 3:-Namespace-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="693e5-114">Example 3: - Namespace - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="693e5-115">Példa 4: EventHub-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="693e5-115">Example 4: EventHub - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="693e5-116">Újragenerálja az engedélyezési szabály MyAuthRuleName másodlagos kulcsát \` \` .</span><span class="sxs-lookup"><span data-stu-id="693e5-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="693e5-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="693e5-117">PARAMETERS</span></span>

### <span data-ttu-id="693e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="693e5-118">-DefaultProfile</span></span>
<span data-ttu-id="693e5-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="693e5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="693e5-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="693e5-120">-EventHub</span></span>
<span data-ttu-id="693e5-121">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="693e5-121">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="693e5-122">-Érték</span><span class="sxs-lookup"><span data-stu-id="693e5-122">-KeyValue</span></span>
<span data-ttu-id="693e5-123">Base64 kódolású 256 bites kulcs a SAS-token aláírásához és érvényesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="693e5-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="693e5-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="693e5-124">-Name</span></span>
<span data-ttu-id="693e5-125">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="693e5-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="693e5-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="693e5-126">-Namespace</span></span>
<span data-ttu-id="693e5-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="693e5-127">Namespace Name</span></span>

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

### <span data-ttu-id="693e5-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="693e5-128">-RegenerateKey</span></span>
<span data-ttu-id="693e5-129">Kulcsok újragenerálása-"PrimaryKey"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="693e5-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

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

### <span data-ttu-id="693e5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="693e5-130">-ResourceGroupName</span></span>
<span data-ttu-id="693e5-131">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="693e5-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="693e5-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="693e5-132">-Confirm</span></span>
<span data-ttu-id="693e5-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="693e5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="693e5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="693e5-134">-WhatIf</span></span>
<span data-ttu-id="693e5-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="693e5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="693e5-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="693e5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="693e5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="693e5-137">CommonParameters</span></span>
<span data-ttu-id="693e5-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="693e5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="693e5-139">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="693e5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="693e5-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="693e5-140">INPUTS</span></span>

### <span data-ttu-id="693e5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="693e5-141">System.String</span></span>

## <span data-ttu-id="693e5-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="693e5-142">OUTPUTS</span></span>

### <span data-ttu-id="693e5-143">Microsoft. Azure. Command. EventHub. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="693e5-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="693e5-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="693e5-144">NOTES</span></span>

## <span data-ttu-id="693e5-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="693e5-145">RELATED LINKS</span></span>
