---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
ms.openlocfilehash: 891e72945e3557ad1047b007504572a981449cd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679840"
---
# <span data-ttu-id="a5a8a-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="a5a8a-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="a5a8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a8a-103">Új elsődleges vagy másodlagos kulcs létrehozása a megadott esemény-hubok engedélyezési szabályához.</span><span class="sxs-lookup"><span data-stu-id="a5a8a-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5a8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5a8a-104">SYNTAX</span></span>

### <span data-ttu-id="a5a8a-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a5a8a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a8a-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a5a8a-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5a8a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5a8a-107">DESCRIPTION</span></span>
<span data-ttu-id="a5a8a-108">Az New-AzureRmEventHubKey parancsmag újragenerálja az elsődleges vagy másodlagos biztonsági társítási kulcsot a megadott esemény-hubok engedélyezési szabályához.</span><span class="sxs-lookup"><span data-stu-id="a5a8a-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="a5a8a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a5a8a-109">EXAMPLES</span></span>

### <span data-ttu-id="a5a8a-110">Példa 1,1-Namespace-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="a5a8a-110">Example 1.1 - Namespace - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="a5a8a-111">Újragenerálja az elsődleges kulcsot az engedélyezési szabály \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="a5a8a-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="a5a8a-112">Példa 1,2-EventHub-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="a5a8a-112">Example 1.2 - EventHub - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="a5a8a-113">Újragenerálja az elsődleges kulcsot az engedélyezési szabály \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="a5a8a-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="a5a8a-114">Példa 2,1-Namespace-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="a5a8a-114">Example 2.1  - Namespace - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="a5a8a-115">Példa 2,2-EventHub-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="a5a8a-115">Example 2.2 - EventHub - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="a5a8a-116">Újragenerálja az engedélyezési szabály MyAuthRuleName másodlagos kulcsát \` \` .</span><span class="sxs-lookup"><span data-stu-id="a5a8a-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="a5a8a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5a8a-117">PARAMETERS</span></span>

### <span data-ttu-id="a5a8a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a8a-118">-DefaultProfile</span></span>
<span data-ttu-id="a5a8a-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a5a8a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a8a-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="a5a8a-120">-EventHub</span></span>
<span data-ttu-id="a5a8a-121">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="a5a8a-121">EventHub Name</span></span>

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

### <span data-ttu-id="a5a8a-122">-Érték</span><span class="sxs-lookup"><span data-stu-id="a5a8a-122">-KeyValue</span></span>
<span data-ttu-id="a5a8a-123">Base64 kódolású 256 bites kulcs a SAS-token aláírásához és érvényesítéséhez.</span><span class="sxs-lookup"><span data-stu-id="a5a8a-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="a5a8a-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a5a8a-124">-Name</span></span>
<span data-ttu-id="a5a8a-125">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="a5a8a-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="a5a8a-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a5a8a-126">-Namespace</span></span>
<span data-ttu-id="a5a8a-127">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="a5a8a-127">Namespace Name</span></span>

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

### <span data-ttu-id="a5a8a-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="a5a8a-128">-RegenerateKey</span></span>
<span data-ttu-id="a5a8a-129">Kulcsok újragenerálása-"PrimaryKey"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="a5a8a-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

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

### <span data-ttu-id="a5a8a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a8a-130">-ResourceGroupName</span></span>
<span data-ttu-id="a5a8a-131">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a5a8a-131">Resource Group Name</span></span>

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

### <span data-ttu-id="a5a8a-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a5a8a-132">-Confirm</span></span>
<span data-ttu-id="a5a8a-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a5a8a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5a8a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a8a-134">-WhatIf</span></span>
<span data-ttu-id="a5a8a-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a5a8a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5a8a-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a5a8a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5a8a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a8a-137">CommonParameters</span></span>
<span data-ttu-id="a5a8a-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5a8a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a8a-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a8a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a8a-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5a8a-140">INPUTS</span></span>

### <span data-ttu-id="a5a8a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a5a8a-141">System.String</span></span>

## <span data-ttu-id="a5a8a-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5a8a-142">OUTPUTS</span></span>

### <span data-ttu-id="a5a8a-143">Microsoft. Azure. Command. EventHub. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="a5a8a-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="a5a8a-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5a8a-144">NOTES</span></span>

## <span data-ttu-id="a5a8a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5a8a-145">RELATED LINKS</span></span>
