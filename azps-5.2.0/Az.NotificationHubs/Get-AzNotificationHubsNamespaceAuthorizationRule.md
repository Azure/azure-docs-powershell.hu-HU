---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 08D03498-D18D-47FE-8916-702FA2E7D719
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: f3ba8428a6f6a9e618872e1292234751979b3c4b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336234"
---
# <span data-ttu-id="513ee-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="513ee-101">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="513ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="513ee-102">SYNOPSIS</span></span>
<span data-ttu-id="513ee-103">Információkat kap az értesítési központ névterére vonatkozó engedélyezési szabályokról.</span><span class="sxs-lookup"><span data-stu-id="513ee-103">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

## <span data-ttu-id="513ee-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="513ee-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="513ee-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="513ee-105">DESCRIPTION</span></span>
<span data-ttu-id="513ee-106">A **Get-AzNotificationHubsNamespaceAuthorizationRule** parancsmag egy értesítési központ névterére vonatkozó MEGOSZTOTT hozzáférés-aláírás (SAS) engedélyezési szabályokkal kapcsolatos információkat ad vissza.</span><span class="sxs-lookup"><span data-stu-id="513ee-106">The **Get-AzNotificationHubsNamespaceAuthorizationRule** cmdlet returns information about the Shared Access Signature (SAS) authorization rules associated with a notification hub namespace.</span></span>
<span data-ttu-id="513ee-107">A névtérhez társított összes szabályról információkat kaphat.</span><span class="sxs-lookup"><span data-stu-id="513ee-107">You can return information about all the rules associated with the namespace.</span></span>
<span data-ttu-id="513ee-108">Másik lehetőségként, az *AuthorizationRule* paraméter megadva adott szabály adatait is visszaadhatja.</span><span class="sxs-lookup"><span data-stu-id="513ee-108">Alternatively, and by including the *AuthorizationRule* parameter, you can return information for a specific rule.</span></span>
<span data-ttu-id="513ee-109">Az engedélyezési szabályok kezelik a névterekhez való hozzáférést.</span><span class="sxs-lookup"><span data-stu-id="513ee-109">Authorization rules manage access to namespaces.</span></span>
<span data-ttu-id="513ee-110">Ezt különböző jogosultsági szinteken alapuló hivatkozások , például URI-k létrehozásával lehet tenni.</span><span class="sxs-lookup"><span data-stu-id="513ee-110">This is done through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="513ee-111">A platformszintek az alábbiak egyike lehet:</span><span class="sxs-lookup"><span data-stu-id="513ee-111">Platform levels can be one of the following:</span></span> 
- <span data-ttu-id="513ee-112">Hallgatás</span><span class="sxs-lookup"><span data-stu-id="513ee-112">Listen</span></span>
- <span data-ttu-id="513ee-113">Küldés</span><span class="sxs-lookup"><span data-stu-id="513ee-113">Send</span></span>
- <span data-ttu-id="513ee-114">Az ügyfelek kezelése a megfelelő engedélyszint alapján az alábbi URI-k egyikéhez irányítja a rendszer.</span><span class="sxs-lookup"><span data-stu-id="513ee-114">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="513ee-115">A Figyelás engedéllyel rendelkező ügyfél például az adott engedélyhez az URI-hoz irányítja.</span><span class="sxs-lookup"><span data-stu-id="513ee-115">For instance, a client given the Listen permission will be directed to the URI for that permission.</span></span>
<span data-ttu-id="513ee-116">Ez a parancsmag csak a névtérhez társított engedélyezési szabályokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="513ee-116">This cmdlet only gets the authorization rules associated with a namespace.</span></span>
<span data-ttu-id="513ee-117">A névtérről a Get-AzNotificationHubsNamespace segítségével tud információt kapni.</span><span class="sxs-lookup"><span data-stu-id="513ee-117">To get information about the namespace itself, use Get-AzNotificationHubsNamespace.</span></span>

