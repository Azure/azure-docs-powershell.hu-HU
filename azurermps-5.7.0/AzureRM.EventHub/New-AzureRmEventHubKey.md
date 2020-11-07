---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
ms.openlocfilehash: 8be39cb4b4b173d3b87efbf0b7ecea72ae233061
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673056"
---
# <span data-ttu-id="7606e-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="7606e-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="7606e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7606e-102">SYNOPSIS</span></span>
<span data-ttu-id="7606e-103">Új elsődleges vagy másodlagos kulcs létrehozása a megadott esemény-hubok engedélyezési szabályához.</span><span class="sxs-lookup"><span data-stu-id="7606e-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7606e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7606e-104">SYNTAX</span></span>

### <span data-ttu-id="7606e-105">NamespaceAuthorizationRuleSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7606e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7606e-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7606e-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7606e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7606e-107">DESCRIPTION</span></span>
<span data-ttu-id="7606e-108">Az New-AzureRmEventHubKey parancsmag újragenerálja az elsődleges vagy másodlagos biztonsági társítási kulcsot a megadott esemény-hubok engedélyezési szabályához.</span><span class="sxs-lookup"><span data-stu-id="7606e-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="7606e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7606e-109">EXAMPLES</span></span>

### <span data-ttu-id="7606e-110">Példa 1,1</span><span class="sxs-lookup"><span data-stu-id="7606e-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="7606e-111">Újragenerálja az elsődleges kulcsot az engedélyezési szabály \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="7606e-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="7606e-112">Példa 1,2</span><span class="sxs-lookup"><span data-stu-id="7606e-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="7606e-113">Újragenerálja az elsődleges kulcsot az engedélyezési szabály \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="7606e-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="7606e-114">Példa 2,1</span><span class="sxs-lookup"><span data-stu-id="7606e-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="7606e-115">Példa 2,2</span><span class="sxs-lookup"><span data-stu-id="7606e-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="7606e-116">Újragenerálja az engedélyezési szabály MyAuthRuleName másodlagos kulcsát \` \` .</span><span class="sxs-lookup"><span data-stu-id="7606e-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="7606e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7606e-117">PARAMETERS</span></span>

### <span data-ttu-id="7606e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7606e-118">-DefaultProfile</span></span>
<span data-ttu-id="7606e-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7606e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7606e-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="7606e-120">-EventHub</span></span>
<span data-ttu-id="7606e-121">EventHub neve</span><span class="sxs-lookup"><span data-stu-id="7606e-121">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7606e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7606e-122">-Name</span></span>
<span data-ttu-id="7606e-123">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="7606e-123">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7606e-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7606e-124">-Namespace</span></span>
<span data-ttu-id="7606e-125">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="7606e-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7606e-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="7606e-126">-RegenerateKey</span></span>
<span data-ttu-id="7606e-127">Kulcsok újragenerálása-"PrimaryKey"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="7606e-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7606e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7606e-128">-ResourceGroupName</span></span>
<span data-ttu-id="7606e-129">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="7606e-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7606e-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7606e-130">-Confirm</span></span>
<span data-ttu-id="7606e-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7606e-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7606e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7606e-132">-WhatIf</span></span>
<span data-ttu-id="7606e-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7606e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7606e-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7606e-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7606e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7606e-135">CommonParameters</span></span>
<span data-ttu-id="7606e-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7606e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7606e-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7606e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7606e-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7606e-138">INPUTS</span></span>

### <span data-ttu-id="7606e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7606e-139">System.String</span></span>


## <span data-ttu-id="7606e-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7606e-140">OUTPUTS</span></span>

### <span data-ttu-id="7606e-141">Microsoft. Azure. Command. EventHub. models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="7606e-141">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="7606e-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7606e-142">NOTES</span></span>

## <span data-ttu-id="7606e-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7606e-143">RELATED LINKS</span></span>
