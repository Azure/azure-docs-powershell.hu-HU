---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 70b58b53b8e1ef88c59983b9da134a0fb935bcd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496860"
---
# <span data-ttu-id="f6f6d-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f6f6d-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="f6f6d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f6d-103">Egy adott névtérhez tartozó meghatározott engedélyezési szabály leírását kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f6d-103">Gets a description of the specified authorization rule for a given namespace.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6f6d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6f6d-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6f6d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6f6d-105">DESCRIPTION</span></span>
<span data-ttu-id="f6f6d-106">A **Get-AzureRmServiceBusNamespaceAuthorizationRule** parancsmag az adott névtérben a megadott engedélyezési szabály leírását kapja.</span><span class="sxs-lookup"><span data-stu-id="f6f6d-106">The **Get-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given namespace.</span></span>

## <span data-ttu-id="f6f6d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f6f6d-107">EXAMPLES</span></span>

### <span data-ttu-id="f6f6d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f6f6d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="f6f6d-109">Adott névtérhez megadott engedélyezési szabály leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6f6d-109">Returns the specified authorization rule description for a specified namespace.</span></span>

## <span data-ttu-id="f6f6d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6f6d-110">PARAMETERS</span></span>

### <span data-ttu-id="f6f6d-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f6f6d-111">-ResourceGroup</span></span>
<span data-ttu-id="f6f6d-112">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="f6f6d-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="f6f6d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f6d-113">-DefaultProfile</span></span>
<span data-ttu-id="f6f6d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6f6d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6f6d-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f6f6d-115">-Name</span></span>
<span data-ttu-id="f6f6d-116">ServiceBus-névtér AuthorizationRule neve</span><span class="sxs-lookup"><span data-stu-id="f6f6d-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f6f6d-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f6f6d-117">-Namespace</span></span>
<span data-ttu-id="f6f6d-118">ServiceBus-névtér neve</span><span class="sxs-lookup"><span data-stu-id="f6f6d-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="f6f6d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f6d-119">CommonParameters</span></span>
<span data-ttu-id="f6f6d-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6f6d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f6d-121">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6f6d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f6d-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6f6d-122">INPUTS</span></span>

### <span data-ttu-id="f6f6d-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f6f6d-123">-ResourceGroup</span></span>
 <span data-ttu-id="f6f6d-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f6f6d-124">System.String</span></span>
 

### <span data-ttu-id="f6f6d-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f6f6d-125">-NamespaceName</span></span>
 <span data-ttu-id="f6f6d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f6f6d-126">System.String</span></span>
 

### <span data-ttu-id="f6f6d-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f6f6d-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="f6f6d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f6f6d-128">System.String</span></span>

## <span data-ttu-id="f6f6d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6f6d-129">OUTPUTS</span></span>

### <span data-ttu-id="f6f6d-130">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Command. ServiceBus. models. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. ServiceBus, Version = 0.0.1.0, Culture = semleges, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f6f6d-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="f6f6d-131">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 típusa: Microsoft. ServiceBus/AuthorizationRules név: AuthoRule1 hely: Címkék: Rights: {figyelj, küldés}</span><span class="sxs-lookup"><span data-stu-id="f6f6d-131">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="f6f6d-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6f6d-132">NOTES</span></span>

## <span data-ttu-id="f6f6d-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6f6d-133">RELATED LINKS</span></span>

