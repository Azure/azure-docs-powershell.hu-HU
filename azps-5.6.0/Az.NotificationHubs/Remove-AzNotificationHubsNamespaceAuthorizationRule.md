---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: 0b16a7feb2d0cba7355b6064c1a0e1e6fb327066
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918178"
---
# <span data-ttu-id="64694-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="64694-101">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="64694-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64694-102">SYNOPSIS</span></span>
<span data-ttu-id="64694-103">Eltávolít egy engedélyezési szabályt az értesítési központ névterében.</span><span class="sxs-lookup"><span data-stu-id="64694-103">Removes an authorization rule from a notification hub namespace.</span></span>

## <span data-ttu-id="64694-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="64694-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64694-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="64694-105">DESCRIPTION</span></span>
<span data-ttu-id="64694-106">A **Remove-AzNotificationHubsNamespaceAuthorizationRule parancsmag** eltávolítja a Megosztott hozzáférés-aláírás (SAS) engedélyezési szabályt az értesítési központ névterében.</span><span class="sxs-lookup"><span data-stu-id="64694-106">The **Remove-AzNotificationHubsNamespaceAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="64694-107">Az engedélyezési szabályok kezelik a névtérhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="64694-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="64694-108">Ezt különböző jogosultsági szinteken alapuló hivatkozások , például URI-k létrehozásával lehet tenni.</span><span class="sxs-lookup"><span data-stu-id="64694-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="64694-109">A jogosultsági szintek a következők:</span><span class="sxs-lookup"><span data-stu-id="64694-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="64694-110">Hallgatás</span><span class="sxs-lookup"><span data-stu-id="64694-110">Listen</span></span>
- <span data-ttu-id="64694-111">Küldés</span><span class="sxs-lookup"><span data-stu-id="64694-111">Send</span></span>
- <span data-ttu-id="64694-112">Az ügyfelek kezelése a megfelelő engedélyszint alapján az alábbi URI-k egyikéhez irányítja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="64694-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="64694-113">A Figyelás engedéllyel rendelkező ügyfél például az adott engedélyhez az URI-hoz irányítja.</span><span class="sxs-lookup"><span data-stu-id="64694-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="64694-114">Az engedélyezési szabály eltávolításával a megfelelő felhasználói engedélyeket is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="64694-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="64694-115">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="64694-115">EXAMPLES</span></span>

### <span data-ttu-id="64694-116">1. példa: Engedélyezési szabály eltávolítása a névtérből</span><span class="sxs-lookup"><span data-stu-id="64694-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzNotificationHubNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="64694-117">Ez a parancs eltávolítja a ListenRule nevű engedélyezési szabályt a ContosoNamespace nevű névtérből.</span><span class="sxs-lookup"><span data-stu-id="64694-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="64694-118">A parancs futtatásakor meg kell adnia azt az erőforráscsoportot, amelyhez a névtér hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="64694-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="64694-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64694-119">PARAMETERS</span></span>

### <span data-ttu-id="64694-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="64694-120">-AuthorizationRule</span></span>
<span data-ttu-id="64694-121">Az eltávolítható SAS-hitelesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="64694-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64694-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64694-122">-DefaultProfile</span></span>
<span data-ttu-id="64694-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="64694-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64694-124">-Force</span><span class="sxs-lookup"><span data-stu-id="64694-124">-Force</span></span>
<span data-ttu-id="64694-125">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="64694-125">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64694-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="64694-126">-Namespace</span></span>
<span data-ttu-id="64694-127">Megadja azt a névteret, amelyhez az engedélyezési szabályok hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="64694-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="64694-128">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="64694-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64694-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="64694-129">-ResourceGroup</span></span>
<span data-ttu-id="64694-130">Azt az erőforráscsoportot adja meg, amelyhez a névteret hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="64694-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="64694-131">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="64694-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="64694-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64694-132">-Confirm</span></span>
<span data-ttu-id="64694-133">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="64694-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64694-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64694-134">-WhatIf</span></span>
<span data-ttu-id="64694-135">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="64694-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="64694-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="64694-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64694-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64694-137">CommonParameters</span></span>
<span data-ttu-id="64694-138">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64694-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64694-139">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64694-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64694-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64694-140">INPUTS</span></span>

### <span data-ttu-id="64694-141">System.String</span><span class="sxs-lookup"><span data-stu-id="64694-141">System.String</span></span>

## <span data-ttu-id="64694-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64694-142">OUTPUTS</span></span>

### <span data-ttu-id="64694-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="64694-143">System.Boolean</span></span>

## <span data-ttu-id="64694-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="64694-144">NOTES</span></span>

## <span data-ttu-id="64694-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64694-145">RELATED LINKS</span></span>

[<span data-ttu-id="64694-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="64694-146">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="64694-147">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="64694-147">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./New-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="64694-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="64694-148">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Set-AzNotificationHubsNamespaceAuthorizationRule.md)


