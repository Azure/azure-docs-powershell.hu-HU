---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: 477884e676118f461578be500715fd3698957003
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386957"
---
# <span data-ttu-id="5c71d-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="5c71d-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="5c71d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c71d-102">SYNOPSIS</span></span>
<span data-ttu-id="5c71d-103">Létrehoz egy új elsődleges vagy másodlagos kulcsot a megadott Eseményközpontok engedélyezési szabályához.</span><span class="sxs-lookup"><span data-stu-id="5c71d-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="5c71d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5c71d-104">SYNTAX</span></span>

### <span data-ttu-id="5c71d-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5c71d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c71d-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c71d-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c71d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5c71d-107">DESCRIPTION</span></span>
<span data-ttu-id="5c71d-108">A New-AzEventHubKey parancsmag létrehozza a megadott Eseményközpontok engedélyezési szabályának elsődleges vagy másodlagos SAS-kulcsát.</span><span class="sxs-lookup"><span data-stu-id="5c71d-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="5c71d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5c71d-109">EXAMPLES</span></span>

### <span data-ttu-id="5c71d-110">1. példa: Namespace - AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="5c71d-110">Example 1: Namespace - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="5c71d-111">A MyAuthRuleName engedélyezési szabály elsődleges kulcsának újbóli \` \` létrehozása.</span><span class="sxs-lookup"><span data-stu-id="5c71d-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="5c71d-112">2. példa: EventHub – AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="5c71d-112">Example 2: EventHub - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="5c71d-113">A MyAuthRuleName engedélyezési szabály elsődleges kulcsának újbóli \` \` létrehozása.</span><span class="sxs-lookup"><span data-stu-id="5c71d-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="5c71d-114">3. példa: - Namespace - AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="5c71d-114">Example 3: - Namespace - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="5c71d-115">4. példa: EventHub – AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="5c71d-115">Example 4: EventHub - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="5c71d-116">A MyAuthRuleName engedélyezési szabály másodlagos kulcsának újbóli \` \` létrehozása.</span><span class="sxs-lookup"><span data-stu-id="5c71d-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="5c71d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c71d-117">PARAMETERS</span></span>

### <span data-ttu-id="5c71d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c71d-118">-DefaultProfile</span></span>
<span data-ttu-id="5c71d-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5c71d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c71d-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5c71d-120">-EventHub</span></span>
<span data-ttu-id="5c71d-121">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="5c71d-121">EventHub Name</span></span>

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

### <span data-ttu-id="5c71d-122">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="5c71d-122">-KeyValue</span></span>
<span data-ttu-id="5c71d-123">Egy 256 bites, base64 kódolású kulcs az SAS-jogkivonat aláírásához és érvényességének igazolásához.</span><span class="sxs-lookup"><span data-stu-id="5c71d-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="5c71d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5c71d-124">-Name</span></span>
<span data-ttu-id="5c71d-125">AuthorizationRule Name</span><span class="sxs-lookup"><span data-stu-id="5c71d-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="5c71d-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5c71d-126">-Namespace</span></span>
<span data-ttu-id="5c71d-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5c71d-127">Namespace Name</span></span>

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

### <span data-ttu-id="5c71d-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="5c71d-128">-RegenerateKey</span></span>
<span data-ttu-id="5c71d-129">A kulcsok újragenerálása – 'PrimaryKey'/'SecondaryKey'</span><span class="sxs-lookup"><span data-stu-id="5c71d-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

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

### <span data-ttu-id="5c71d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c71d-130">-ResourceGroupName</span></span>
<span data-ttu-id="5c71d-131">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="5c71d-131">Resource Group Name</span></span>

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

### <span data-ttu-id="5c71d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c71d-132">-Confirm</span></span>
<span data-ttu-id="5c71d-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5c71d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c71d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c71d-134">-WhatIf</span></span>
<span data-ttu-id="5c71d-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5c71d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c71d-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5c71d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c71d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c71d-137">CommonParameters</span></span>
<span data-ttu-id="5c71d-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c71d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c71d-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c71d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c71d-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c71d-140">INPUTS</span></span>

### <span data-ttu-id="5c71d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5c71d-141">System.String</span></span>

## <span data-ttu-id="5c71d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5c71d-142">OUTPUTS</span></span>

### <span data-ttu-id="5c71d-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="5c71d-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="5c71d-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5c71d-144">NOTES</span></span>

## <span data-ttu-id="5c71d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5c71d-145">RELATED LINKS</span></span>
