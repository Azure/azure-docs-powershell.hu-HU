---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubAuthorizationRule.md
ms.openlocfilehash: bb433499b53a1067e21996fe33fd6e9765dcab4e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669915"
---
# <span data-ttu-id="96e59-101">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="96e59-101">Get-AzNotificationHubAuthorizationRule</span></span>

## <span data-ttu-id="96e59-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="96e59-102">SYNOPSIS</span></span>
<span data-ttu-id="96e59-103">Információt kap az értesítési központtal társított engedélyezési szabályokról.</span><span class="sxs-lookup"><span data-stu-id="96e59-103">Gets information about the authorization rules associated with a notification hub.</span></span>

## <span data-ttu-id="96e59-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="96e59-104">SYNTAX</span></span>

```
Get-AzNotificationHubAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96e59-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="96e59-105">DESCRIPTION</span></span>
<span data-ttu-id="96e59-106">A **Get-AzNotificationHubAuthorizationRule** parancsmag információt kap az értesítési központhoz társított megosztott hozzáférés-aláírási engedélyekkel kapcsolatos szabályokról.</span><span class="sxs-lookup"><span data-stu-id="96e59-106">The **Get-AzNotificationHubAuthorizationRule** cmdlet gets information about the Shared Access Signature (SAS) authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="96e59-107">A parancsmag információt ad a hub-hoz társított összes szabályról, vagy a *AuthorizationRule* paraméterrel együtt az adott szabályra vonatkozó információkat.</span><span class="sxs-lookup"><span data-stu-id="96e59-107">The cmdlet returns information about all the rules associated with a hub or, by including the *AuthorizationRule* parameter, gets information about a specific rule.</span></span>
<span data-ttu-id="96e59-108">Engedélyezési szabályok: hozzáférés kezelése az értesítési hubokhoz.</span><span class="sxs-lookup"><span data-stu-id="96e59-108">Authorization rules manage access to your notification hubs.</span></span>
<span data-ttu-id="96e59-109">Egy engedélyezési szabály eltérő jogosultsági szinteken alapuló URI-ként hoz létre hivatkozásokat.</span><span class="sxs-lookup"><span data-stu-id="96e59-109">An authorization rule will create links, as a URI, based on different permission levels.</span></span>
<span data-ttu-id="96e59-110">Az ügyfelek a megfelelő jogosultsági szint alapján a megfelelő jogosultsági szint alapján kerülnek a megfelelő jogosultsági szinthez.</span><span class="sxs-lookup"><span data-stu-id="96e59-110">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="96e59-111">A figyelés engedéllyel rendelkező ügyfél például az adott engedélyhez tartozó URI-azonosítóra fog irányulni.</span><span class="sxs-lookup"><span data-stu-id="96e59-111">For instance, a client with the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="96e59-112">A **Get-AzNotificationHubAuthorizationRule** parancsmag csak az értesítési központtal társított engedélyezési szabályokról kap információkat.</span><span class="sxs-lookup"><span data-stu-id="96e59-112">The **Get-AzNotificationHubAuthorizationRule** cmdlet only gets information about the authorization rules associated with a notification hub.</span></span>
<span data-ttu-id="96e59-113">Ha a középpontról szeretne információt kapni, használja a Get-AzNotificationHub.</span><span class="sxs-lookup"><span data-stu-id="96e59-113">To get information about the hub itself, use Get-AzNotificationHub.</span></span>

## <span data-ttu-id="96e59-114">Példák</span><span class="sxs-lookup"><span data-stu-id="96e59-114">EXAMPLES</span></span>

### <span data-ttu-id="96e59-115">1. példa: információk kérése az értesítési központhoz rendelt összes engedélyezési szabályhoz</span><span class="sxs-lookup"><span data-stu-id="96e59-115">Example 1: Get information for all authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="96e59-116">Ez a parancs információt kap a ContosoInternalHub nevű értesítési központhoz rendelt összes engedélyezési szabályról a névtér ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="96e59-116">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="96e59-117">Meg kell adnia azt a névteret, ahol a hub található, valamint a hub által hozzárendelt erőforráscsoport.</span><span class="sxs-lookup"><span data-stu-id="96e59-117">You must specify the namespace where the hub is located as well as the resource group that the hub has been assigned to.</span></span>

### <span data-ttu-id="96e59-118">2. példa: információ kérése az értesítési központhoz rendelt engedélyezési szabályokról</span><span class="sxs-lookup"><span data-stu-id="96e59-118">Example 2: Get information for an authorization rules assigned to a notification hub</span></span>
```
PS C:\>Get-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="96e59-119">Ez a parancs információt kap a ContosoInternalHub nevű értesítési központhoz rendelt összes engedélyezési szabályról a névtér ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="96e59-119">This command gets information for all the authorization rules assigned to the notification hub named ContosoInternalHub in the namespace ContosoNamespace.</span></span>
<span data-ttu-id="96e59-120">A parancs a *AuthorizationRule* paraméter használatával korlátozza a visszaadott adatot egy ListenRule nevű egyetlen engedélyezési szabályra.</span><span class="sxs-lookup"><span data-stu-id="96e59-120">The command uses the *AuthorizationRule* parameter to limit the returned data to a single authorization rule named ListenRule.</span></span>