## <span data-ttu-id="513ee-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="513ee-118">EXAMPLES</span></span>

### <span data-ttu-id="513ee-119">1. példa: Információk kérése a névterekhez rendelt összes engedélyezési szabályról</span><span class="sxs-lookup"><span data-stu-id="513ee-119">Example 1: Get information about all authorization rules assigned to namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="513ee-120">Ez a parancs információkat kap a ContosoNamespace névtérhez és a ContosoNotificationsGroup erőforráscsoporthoz rendelt összes engedélyezési szabályról.</span><span class="sxs-lookup"><span data-stu-id="513ee-120">This command gets information about all the authorization rules assigned to both the namespace ContosoNamespace and the ContosoNotificationsGroup resource group.</span></span>

### <span data-ttu-id="513ee-121">2. példa: Információ kérése egy engedélyezési szabályról</span><span class="sxs-lookup"><span data-stu-id="513ee-121">Example 2: Get information about an authorization rule</span></span>
```
PS C:\>Get-AzNotificationHubsNamespaceAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="513ee-122">Ez a parancs információt kap a ListenRule nevű névtér-engedélyezési szabályról.</span><span class="sxs-lookup"><span data-stu-id="513ee-122">This command gets information about a single namespace authorization rule named ListenRule.</span></span>
<span data-ttu-id="513ee-123">A névteret és az erőforráscsoportot is meg kell jelennie, amikor információkat kap egy adott engedélyezési szabályról.</span><span class="sxs-lookup"><span data-stu-id="513ee-123">You must include the namespace and the resource group when you get information for a specific authorization rule.</span></span>

## <span data-ttu-id="513ee-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="513ee-124">PARAMETERS</span></span>

### <span data-ttu-id="513ee-125">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="513ee-125">-AuthorizationRule</span></span>
<span data-ttu-id="513ee-126">Egy SAS-hitelesítési szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="513ee-126">Specifies the name of a SAS authentication rule.</span></span>
<span data-ttu-id="513ee-127">Ezek a szabályok határozzák meg, hogy a felhasználóknak milyen típusú hozzáféréssel kell a névtérhez hozzáférniük.</span><span class="sxs-lookup"><span data-stu-id="513ee-127">These rules determine the type of access that users have to the namespace.</span></span>

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

### <span data-ttu-id="513ee-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513ee-128">-DefaultProfile</span></span>
<span data-ttu-id="513ee-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="513ee-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="513ee-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="513ee-130">-Namespace</span></span>
<span data-ttu-id="513ee-131">Megadja azt a névteret, amelyhez az engedélyezési szabályok hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="513ee-131">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="513ee-132">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="513ee-132">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="513ee-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="513ee-133">-ResourceGroup</span></span>
<span data-ttu-id="513ee-134">Azt az erőforráscsoportot adja meg, amelyhez az engedélyezési szabályok hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="513ee-134">Specifies the resource group to which the authorization rules are assigned.</span></span>
<span data-ttu-id="513ee-135">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="513ee-135">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="513ee-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513ee-136">CommonParameters</span></span>
<span data-ttu-id="513ee-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="513ee-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513ee-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="513ee-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513ee-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="513ee-139">INPUTS</span></span>

### <span data-ttu-id="513ee-140">System.String</span><span class="sxs-lookup"><span data-stu-id="513ee-140">System.String</span></span>

## <span data-ttu-id="513ee-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="513ee-141">OUTPUTS</span></span>

### <span data-ttu-id="513ee-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="513ee-142">Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="513ee-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="513ee-143">NOTES</span></span>

## <span data-ttu-id="513ee-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="513ee-144">RELATED LINKS</span></span>

[<span data-ttu-id="513ee-145">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="513ee-145">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="513ee-146">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="513ee-146">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="513ee-147">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="513ee-147">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="513ee-148">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="513ee-148">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


