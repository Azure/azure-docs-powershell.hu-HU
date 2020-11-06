---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 9ae94e039d91f8f21015fb28b726ef5bacfb4ae4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494432"
---
# <span data-ttu-id="520cf-101">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="520cf-101">Remove-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="520cf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="520cf-102">SYNOPSIS</span></span>
<span data-ttu-id="520cf-103">Egy engedélyezési szabály eltávolítása az értesítési központból.</span><span class="sxs-lookup"><span data-stu-id="520cf-103">Removes an authorization rule from a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="520cf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="520cf-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="520cf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="520cf-105">DESCRIPTION</span></span>
<span data-ttu-id="520cf-106">A **Remove-AzureRmNotificationHubAuthorizationRules** parancsmag egy értesítési központból távolítja el a megosztott hozzáférés-aláírások (SAS) engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="520cf-106">The **Remove-AzureRmNotificationHubAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>

<span data-ttu-id="520cf-107">Engedélyezési szabályok: hozzáférést biztosít az értesítési hubokhoz, ha hivatkozásokat hoz létre a különböző jogosultsági szintek szerinti URI-ként.</span><span class="sxs-lookup"><span data-stu-id="520cf-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="520cf-108">A jogosultsági szint az alábbiak egyike lehet:</span><span class="sxs-lookup"><span data-stu-id="520cf-108">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="520cf-109">Hallgatni</span><span class="sxs-lookup"><span data-stu-id="520cf-109">Listen</span></span>
- <span data-ttu-id="520cf-110">Küldése</span><span class="sxs-lookup"><span data-stu-id="520cf-110">Send</span></span>
- <span data-ttu-id="520cf-111">Kezelése</span><span class="sxs-lookup"><span data-stu-id="520cf-111">Manage</span></span>

<span data-ttu-id="520cf-112">Az ügyfelek a megfelelő jogosultsági szint alapján a megfelelő jogosultsági szint alapján kerülnek a megfelelő jogosultsági szinthez.</span><span class="sxs-lookup"><span data-stu-id="520cf-112">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="520cf-113">A figyelési engedélyt tartalmazó ügyfél például az adott engedélyhez tartozó URI-azonosítóra fog irányulni.</span><span class="sxs-lookup"><span data-stu-id="520cf-113">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="520cf-114">Egy engedélyezési szabály eltávolítása a megfelelő felhasználói engedélyt is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="520cf-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="520cf-115">Példák</span><span class="sxs-lookup"><span data-stu-id="520cf-115">EXAMPLES</span></span>

### <span data-ttu-id="520cf-116">1. példa: engedélyezési szabály eltávolítása az értesítési központból</span><span class="sxs-lookup"><span data-stu-id="520cf-116">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="520cf-117">Ez a parancs eltávolítja a ListenRule nevű engedélyezési szabályt az ContosoExternalHub nevű értesítési központban.</span><span class="sxs-lookup"><span data-stu-id="520cf-117">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="520cf-118">A parancs futtatásakor meg kell adnia mind a névteret, mind annak az erőforráscsoport-csoportot, amelyhez a hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="520cf-118">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="520cf-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="520cf-119">PARAMETERS</span></span>

### <span data-ttu-id="520cf-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="520cf-120">-AuthorizationRule</span></span>
<span data-ttu-id="520cf-121">Annak a SAS-hitelesítési szabálynak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="520cf-121">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="520cf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="520cf-122">-DefaultProfile</span></span>
<span data-ttu-id="520cf-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="520cf-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="520cf-124">-Force</span><span class="sxs-lookup"><span data-stu-id="520cf-124">-Force</span></span>
<span data-ttu-id="520cf-125">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="520cf-125">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520cf-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="520cf-126">-Namespace</span></span>
<span data-ttu-id="520cf-127">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="520cf-127">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="520cf-128">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="520cf-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="520cf-129">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="520cf-129">-NotificationHub</span></span>
<span data-ttu-id="520cf-130">Megadja az értesítési központot, amelyre az engedélyezési szabályok hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="520cf-130">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="520cf-131">Az értesítési hubok a platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="520cf-131">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="520cf-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="520cf-132">-ResourceGroup</span></span>
<span data-ttu-id="520cf-133">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="520cf-133">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="520cf-134">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="520cf-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="520cf-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="520cf-135">-Confirm</span></span>
<span data-ttu-id="520cf-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="520cf-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="520cf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="520cf-137">-WhatIf</span></span>
<span data-ttu-id="520cf-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="520cf-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="520cf-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="520cf-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="520cf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="520cf-140">CommonParameters</span></span>
<span data-ttu-id="520cf-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="520cf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="520cf-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="520cf-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="520cf-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="520cf-143">INPUTS</span></span>

### <span data-ttu-id="520cf-144">Nincs</span><span class="sxs-lookup"><span data-stu-id="520cf-144">None</span></span>
<span data-ttu-id="520cf-145">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="520cf-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="520cf-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="520cf-146">OUTPUTS</span></span>

## <span data-ttu-id="520cf-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="520cf-147">NOTES</span></span>

## <span data-ttu-id="520cf-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="520cf-148">RELATED LINKS</span></span>

[<span data-ttu-id="520cf-149">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="520cf-149">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="520cf-150">Új – AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="520cf-150">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="520cf-151">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="520cf-151">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


