---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 715F8821-BBD1-440A-AD54-E960939E288A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: bb92344616c79db26b37bd9b18bdff7973946c24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494782"
---
# <span data-ttu-id="40fce-101">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="40fce-101">Remove-AzureRmNotificationHubAuthorizationRules</span></span>

## <span data-ttu-id="40fce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40fce-102">SYNOPSIS</span></span>
<span data-ttu-id="40fce-103">Egy engedélyezési szabály eltávolítása az értesítési központból.</span><span class="sxs-lookup"><span data-stu-id="40fce-103">Removes an authorization rule from a notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40fce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40fce-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40fce-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="40fce-105">DESCRIPTION</span></span>
<span data-ttu-id="40fce-106">A **Remove-AzureRmNotificationHubAuthorizationRules** parancsmag egy értesítési központból távolítja el a megosztott hozzáférés-aláírások (SAS) engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="40fce-106">The **Remove-AzureRmNotificationHubAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub.</span></span>

<span data-ttu-id="40fce-107">Engedélyezési szabályok: hozzáférést biztosít az értesítési hubokhoz, ha hivatkozásokat hoz létre a különböző jogosultsági szintek szerinti URI-ként.</span><span class="sxs-lookup"><span data-stu-id="40fce-107">Authorization rules manage access to your notification hubs through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="40fce-108">A jogosultsági szint az alábbiak egyike lehet:</span><span class="sxs-lookup"><span data-stu-id="40fce-108">Permission levels can be one of the following:</span></span> 

- <span data-ttu-id="40fce-109">Hallgatni</span><span class="sxs-lookup"><span data-stu-id="40fce-109">Listen</span></span>
- <span data-ttu-id="40fce-110">Küldése</span><span class="sxs-lookup"><span data-stu-id="40fce-110">Send</span></span>
- <span data-ttu-id="40fce-111">Kezelése</span><span class="sxs-lookup"><span data-stu-id="40fce-111">Manage</span></span>

<span data-ttu-id="40fce-112">Az ügyfelek a megfelelő jogosultsági szint alapján a megfelelő jogosultsági szint alapján kerülnek a megfelelő jogosultsági szinthez.</span><span class="sxs-lookup"><span data-stu-id="40fce-112">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="40fce-113">A figyelési engedélyt tartalmazó ügyfél például az adott engedélyhez tartozó URI-azonosítóra fog irányulni.</span><span class="sxs-lookup"><span data-stu-id="40fce-113">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="40fce-114">Egy engedélyezési szabály eltávolítása a megfelelő felhasználói engedélyt is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="40fce-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="40fce-115">Példák</span><span class="sxs-lookup"><span data-stu-id="40fce-115">EXAMPLES</span></span>

### <span data-ttu-id="40fce-116">1. példa: engedélyezési szabály eltávolítása az értesítési központból</span><span class="sxs-lookup"><span data-stu-id="40fce-116">Example 1: Remove an authorization rule from a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -NotificationHub "ContosoExternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="40fce-117">Ez a parancs eltávolítja a ListenRule nevű engedélyezési szabályt az ContosoExternalHub nevű értesítési központban.</span><span class="sxs-lookup"><span data-stu-id="40fce-117">This command removes the authorization rule named ListenRule from the notification hub named ContosoExternalHub.</span></span>
<span data-ttu-id="40fce-118">A parancs futtatásakor meg kell adnia mind a névteret, mind annak az erőforráscsoport-csoportot, amelyhez a hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="40fce-118">When you run this command you must specify both the namespace and the resource group that the hub is assigned to.</span></span>

## <span data-ttu-id="40fce-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40fce-119">PARAMETERS</span></span>

### <span data-ttu-id="40fce-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="40fce-120">-AuthorizationRule</span></span>
<span data-ttu-id="40fce-121">Annak a SAS-hitelesítési szabálynak a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="40fce-121">Specifies the name of the SAS authentication rule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="40fce-122">-Force</span><span class="sxs-lookup"><span data-stu-id="40fce-122">-Force</span></span>
<span data-ttu-id="40fce-123">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="40fce-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="40fce-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="40fce-124">-Namespace</span></span>
<span data-ttu-id="40fce-125">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="40fce-125">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="40fce-126">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="40fce-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="40fce-127">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="40fce-127">-NotificationHub</span></span>
<span data-ttu-id="40fce-128">Megadja az értesítési központot, amelyre az engedélyezési szabályok hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="40fce-128">Specifies the notification hub the authorization rules are assigned to.</span></span>
<span data-ttu-id="40fce-129">Az értesítési hubok a platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="40fce-129">Notification hubs are used to send push notifications to multiple clients regardless of the platform.</span></span>

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

### <span data-ttu-id="40fce-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="40fce-130">-ResourceGroup</span></span>
<span data-ttu-id="40fce-131">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="40fce-131">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="40fce-132">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="40fce-132">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="40fce-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="40fce-133">-Confirm</span></span>
<span data-ttu-id="40fce-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="40fce-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40fce-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40fce-135">-WhatIf</span></span>
<span data-ttu-id="40fce-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="40fce-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40fce-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40fce-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40fce-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40fce-138">-DefaultProfile</span></span>
<span data-ttu-id="40fce-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40fce-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40fce-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40fce-140">CommonParameters</span></span>
<span data-ttu-id="40fce-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40fce-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40fce-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40fce-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40fce-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40fce-143">INPUTS</span></span>

## <span data-ttu-id="40fce-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40fce-144">OUTPUTS</span></span>

## <span data-ttu-id="40fce-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40fce-145">NOTES</span></span>

## <span data-ttu-id="40fce-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40fce-146">RELATED LINKS</span></span>

[<span data-ttu-id="40fce-147">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="40fce-147">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="40fce-148">Új – AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="40fce-148">New-AzureRmNotificationHubAuthorizationRules</span></span>](./New-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="40fce-149">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="40fce-149">Set-AzureRmNotificationHubAuthorizationRules</span></span>](./Set-AzureRmNotificationHubAuthorizationRules.md)


