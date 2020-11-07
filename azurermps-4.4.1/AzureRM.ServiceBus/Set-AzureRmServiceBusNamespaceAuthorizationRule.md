---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: a56f9b27e19868d22eed94fbcf7717fbe1c68b39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680226"
---
# <span data-ttu-id="f1db9-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f1db9-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="f1db9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f1db9-102">SYNOPSIS</span></span>
<span data-ttu-id="f1db9-103">Frissíti a megadott engedélyezési szabály leírását a megadott szolgáltatási busz névteréhez.</span><span class="sxs-lookup"><span data-stu-id="f1db9-103">Updates the specified authorization rule description for the given Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1db9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f1db9-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1db9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f1db9-105">DESCRIPTION</span></span>
<span data-ttu-id="f1db9-106">A **set-AzureRmServiceBusNamespaceAuthorizationRule** parancsmag a megadott szolgáltatási busz névtérben frissíti a megadott engedélyezési szabály leírását.</span><span class="sxs-lookup"><span data-stu-id="f1db9-106">The **Set-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace.</span></span>

## <span data-ttu-id="f1db9-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f1db9-107">EXAMPLES</span></span>

### <span data-ttu-id="f1db9-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f1db9-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="f1db9-109">Eltávolítja a **Manage** (névtér) engedélyezési szabályának hozzáférési jogát `AuthoRule1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="f1db9-109">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

## <span data-ttu-id="f1db9-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f1db9-110">PARAMETERS</span></span>

### <span data-ttu-id="f1db9-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f1db9-111">-ResourceGroup</span></span>
<span data-ttu-id="f1db9-112">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f1db9-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="f1db9-113">– Jogok</span><span class="sxs-lookup"><span data-stu-id="f1db9-113">-Rights</span></span>
<span data-ttu-id="f1db9-114">Tartalomvédelmi például @ ("Figyelj", "Küldés", "kezelés").</span><span class="sxs-lookup"><span data-stu-id="f1db9-114">Rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="f1db9-115">Kötelező, ha a **AuthruleObj** nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="f1db9-115">Required if **AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1db9-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f1db9-116">-Confirm</span></span>
<span data-ttu-id="f1db9-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f1db9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1db9-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1db9-118">-WhatIf</span></span>
<span data-ttu-id="f1db9-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f1db9-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1db9-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f1db9-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1db9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1db9-121">-DefaultProfile</span></span>
<span data-ttu-id="f1db9-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f1db9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1db9-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="f1db9-123">-InputObj</span></span>
<span data-ttu-id="f1db9-124">ServiceBus NameSpace AuthorizationRule objektum</span><span class="sxs-lookup"><span data-stu-id="f1db9-124">ServiceBus NameSpace AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1db9-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f1db9-125">-Name</span></span>
<span data-ttu-id="f1db9-126">AuthorizationRule neve – kötelező, ha a "AuthruleObj" nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="f1db9-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1db9-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f1db9-127">-Namespace</span></span>
<span data-ttu-id="f1db9-128">ServiceBus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="f1db9-128">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="f1db9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1db9-129">CommonParameters</span></span>
<span data-ttu-id="f1db9-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f1db9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1db9-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1db9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1db9-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1db9-132">INPUTS</span></span>

### <span data-ttu-id="f1db9-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f1db9-133">-ResourceGroup</span></span>
 <span data-ttu-id="f1db9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f1db9-134">System.String</span></span>

### <span data-ttu-id="f1db9-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f1db9-135">-NamespaceName</span></span>
 <span data-ttu-id="f1db9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f1db9-136">System.String</span></span>

### <span data-ttu-id="f1db9-137">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="f1db9-137">-AuthRuleObj</span></span>
 <span data-ttu-id="f1db9-138">Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f1db9-138">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f1db9-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f1db9-139">OUTPUTS</span></span>

### <span data-ttu-id="f1db9-140">Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f1db9-140">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="f1db9-141">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 típusa: Microsoft. ServiceBus/AuthorizationRules név: AuthoRule1 hely: Címkék: Rights: {figyelj, küldés}</span><span class="sxs-lookup"><span data-stu-id="f1db9-141">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="f1db9-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f1db9-142">NOTES</span></span>

## <span data-ttu-id="f1db9-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f1db9-143">RELATED LINKS</span></span>

