---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: 7c85bafabede1c905efaf000721e5f8d6bee1572
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336270"
---
# <span data-ttu-id="8c61d-101">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8c61d-101">Get-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="8c61d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c61d-102">SYNOPSIS</span></span>
<span data-ttu-id="8c61d-103">Információkat kap az értesítési központhoz társított engedélyezési szabályokról.</span><span class="sxs-lookup"><span data-stu-id="8c61d-103">Gets information about the authorization rules associated with a notification hub.</span></span>

## <span data-ttu-id="8c61d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8c61d-104">SYNTAX</span></span>

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c61d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8c61d-105">DESCRIPTION</span></span>
<span data-ttu-id="8c61d-106">A **Get-AzNotificationHubAuthorizationRule** parancsmag információt kap az értesítési központhoz társított MEGOSZTOTT hozzáférés-aláírás (SAS) engedélyezési szabályairól.</span><span class="sxs-lookup"><span data-stu-id="8c61d-106">The **Get-AzNotificationHubAuthorizationRule** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="8c61d-107">A parancsmag információt ad a központhoz társított összes szabályról, vagy az *AuthorizationRule* paraméter megadva információkat kap egy adott szabályról.</span><span class="sxs-lookup"><span data-stu-id="8c61d-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="8c61d-108">Az engedélyezési szabályok kezelik az értesítési központokhoz való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="8c61d-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="8c61d-109">Az engedélyezési szabályok különböző engedélyszintek alapján hoznak létre hivatkozásokat URI-ként.</span><span class="sxs-lookup"><span data-stu-id="8c61d-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="8c61d-110">Az ügyfél a megfelelő jogosultsági szint alapján az alábbi URI-k egyikére irányítja az URI-ket.</span><span class="sxs-lookup"><span data-stu-id="8c61d-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="8c61d-111">A Figyelás engedéllyel rendelkező ügyfél például az adott engedélyhez az URI-hoz irányítja.</span><span class="sxs-lookup"><span data-stu-id="8c61d-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="8c61d-112">A **Get-AzNotificationHubAuthorizationRule** parancsmag csak az értesítési központhoz társított engedélyezési szabályokkal kapcsolatos információkat kap.</span><span class="sxs-lookup"><span data-stu-id="8c61d-112">The **Get-AzNotificationHubAuthorizationRule** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="8c61d-113">Ha információt kap a központról, használja a Get-AzNotificationHubot.</span><span class="sxs-lookup"><span data-stu-id="8c61d-113">To get information about the hub itself, use Get-AzNotificationHub.</span></span>

## <span data-ttu-id="8c61d-114">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8c61d-114">EXAMPLES</span></span>

### <span data-ttu-id="8c61d-115">1. példa: Információ kérése az értesítési központhoz rendelt összes engedélyezési szabályról</span><span class="sxs-lookup"><span data-stu-id="8c61d-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="8c61d-116">Ez a parancs információkat kap a ContosoNamespace névtéren található ContosoInternalHub értesítési központhoz rendelt összes engedélyezési szabályról.</span><span class="sxs-lookup"><span data-stu-id="8c61d-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="8c61d-117">Meg kell adnia azt a névteret, ahol a központ található, valamint azt az erőforráscsoportot, amelyhez a központ hozzá lett rendelve.</span><span class="sxs-lookup"><span data-stu-id="8c61d-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="8c61d-118">2. példa: Információ kérése egy értesítési központhoz rendelt engedélyezési szabályokkal kapcsolatban</span><span class="sxs-lookup"><span data-stu-id="8c61d-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="8c61d-119">Ez a parancs információkat kap a ContosoNamespace névtéren található ContosoInternalHub értesítési központhoz rendelt összes engedélyezési szabályról.</span><span class="sxs-lookup"><span data-stu-id="8c61d-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="8c61d-120">A parancs az *AuthorizationRule paraméterrel* korlátozza a visszaadott adatokat egyetlen, ListenRule nevű engedélyezési szabályra.</span><span class="sxs-lookup"><span data-stu-id="8c61d-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="8c61d-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c61d-121">PARAMETERS</span></span>

### <span data-ttu-id="8c61d-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8c61d-122">-AuthorizationRule</span></span>
<span data-ttu-id="8c61d-123">Egy SAS-hitelesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8c61d-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="8c61d-124">Ezek a szabályok határozzák meg, hogy a felhasználók milyen típusú hozzáféréssel férnek hozzá az értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="8c61d-124">These rules determine the type of access that users have to the notification hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c61d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c61d-125">-DefaultProfile</span></span>
<span data-ttu-id="8c61d-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8c61d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c61d-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8c61d-127">-Namespace</span></span>
<span data-ttu-id="8c61d-128">Azt a névteret adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="8c61d-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="8c61d-129">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="8c61d-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="8c61d-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="8c61d-130">-NotificationHub</span></span>
<span data-ttu-id="8c61d-131">Megadja azt az értesítési központot, amelyhez ez a parancsmag engedélyezési szabályokat rendel.</span><span class="sxs-lookup"><span data-stu-id="8c61d-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="8c61d-132">Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek attól függetlenül, hogy milyen platformon használják őket.</span><span class="sxs-lookup"><span data-stu-id="8c61d-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="8c61d-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c61d-133">-ResourceGroup</span></span>
<span data-ttu-id="8c61d-134">Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="8c61d-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="8c61d-135">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét megkönnyítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="8c61d-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="8c61d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c61d-136">CommonParameters</span></span>
<span data-ttu-id="8c61d-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c61d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c61d-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c61d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c61d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8c61d-139">INPUTS</span></span>

### <span data-ttu-id="8c61d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="8c61d-140">System.String</span></span>

## <span data-ttu-id="8c61d-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8c61d-141">OUTPUTS</span></span>

### <span data-ttu-id="8c61d-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8c61d-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8c61d-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8c61d-143">NOTES</span></span>

## <span data-ttu-id="8c61d-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8c61d-144">RELATED LINKS</span></span>

[<span data-ttu-id="8c61d-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8c61d-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="8c61d-146">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8c61d-146">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="8c61d-147">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8c61d-147">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="8c61d-148">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8c61d-148">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


