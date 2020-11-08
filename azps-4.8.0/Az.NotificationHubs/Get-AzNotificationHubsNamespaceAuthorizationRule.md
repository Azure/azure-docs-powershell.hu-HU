---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184757"
---
# <span data-ttu-id="ace0c-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ace0c-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="ace0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ace0c-102">SYNOPSIS</span></span>
<span data-ttu-id="ace0c-103">Információt kap az értesítési hub névteréhez társított engedélyezési szabályokról.</span><span class="sxs-lookup"><span data-stu-id="ace0c-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="ace0c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ace0c-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ace0c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ace0c-105">DESCRIPTION</span></span>
<span data-ttu-id="ace0c-106">A **Get-AzNotificationHubsNamespaceAuthorizationRule** parancsmag információt ad az értesítési hub névteréhez társított megosztott hozzáférés-aláírási szabályokról.</span><span class="sxs-lookup"><span data-stu-id="ace0c-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="ace0c-107">A névtérhez társított összes szabályról információt adhat vissza.</span><span class="sxs-lookup"><span data-stu-id="ace0c-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="ace0c-108">A másik lehetőség, hogy a *AuthorizationRule* paramétert is beleszámítva visszaadja az adott szabály adatait.</span><span class="sxs-lookup"><span data-stu-id="ace0c-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="ace0c-109">Engedélyezési szabályok: hozzáférés kezelése a névterekhez.</span><span class="sxs-lookup"><span data-stu-id="ace0c-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="ace0c-110">Ez a hivatkozás a különböző jogosultsági szintek alapján létrehozott URI-k létrehozásával végezhető el.</span><span class="sxs-lookup"><span data-stu-id="ace0c-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="ace0c-111">A platform szintjei az alábbiak lehetnek:</span><span class="sxs-lookup"><span data-stu-id="ace0c-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="ace0c-112">Hallgatni</span><span class="sxs-lookup"><span data-stu-id="ace0c-112">Listen</span></span>
- <span data-ttu-id="ace0c-113">Küldése</span><span class="sxs-lookup"><span data-stu-id="ace0c-113">Send</span></span>
- <span data-ttu-id="ace0c-114">Az ügyfelek kezelése a megfelelő jogosultsági szint alapján a fenti URI-k egyikéhez van irányítva.</span><span class="sxs-lookup"><span data-stu-id="ace0c-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="ace0c-115">A figyelési engedélyt tartalmazó ügyfél például az adott engedélyhez tartozó URI-azonosítóra fog irányulni.</span><span class="sxs-lookup"><span data-stu-id="ace0c-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="ace0c-116">Ez a parancsmag csak a névtérhez társított engedélyezési szabályokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ace0c-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="ace0c-117">Ha a névtérről szeretne információt kapni, használja a Get-AzNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="ace0c-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="ace0c-118">Példák</span><span class="sxs-lookup"><span data-stu-id="ace0c-118">EXAMPLES</span></span>

### <span data-ttu-id="ace0c-119">Példa 1: információk beszerzése a névterekhez rendelt összes engedélyezési szabályról</span><span class="sxs-lookup"><span data-stu-id="ace0c-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="ace0c-120">Ez a parancs a névtér ContosoNamespace és a ContosoNotificationsGroup erőforráscsoporthoz rendelt összes engedélyezési szabályról információt kap.</span><span class="sxs-lookup"><span data-stu-id="ace0c-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="ace0c-121">2. példa: az engedélyezési szabályokról szóló információk beszerzése</span><span class="sxs-lookup"><span data-stu-id="ace0c-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="ace0c-122">Ez a parancs a ListenRule nevű egyetlen névtér-engedélyezési szabályról kap információkat.</span><span class="sxs-lookup"><span data-stu-id="ace0c-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="ace0c-123">Ha egy adott engedélyezési szabályról szeretne információt kapni, akkor a névteret és az erőforráscsoportot is be kell írnia.</span><span class="sxs-lookup"><span data-stu-id="ace0c-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="ace0c-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ace0c-124">PARAMETERS</span></span>

### <span data-ttu-id="ace0c-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ace0c-125">-AuthorizationRule</span></span>
<span data-ttu-id="ace0c-126">A SAS-hitelesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ace0c-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="ace0c-127">Ezek a szabályok határozzák meg, hogy a felhasználók milyen típusú hozzáféréssel rendelkeznek a névtérhez.</span><span class="sxs-lookup"><span data-stu-id="ace0c-127">These rules determine the type of access that users have to the namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ace0c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ace0c-128">-DefaultProfile</span></span>
<span data-ttu-id="ace0c-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ace0c-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ace0c-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ace0c-130">-Namespace</span></span>
<span data-ttu-id="ace0c-131">Azt a névteret adja meg, amelyre az engedélyezési szabályok hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="ace0c-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="ace0c-132">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="ace0c-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="ace0c-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ace0c-133">-ResourceGroup</span></span>
<span data-ttu-id="ace0c-134">Azt az erőforráscsoport-csoportot adja meg, amelyhez az engedélyezési szabályokat hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="ace0c-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="ace0c-135">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="ace0c-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="ace0c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ace0c-136">CommonParameters</span></span>
<span data-ttu-id="ace0c-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ace0c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ace0c-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ace0c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ace0c-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ace0c-139">INPUTS</span></span>

### <span data-ttu-id="ace0c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ace0c-140">System.String</span></span>

## <span data-ttu-id="ace0c-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ace0c-141">OUTPUTS</span></span>

### <span data-ttu-id="ace0c-142">Microsoft. Azure. Command. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ace0c-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ace0c-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ace0c-143">NOTES</span></span>

## <span data-ttu-id="ace0c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ace0c-144">RELATED LINKS</span></span>

[<span data-ttu-id="ace0c-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ace0c-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="ace0c-146">Új – AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ace0c-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="ace0c-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ace0c-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="ace0c-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="ace0c-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)