## <span data-ttu-id="96e59-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="96e59-121">PARAMETERS</span></span>

### <span data-ttu-id="96e59-122">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="96e59-122">-AuthorizationRule</span></span>
<span data-ttu-id="96e59-123">A SAS-hitelesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="96e59-123">Specifies the name of an SAS authentication rule.</span></span>
<span data-ttu-id="96e59-124">Ezek a szabályok határozzák meg, hogy milyen típusú hozzáférést kell biztosítani a felhasználóknak az értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="96e59-124">These rules determine the type of access that users have to the notification hub.</span></span>

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

### <span data-ttu-id="96e59-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e59-125">-DefaultProfile</span></span>
<span data-ttu-id="96e59-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="96e59-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96e59-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="96e59-127">-Namespace</span></span>
<span data-ttu-id="96e59-128">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="96e59-128">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="96e59-129">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="96e59-129">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="96e59-130">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="96e59-130">-NotificationHub</span></span>
<span data-ttu-id="96e59-131">Annak az értesítési csomópontnak a megadása, amelyhez a parancsmag engedélyezési szabályokat rendel.</span><span class="sxs-lookup"><span data-stu-id="96e59-131">Specifies the notification hub that this cmdlet assigns authorization rules.</span></span>
<span data-ttu-id="96e59-132">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="96e59-132">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="96e59-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="96e59-133">-ResourceGroup</span></span>
<span data-ttu-id="96e59-134">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="96e59-134">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="96e59-135">Az erőforráscsoportok a Készletkezelés és az Azure-felügyelet egyszerűsítését segítő módon rendezheti az elemeket, például a névtereket, az értesítési hubokat és a engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="96e59-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simplify inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="96e59-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e59-136">CommonParameters</span></span>
<span data-ttu-id="96e59-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="96e59-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e59-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96e59-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e59-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="96e59-139">INPUTS</span></span>

### <span data-ttu-id="96e59-140">System. String</span><span class="sxs-lookup"><span data-stu-id="96e59-140">System.String</span></span>

## <span data-ttu-id="96e59-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="96e59-141">OUTPUTS</span></span>

### <span data-ttu-id="96e59-142">Microsoft. Azure. Command. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="96e59-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="96e59-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="96e59-143">NOTES</span></span>

## <span data-ttu-id="96e59-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="96e59-144">RELATED LINKS</span></span>

[<span data-ttu-id="96e59-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="96e59-145">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[<span data-ttu-id="96e59-146">Új – AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="96e59-146">New-AzNotificationHubAuthorizationRule</span></span>](./New-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="96e59-147">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="96e59-147">Remove-AzNotificationHubAuthorizationRule</span></span>](./Remove-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="96e59-148">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="96e59-148">Set-AzNotificationHubAuthorizationRule</span></span>](./Set-AzNotificationHubAuthorizationRule.md)


