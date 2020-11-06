---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 08f7f33138ddf9d5226cfc93f263fdec65de3388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494684"
---
# <span data-ttu-id="bce6d-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bce6d-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="bce6d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bce6d-102">SYNOPSIS</span></span>
<span data-ttu-id="bce6d-103">Egy, a megadott erőforráscsoport által létrehozott szolgáltatási busz névterének engedélyezési szabályát távolítja el.</span><span class="sxs-lookup"><span data-stu-id="bce6d-103">Removes the authorization rule of a Service Bus namespace from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bce6d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bce6d-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroupName <String> -Namespace <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bce6d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bce6d-105">DESCRIPTION</span></span>
<span data-ttu-id="bce6d-106">A **Remove-AzureRmServiceBusNamespaceAuthorizationRule** parancsmag eltávolítja a megadott erőforráscsoport szolgáltatási busz névterének engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="bce6d-106">The **Remove-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace for the specified resource group.</span></span>

## <span data-ttu-id="bce6d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bce6d-107">EXAMPLES</span></span>

### <span data-ttu-id="bce6d-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bce6d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="bce6d-109">Eltávolítja a `SBAuthoRule1` megadott erőforráscsoport névterének engedélyezési szabályát `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="bce6d-109">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

## <span data-ttu-id="bce6d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bce6d-110">PARAMETERS</span></span>

### <span data-ttu-id="bce6d-111">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bce6d-111">-Confirm</span></span>
<span data-ttu-id="bce6d-112">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bce6d-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bce6d-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bce6d-113">-WhatIf</span></span>
<span data-ttu-id="bce6d-114">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bce6d-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bce6d-115">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bce6d-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bce6d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce6d-116">-DefaultProfile</span></span>
<span data-ttu-id="bce6d-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bce6d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bce6d-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bce6d-118">-Name</span></span>
<span data-ttu-id="bce6d-119">A névtér AuthorizationRule neve.</span><span class="sxs-lookup"><span data-stu-id="bce6d-119">Namespace AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="bce6d-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bce6d-120">-Namespace</span></span>
<span data-ttu-id="bce6d-121">Névtér neve</span><span class="sxs-lookup"><span data-stu-id="bce6d-121">Namespace Name.</span></span>

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

### <span data-ttu-id="bce6d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bce6d-122">-ResourceGroupName</span></span>
<span data-ttu-id="bce6d-123">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="bce6d-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bce6d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce6d-124">CommonParameters</span></span>
<span data-ttu-id="bce6d-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bce6d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce6d-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bce6d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce6d-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bce6d-127">INPUTS</span></span>

### <span data-ttu-id="bce6d-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bce6d-128">-ResourceGroup</span></span>
 <span data-ttu-id="bce6d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bce6d-129">System.String</span></span>

### <span data-ttu-id="bce6d-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="bce6d-130">-NamespaceName</span></span>
 <span data-ttu-id="bce6d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="bce6d-131">System.String</span></span>

### <span data-ttu-id="bce6d-132">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="bce6d-132">-AuthorizationRuleName</span></span>
 <span data-ttu-id="bce6d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bce6d-133">System.String</span></span>

## <span data-ttu-id="bce6d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bce6d-134">OUTPUTS</span></span>

### <span data-ttu-id="bce6d-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bce6d-135">System.Boolean</span></span>

## <span data-ttu-id="bce6d-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bce6d-136">NOTES</span></span>

## <span data-ttu-id="bce6d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bce6d-137">RELATED LINKS</span></span>

