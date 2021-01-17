---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: d908d9d12e917efca6901c08bc69d4888072b6ef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385109"
---
# <span data-ttu-id="3bd14-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3bd14-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="3bd14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bd14-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd14-103">Eltávolít egy engedélyezési szabályt egy értesítési központban.</span><span class="sxs-lookup"><span data-stu-id="3bd14-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="3bd14-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3bd14-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bd14-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3bd14-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd14-106">A **Remove-AzNotificationHubAuthorizationRule** parancsmag eltávolítja a Megosztott hozzáférés-aláírás (SAS) engedélyezési szabályt az értesítési központban.</span><span class="sxs-lookup"><span data-stu-id="3bd14-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="3bd14-107">Az engedélyezési szabályok a különböző engedélyszintek alapján hivatkozások (URI-k) létrehozásával kezelik az értesítési központokhoz való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="3bd14-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="3bd14-108">A jogosultsági szintek az alábbiak egyike lehet:</span><span class="sxs-lookup"><span data-stu-id="3bd14-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="3bd14-109">Hallgatás</span><span class="sxs-lookup"><span data-stu-id="3bd14-109">Listen</span></span>
- <span data-ttu-id="3bd14-110">Küldés</span><span class="sxs-lookup"><span data-stu-id="3bd14-110">Send</span></span>
- <span data-ttu-id="3bd14-111">Az ügyfelek kezelése a megfelelő engedélyszint alapján az alábbi URI-k egyikéhez irányítja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="3bd14-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="3bd14-112">A Figyelás engedéllyel rendelkező ügyfél például az adott engedélyhez az URI-hoz irányítja.</span><span class="sxs-lookup"><span data-stu-id="3bd14-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="3bd14-113">Az engedélyezési szabály eltávolításával a megfelelő felhasználói engedélyeket is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="3bd14-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="3bd14-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3bd14-114">EXAMPLES</span></span>

### <span data-ttu-id="3bd14-115">1. példa: Engedélyezési szabály eltávolítása az értesítési központból</span><span class="sxs-lookup"><span data-stu-id="3bd14-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="3bd14-116">Ez a parancs eltávolítja a ListenRule engedélyezési szabályt a ContosoExternalHub nevű értesítési központból.</span><span class="sxs-lookup"><span data-stu-id="3bd14-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="3bd14-117">A parancs futtatásakor meg kell adnia a névteret és azt az erőforráscsoportot is, amelyhez a központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="3bd14-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="3bd14-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bd14-118">PARAMETERS</span></span>

### <span data-ttu-id="3bd14-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3bd14-119">-AuthorizationRule</span></span>
<span data-ttu-id="3bd14-120">A parancsmag által eltávolított SAS-hitelesítési szabály neve.</span><span class="sxs-lookup"><span data-stu-id="3bd14-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd14-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd14-121">-DefaultProfile</span></span>
<span data-ttu-id="3bd14-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3bd14-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3bd14-123">-Force</span><span class="sxs-lookup"><span data-stu-id="3bd14-123">-Force</span></span>
<span data-ttu-id="3bd14-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3bd14-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3bd14-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3bd14-125">-Namespace</span></span>
<span data-ttu-id="3bd14-126">Azt a névteret adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="3bd14-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="3bd14-127">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="3bd14-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="3bd14-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="3bd14-128">-NotificationHub</span></span>
<span data-ttu-id="3bd14-129">Azt az értesítési központot adja meg, amelyhez az engedélyezési szabályok vannak hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="3bd14-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="3bd14-130">Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek, platformtól függetlenül.</span><span class="sxs-lookup"><span data-stu-id="3bd14-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="3bd14-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3bd14-131">-ResourceGroup</span></span>
<span data-ttu-id="3bd14-132">Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="3bd14-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="3bd14-133">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="3bd14-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="3bd14-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3bd14-134">-Confirm</span></span>
<span data-ttu-id="3bd14-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="3bd14-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bd14-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd14-136">-WhatIf</span></span>
<span data-ttu-id="3bd14-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="3bd14-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3bd14-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3bd14-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bd14-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd14-139">CommonParameters</span></span>
<span data-ttu-id="3bd14-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bd14-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd14-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bd14-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd14-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3bd14-142">INPUTS</span></span>

### <span data-ttu-id="3bd14-143">System.String</span><span class="sxs-lookup"><span data-stu-id="3bd14-143">System.String</span></span>

## <span data-ttu-id="3bd14-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bd14-144">OUTPUTS</span></span>

### <span data-ttu-id="3bd14-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="3bd14-145">System.Void</span></span>

## <span data-ttu-id="3bd14-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3bd14-146">NOTES</span></span>

## <span data-ttu-id="3bd14-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bd14-147">RELATED LINKS</span></span>

[<span data-ttu-id="3bd14-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3bd14-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="3bd14-149">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3bd14-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="3bd14-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3bd14-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


