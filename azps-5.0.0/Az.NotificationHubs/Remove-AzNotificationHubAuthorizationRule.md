---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: d908d9d12e917efca6901c08bc69d4888072b6ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186041"
---
# <span data-ttu-id="b742c-101">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b742c-101">Remove-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="b742c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b742c-102">SYNOPSIS</span></span>
<span data-ttu-id="b742c-103">Egy engedélyezési szabály eltávolítása az értesítési központból.</span><span class="sxs-lookup"><span data-stu-id="b742c-103">Removes an authorization rule from a notification hub.</span></span>

## <span data-ttu-id="b742c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b742c-104">SYNTAX</span></span>

```
Remove-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b742c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b742c-105">DESCRIPTION</span></span>
<span data-ttu-id="b742c-106">A **Remove-AzNotificationHubAuthorizationRule** parancsmag egy értesítési központból távolítja el a megosztott hozzáférés-aláírások (SAS) engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="b742c-106">The **Remove-AzNotificationHubAuthorizationRule** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>
<span data-ttu-id="b742c-107">Engedélyezési szabályok: hozzáférést biztosít az értesítési hubokhoz, ha hivatkozásokat hoz létre a különböző jogosultsági szintek szerinti URI-ként.</span><span class="sxs-lookup"><span data-stu-id="b742c-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="b742c-108">A jogosultsági szint az alábbiak egyike lehet:</span><span class="sxs-lookup"><span data-stu-id="b742c-108">Permission levels can be one of the following:</span></span> 
- <span data-ttu-id="b742c-109">Hallgatni</span><span class="sxs-lookup"><span data-stu-id="b742c-109">Listen</span></span>
- <span data-ttu-id="b742c-110">Küldése</span><span class="sxs-lookup"><span data-stu-id="b742c-110">Send</span></span>
- <span data-ttu-id="b742c-111">Az ügyfelek kezelése a megfelelő jogosultsági szint alapján a fenti URI-k egyikéhez van irányítva.</span><span class="sxs-lookup"><span data-stu-id="b742c-111">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="b742c-112">A figyelési engedélyt tartalmazó ügyfél például az adott engedélyhez tartozó URI-azonosítóra fog irányulni.</span><span class="sxs-lookup"><span data-stu-id="b742c-112">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="b742c-113">Egy engedélyezési szabály eltávolítása a megfelelő felhasználói engedélyt is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="b742c-113">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="b742c-114">Példák</span><span class="sxs-lookup"><span data-stu-id="b742c-114">EXAMPLES</span></span>

### <span data-ttu-id="b742c-115">1. példa: engedélyezési szabály eltávolítása az értesítési központból</span><span class="sxs-lookup"><span data-stu-id="b742c-115">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="b742c-116">Ez a parancs eltávolítja a ListenRule nevű engedélyezési szabályt az ContosoExternalHub nevű értesítési központban.</span><span class="sxs-lookup"><span data-stu-id="b742c-116">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="b742c-117">A parancs futtatásakor meg kell adnia mind a névteret, mind annak az erőforráscsoport-csoportot, amelyhez a hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b742c-117">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="b742c-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b742c-118">PARAMETERS</span></span>

### <span data-ttu-id="b742c-119">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b742c-119">-AuthorizationRule</span></span>
<span data-ttu-id="b742c-120">Annak a SAS-hitelesítési szabálynak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="b742c-120">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b742c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b742c-121">-DefaultProfile</span></span>
<span data-ttu-id="b742c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b742c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b742c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="b742c-123">-Force</span></span>
<span data-ttu-id="b742c-124">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b742c-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b742c-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b742c-125">-Namespace</span></span>
<span data-ttu-id="b742c-126">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b742c-126">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="b742c-127">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="b742c-127">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="b742c-128">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="b742c-128">-NotificationHub</span></span>
<span data-ttu-id="b742c-129">Megadja az értesítési központot, amelyre az engedélyezési szabályok hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="b742c-129">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="b742c-130">Az értesítési hubok a platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="b742c-130">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="b742c-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b742c-131">-ResourceGroup</span></span>
<span data-ttu-id="b742c-132">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="b742c-132">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="b742c-133">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="b742c-133">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="b742c-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="b742c-134">-Confirm</span></span>
<span data-ttu-id="b742c-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="b742c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b742c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b742c-136">-WhatIf</span></span>
<span data-ttu-id="b742c-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="b742c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b742c-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b742c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b742c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b742c-139">CommonParameters</span></span>
<span data-ttu-id="b742c-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b742c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b742c-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b742c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b742c-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b742c-142">INPUTS</span></span>

### <span data-ttu-id="b742c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b742c-143">System.String</span></span>

## <span data-ttu-id="b742c-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b742c-144">OUTPUTS</span></span>

### <span data-ttu-id="b742c-145">System. Void</span><span class="sxs-lookup"><span data-stu-id="b742c-145">System.Void</span></span>

## <span data-ttu-id="b742c-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b742c-146">NOTES</span></span>

## <span data-ttu-id="b742c-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b742c-147">RELATED LINKS</span></span>

[<span data-ttu-id="b742c-148">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b742c-148">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="b742c-149">Új – AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b742c-149">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="b742c-150">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b742c-150">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)

