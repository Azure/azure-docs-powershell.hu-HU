---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 860AB403-3F99-45FA-8E6A-8C9872C121E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 192034e060b7162dcf04695d49a128d6a116bbcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500163"
---
# <span data-ttu-id="5ca46-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="5ca46-101">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>

## <span data-ttu-id="5ca46-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ca46-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca46-103">Az értesítési központ névterének engedélyezési szabályait távolítja el.</span><span class="sxs-lookup"><span data-stu-id="5ca46-103">Removes an authorization rule from a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ca46-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ca46-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ca46-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ca46-105">DESCRIPTION</span></span>
<span data-ttu-id="5ca46-106">A **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** parancsmag az értesítési hub-névtérből eltávolítja a megosztott hozzáférés-aláírások (SAS) engedélyezési szabályát.</span><span class="sxs-lookup"><span data-stu-id="5ca46-106">The **Remove-AzureRmNotificationHubsNamespaceAuthorizationRules** cmdlet removes a Shared Access Signature (SAS) authorization rule from a notification hub namespace.</span></span>
<span data-ttu-id="5ca46-107">Az engedélyezési szabályok kezelik a névterek elérését.</span><span class="sxs-lookup"><span data-stu-id="5ca46-107">Authorization rules manage access to a namespace.</span></span>
<span data-ttu-id="5ca46-108">Ezt úgy teheti meg, hogy a hivatkozásokat a különböző jogosultsági szintek alapján URI-ként hozza létre.</span><span class="sxs-lookup"><span data-stu-id="5ca46-108">This is done by through the creation of links, as URIs, based on different permission levels.</span></span>
<span data-ttu-id="5ca46-109">A jogosultsági szintek az alábbiak lehetnek:</span><span class="sxs-lookup"><span data-stu-id="5ca46-109">Permission levels can be of the following:</span></span> 
- <span data-ttu-id="5ca46-110">Hallgatni</span><span class="sxs-lookup"><span data-stu-id="5ca46-110">Listen</span></span>
- <span data-ttu-id="5ca46-111">Küldése</span><span class="sxs-lookup"><span data-stu-id="5ca46-111">Send</span></span>
- <span data-ttu-id="5ca46-112">Az ügyfelek kezelése a megfelelő jogosultsági szint alapján a fenti URI-k egyikéhez van irányítva.</span><span class="sxs-lookup"><span data-stu-id="5ca46-112">Manage Clients are directed to one of these URIs based on the appropriate permission level.</span></span>
<span data-ttu-id="5ca46-113">A figyelési engedélyt tartalmazó ügyfél például az adott engedélyhez tartozó URI-azonosítóra irányul.</span><span class="sxs-lookup"><span data-stu-id="5ca46-113">For instance, a client given the Listen permission is directed to the URI for that permission.</span></span>
<span data-ttu-id="5ca46-114">Egy engedélyezési szabály eltávolítása a megfelelő felhasználói engedélyt is eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="5ca46-114">Removing an authorization rule also removes the corresponding user permission.</span></span>

## <span data-ttu-id="5ca46-115">Példák</span><span class="sxs-lookup"><span data-stu-id="5ca46-115">EXAMPLES</span></span>

### <span data-ttu-id="5ca46-116">1. példa: engedélyezési szabály eltávolítása egy névtérből</span><span class="sxs-lookup"><span data-stu-id="5ca46-116">Example 1: Remove an authorization rule from a namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubNamespaceAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

<span data-ttu-id="5ca46-117">Ez a parancs eltávolítja a ListenRule nevű engedélyezési szabályt a ContosoNamespace nevű névtérből.</span><span class="sxs-lookup"><span data-stu-id="5ca46-117">This command removes the authorization rule named ListenRule from the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="5ca46-118">A parancs futtatásakor meg kell adnia azt az erőforráscsoport-csoportot, amelyhez a névtér hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="5ca46-118">When you run this command you must specify the resource group that the namespace is assigned to.</span></span>

## <span data-ttu-id="5ca46-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ca46-119">PARAMETERS</span></span>

### <span data-ttu-id="5ca46-120">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5ca46-120">-AuthorizationRule</span></span>
<span data-ttu-id="5ca46-121">Annak a SAS-hitelesítési szabálynak a nevét adja meg, amelyet el szeretne távolítani.</span><span class="sxs-lookup"><span data-stu-id="5ca46-121">Specifies the name of the SAS authentication rule to be removed.</span></span>

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

### <span data-ttu-id="5ca46-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca46-122">-DefaultProfile</span></span>
<span data-ttu-id="5ca46-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5ca46-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ca46-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5ca46-124">-Force</span></span>
<span data-ttu-id="5ca46-125">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ca46-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5ca46-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5ca46-126">-Namespace</span></span>
<span data-ttu-id="5ca46-127">Azt a névteret adja meg, amelyre az engedélyezési szabályok hozzá vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="5ca46-127">Specifies the namespace to which the authorization rules are assigned.</span></span>
<span data-ttu-id="5ca46-128">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="5ca46-128">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="5ca46-129">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5ca46-129">-ResourceGroup</span></span>
<span data-ttu-id="5ca46-130">Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.</span><span class="sxs-lookup"><span data-stu-id="5ca46-130">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="5ca46-131">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="5ca46-131">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="5ca46-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ca46-132">-Confirm</span></span>
<span data-ttu-id="5ca46-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ca46-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ca46-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ca46-134">-WhatIf</span></span>
<span data-ttu-id="5ca46-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ca46-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ca46-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ca46-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ca46-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca46-137">CommonParameters</span></span>
<span data-ttu-id="5ca46-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ca46-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca46-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ca46-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca46-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ca46-140">INPUTS</span></span>

### <span data-ttu-id="5ca46-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5ca46-141">System.String</span></span>

## <span data-ttu-id="5ca46-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ca46-142">OUTPUTS</span></span>

### <span data-ttu-id="5ca46-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ca46-143">System.Boolean</span></span>

## <span data-ttu-id="5ca46-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ca46-144">NOTES</span></span>

## <span data-ttu-id="5ca46-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ca46-145">RELATED LINKS</span></span>

[<span data-ttu-id="5ca46-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="5ca46-146">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="5ca46-147">Új – AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="5ca46-147">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="5ca46-148">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="5ca46-148">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](./Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


