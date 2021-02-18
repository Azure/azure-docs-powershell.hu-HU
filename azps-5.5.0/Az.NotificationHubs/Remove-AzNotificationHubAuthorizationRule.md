---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: d908d9d12e917efca6901c08bc69d4888072b6ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206406"
---
# <span data-ttu-id="cfbbc-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cfbbc-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="cfbbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfbbc-102">SYNOPSIS</span></span>
<span data-ttu-id="cfbbc-103">Eltávolít egy engedélyezési szabályt egy értesítési központban.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="cfbbc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cfbbc-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfbbc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cfbbc-105">DESCRIPTION</span></span>
<span data-ttu-id="cfbbc-106">A **Remove-AzNotificationHubAuthorizationRule** parancsmag eltávolítja a Megosztott hozzáférés-aláírás (SAS) engedélyezési szabályt az értesítési központban.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="cfbbc-107">Az engedélyezési szabályok a különböző engedélyszintek alapján hivatkozások (URI-k) létrehozásával kezelik az értesítési központokhoz való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="cfbbc-108">A jogosultsági szintek az alábbiak egyike lehet:</span><span class="sxs-lookup"><span data-stu-id="cfbbc-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="cfbbc-109">Hallgatás</span><span class="sxs-lookup"><span data-stu-id="cfbbc-109">Listen</span></span>
- <span data-ttu-id="cfbbc-110">Küldés</span><span class="sxs-lookup"><span data-stu-id="cfbbc-110">Send</span></span>
- <span data-ttu-id="cfbbc-111">Az ügyfelek kezelése a megfelelő engedélyszint alapján az alábbi URI-k egyikére irányítja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="cfbbc-112">A Figyelás engedéllyel rendelkező ügyfél például az adott engedélyhez az URI-hoz irányítja.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="cfbbc-113">Az engedélyezési szabály eltávolításával a megfelelő felhasználói engedélyeket is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="cfbbc-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cfbbc-114">EXAMPLES</span></span>

### <span data-ttu-id="cfbbc-115">1. példa: Engedélyezési szabály eltávolítása az értesítési központból</span><span class="sxs-lookup"><span data-stu-id="cfbbc-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="cfbbc-116">Ez a parancs eltávolítja a ListenRule engedélyezési szabályt a ContosoExternalHub nevű értesítési központból.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="cfbbc-117">A parancs futtatásakor meg kell adnia a névteret és azt az erőforráscsoportot is, amelyhez a központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="cfbbc-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfbbc-118">PARAMETERS</span></span>

### <span data-ttu-id="cfbbc-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cfbbc-119">-AuthorizationRule</span></span>
<span data-ttu-id="cfbbc-120">Annak az SAS-hitelesítési szabálynak a nevét adja meg, amelyről ez a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cfbbc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfbbc-121">-DefaultProfile</span></span>
<span data-ttu-id="cfbbc-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cfbbc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfbbc-123">-Force</span><span class="sxs-lookup"><span data-stu-id="cfbbc-123">-Force</span></span>
<span data-ttu-id="cfbbc-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cfbbc-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cfbbc-125">-Namespace</span></span>
<span data-ttu-id="cfbbc-126">Azt a névteret adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="cfbbc-127">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="cfbbc-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="cfbbc-128">-NotificationHub</span></span>
<span data-ttu-id="cfbbc-129">Azt az értesítési központot adja meg, amelyhez az engedélyezési szabályok vannak hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="cfbbc-130">Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek, platformtól függetlenül.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="cfbbc-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cfbbc-131">-ResourceGroup</span></span>
<span data-ttu-id="cfbbc-132">Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="cfbbc-133">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="cfbbc-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfbbc-134">-Confirm</span></span>
<span data-ttu-id="cfbbc-135">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfbbc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfbbc-136">-WhatIf</span></span>
<span data-ttu-id="cfbbc-137">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfbbc-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfbbc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfbbc-139">CommonParameters</span></span>
<span data-ttu-id="cfbbc-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfbbc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfbbc-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfbbc-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfbbc-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cfbbc-142">INPUTS</span></span>

### <span data-ttu-id="cfbbc-143">System.String</span><span class="sxs-lookup"><span data-stu-id="cfbbc-143">System.String</span></span>

## <span data-ttu-id="cfbbc-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfbbc-144">OUTPUTS</span></span>

### <span data-ttu-id="cfbbc-145">System.Void</span><span class="sxs-lookup"><span data-stu-id="cfbbc-145">System.Void</span></span>

## <span data-ttu-id="cfbbc-146">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cfbbc-146">NOTES</span></span>

## <span data-ttu-id="cfbbc-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfbbc-147">RELATED LINKS</span></span>

[<span data-ttu-id="cfbbc-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cfbbc-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="cfbbc-149">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cfbbc-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="cfbbc-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cfbbc-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


