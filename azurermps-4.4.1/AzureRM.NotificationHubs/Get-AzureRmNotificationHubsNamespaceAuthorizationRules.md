---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: aa9b4dba29c766923966571c736c7f96a608df29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494785"
---
# <span data-ttu-id="d2a26-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="d2a26-101">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="d2a26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2a26-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a26-103">Információt kap az értesítési hub névteréhez társított engedélyezési szabályokról.</span><span class="sxs-lookup"><span data-stu-id="d2a26-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2a26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2a26-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2a26-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2a26-105">DESCRIPTION</span></span>
<span data-ttu-id="d2a26-106">A **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** parancsmag információt ad az értesítési hub névteréhez társított megosztott hozzáférés-aláírási szabályokról.</span><span class="sxs-lookup"><span data-stu-id="d2a26-106">The **Get-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="d2a26-107">A névtérhez társított összes szabályról információt adhat vissza.</span><span class="sxs-lookup"><span data-stu-id="d2a26-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="d2a26-108">A másik lehetőség, hogy a *AuthorizationRule* paramétert is beleszámítva visszaadja az adott szabály adatait.</span><span class="sxs-lookup"><span data-stu-id="d2a26-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>

<span data-ttu-id="d2a26-109">Engedélyezési szabályok: hozzáférés kezelése a névterekhez.</span><span class="sxs-lookup"><span data-stu-id="d2a26-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="d2a26-110">Ez a hivatkozás a különböző jogosultsági szintek alapján létrehozott URI-k létrehozásával végezhető el.</span><span class="sxs-lookup"><span data-stu-id="d2a26-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="d2a26-111">A platform szintjei az alábbiak lehetnek:</span><span class="sxs-lookup"><span data-stu-id="d2a26-111">Platform levels can be one of the following:</span></span> 

- <span data-ttu-id="d2a26-112">Hallgatni</span><span class="sxs-lookup"><span data-stu-id="d2a26-112">Listen</span></span>
- <span data-ttu-id="d2a26-113">Küldése</span><span class="sxs-lookup"><span data-stu-id="d2a26-113">Send</span></span>
- <span data-ttu-id="d2a26-114">Kezelése</span><span class="sxs-lookup"><span data-stu-id="d2a26-114">Manage</span></span>

<span data-ttu-id="d2a26-115">Az ügyfelek a megfelelő jogosultsági szint alapján a megfelelő jogosultsági szint alapján kerülnek a megfelelő jogosultsági szinthez.</span><span class="sxs-lookup"><span data-stu-id="d2a26-115">Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="d2a26-116">A figyelési engedélyt tartalmazó ügyfél például az adott engedélyhez tartozó URI-azonosítóra fog irányulni.</span><span class="sxs-lookup"><span data-stu-id="d2a26-116">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>

<span data-ttu-id="d2a26-117">Ez a parancsmag csak a névtérhez társított engedélyezési szabályokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d2a26-117">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="d2a26-118">Ha a névtérről szeretne információt kapni, használja a Get-AzureRmNotificationHubsNamespace.</span><span class="sxs-lookup"><span data-stu-id="d2a26-118">To get information about the namespace itself, use Get-AzureRmNotificationHubsNamespace.</span></span>

## <span data-ttu-id="d2a26-119">Példák</span><span class="sxs-lookup"><span data-stu-id="d2a26-119">EXAMPLES</span></span>

### <span data-ttu-id="d2a26-120">Példa 1: információk beszerzése a névterekhez rendelt összes engedélyezési szabályról</span><span class="sxs-lookup"><span data-stu-id="d2a26-120">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="d2a26-121">Ez a parancs a névtér ContosoNamespace és a ContosoNotificationsGroup erőforráscsoporthoz rendelt összes engedélyezési szabályról információt kap.</span><span class="sxs-lookup"><span data-stu-id="d2a26-121">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="d2a26-122">2. példa: az engedélyezési szabályokról szóló információk beszerzése</span><span class="sxs-lookup"><span data-stu-id="d2a26-122">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzureRmNotificationHubsNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="d2a26-123">Ez a parancs a ListenRule nevű egyetlen névtér-engedélyezési szabályról kap információkat.</span><span class="sxs-lookup"><span data-stu-id="d2a26-123">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="d2a26-124">Ha egy adott engedélyezési szabályról szeretne információt kapni, akkor a névteret és az erőforráscsoportot is be kell írnia.</span><span class="sxs-lookup"><span data-stu-id="d2a26-124">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="d2a26-125">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2a26-125">PARAMETERS</span></span>

### <span data-ttu-id="d2a26-126">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d2a26-126">-AuthorizationRule</span></span>
<span data-ttu-id="d2a26-127">A SAS-hitelesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2a26-127">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="d2a26-128">Ezek a szabályok határozzák meg, hogy a felhasználók milyen típusú hozzáféréssel rendelkeznek a névtérhez.</span><span class="sxs-lookup"><span data-stu-id="d2a26-128">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="d2a26-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d2a26-129">-Namespace</span></span>
<span data-ttu-id="d2a26-130">Azt a névteret adja meg, amelyre az engedélyezési szabályok hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="d2a26-130">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="d2a26-131">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="d2a26-131">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d2a26-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d2a26-132">-ResourceGroup</span></span>
<span data-ttu-id="d2a26-133">Azt az erőforráscsoport-csoportot adja meg, amelyhez az engedélyezési szabályokat hozzárendelték.</span><span class="sxs-lookup"><span data-stu-id="d2a26-133">Specifies the resource group to which the authorization rules are assigned.</span></span>

<span data-ttu-id="d2a26-134">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="d2a26-134">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d2a26-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a26-135">-DefaultProfile</span></span>
<span data-ttu-id="d2a26-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2a26-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2a26-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a26-137">CommonParameters</span></span>
<span data-ttu-id="d2a26-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2a26-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a26-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2a26-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a26-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2a26-140">INPUTS</span></span>

## <span data-ttu-id="d2a26-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2a26-141">OUTPUTS</span></span>

### <span data-ttu-id="d2a26-142">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes]</span><span class="sxs-lookup"><span data-stu-id="d2a26-142">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes]</span></span>

## <span data-ttu-id="d2a26-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2a26-143">NOTES</span></span>

## <span data-ttu-id="d2a26-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2a26-144">RELATED LINKS</span></span>

[<span data-ttu-id="d2a26-145">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d2a26-145">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="d2a26-146">Új – AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d2a26-146">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="d2a26-147">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d2a26-147">Remove-AzureRmNotificationHubsNamespace</span></span>](./Remove-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="d2a26-148">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="d2a26-148">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


