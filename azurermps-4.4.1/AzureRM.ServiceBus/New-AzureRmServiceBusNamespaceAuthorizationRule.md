---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 6e20ceb2a6809e1e6010263563006468753cd41c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679938"
---
# <span data-ttu-id="9aa3c-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9aa3c-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="9aa3c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9aa3c-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa3c-103">Új engedélyezési szabály létrehozása a megadott szolgáltatási busz névteréhez</span><span class="sxs-lookup"><span data-stu-id="9aa3c-103">Creates a new authorization rule for the specified Service Bus namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9aa3c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9aa3c-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9aa3c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9aa3c-105">DESCRIPTION</span></span>
<span data-ttu-id="9aa3c-106">A **New-AzureRmServiceBusNamespaceAuthorizationRule** parancsmag új engedélyezési szabályt hoz létre a megadott szolgáltatási busz névteréhez.</span><span class="sxs-lookup"><span data-stu-id="9aa3c-106">The **New-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="9aa3c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9aa3c-107">EXAMPLES</span></span>

### <span data-ttu-id="9aa3c-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9aa3c-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="9aa3c-109">`AuthoRule1`A névtér **figyelési** és **küldési** jogosultságait hozza létre `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="9aa3c-109">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="9aa3c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9aa3c-110">PARAMETERS</span></span>

### <span data-ttu-id="9aa3c-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9aa3c-111">-ResourceGroup</span></span>
<span data-ttu-id="9aa3c-112">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9aa3c-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="9aa3c-113">– Jogok</span><span class="sxs-lookup"><span data-stu-id="9aa3c-113">-Rights</span></span>
<span data-ttu-id="9aa3c-114">A jogok; például @ ("Figyelj", "Küldés", "kezelés")</span><span class="sxs-lookup"><span data-stu-id="9aa3c-114">The Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa3c-115">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9aa3c-115">-Confirm</span></span>
<span data-ttu-id="9aa3c-116">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9aa3c-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa3c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aa3c-117">-WhatIf</span></span>
<span data-ttu-id="9aa3c-118">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9aa3c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9aa3c-119">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9aa3c-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa3c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa3c-120">-DefaultProfile</span></span>
<span data-ttu-id="9aa3c-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9aa3c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9aa3c-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9aa3c-122">-Name</span></span>
<span data-ttu-id="9aa3c-123">AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="9aa3c-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="9aa3c-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9aa3c-124">-Namespace</span></span>
<span data-ttu-id="9aa3c-125">ServiceBus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="9aa3c-125">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="9aa3c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa3c-126">CommonParameters</span></span>
<span data-ttu-id="9aa3c-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9aa3c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa3c-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aa3c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa3c-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9aa3c-129">INPUTS</span></span>

### <span data-ttu-id="9aa3c-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9aa3c-130">-ResourceGroup</span></span>
 <span data-ttu-id="9aa3c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9aa3c-131">System.String</span></span>
 

### <span data-ttu-id="9aa3c-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9aa3c-132">-NamespaceName</span></span>
 <span data-ttu-id="9aa3c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9aa3c-133">System.String</span></span>
 

### <span data-ttu-id="9aa3c-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="9aa3c-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="9aa3c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9aa3c-135">System.String</span></span>
 

### <span data-ttu-id="9aa3c-136">– Jogok</span><span class="sxs-lookup"><span data-stu-id="9aa3c-136">-Rights</span></span>
 <span data-ttu-id="9aa3c-137">System. string []</span><span class="sxs-lookup"><span data-stu-id="9aa3c-137">System.String []</span></span>

## <span data-ttu-id="9aa3c-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9aa3c-138">OUTPUTS</span></span>

### <span data-ttu-id="9aa3c-139">Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="9aa3c-139">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="9aa3c-140">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 típusa: Microsoft. ServiceBus/AuthorizationRules név: AuthoRule1 hely: Címkék: Rights: {figyelj, küldés}</span><span class="sxs-lookup"><span data-stu-id="9aa3c-140">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="9aa3c-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9aa3c-141">NOTES</span></span>

## <span data-ttu-id="9aa3c-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9aa3c-142">RELATED LINKS</span></span>

