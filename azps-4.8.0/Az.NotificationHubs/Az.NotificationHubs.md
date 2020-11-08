---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184048"
---
# <span data-ttu-id="cb8de-101">Az. NotificationHubs modul</span><span class="sxs-lookup"><span data-stu-id="cb8de-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="cb8de-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb8de-102">Description</span></span>
<span data-ttu-id="cb8de-103">Ez a témakör az Azure Notification hub-parancsmagok súgótémaköröket jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="cb8de-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="cb8de-104">Az értesítési hubok a leküldéses értesítéseket több ügyfélnek küldik el, függetlenül attól, hogy milyen platformon (iOS, Android, Windows Phone 8, Windows áruház stb.) használják ezeket az ügyfelek.</span><span class="sxs-lookup"><span data-stu-id="cb8de-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="cb8de-105">Ezek a hubok nagyjából egyenértékűek az egyes alkalmazásokkal: az egyes alkalmazások általában saját értesítési központtal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="cb8de-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="cb8de-106">Az értesítési hubok a névterek néven ismert logikai tárolókban, míg a megosztott hozzáférés-aláírási (SAS) engedélyezési szabályok az hubokhoz és névterekhez való hozzáférés kezelésére szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="cb8de-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="cb8de-107">Az alábbi elemek mindegyike felügyelhető az értesítési hub-parancsmagok használatával.</span><span class="sxs-lookup"><span data-stu-id="cb8de-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="cb8de-108">Az. NotificationHubs parancsmagok</span><span class="sxs-lookup"><span data-stu-id="cb8de-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="cb8de-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cb8de-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="cb8de-110">Információt kap az értesítési hubokról.</span><span class="sxs-lookup"><span data-stu-id="cb8de-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="cb8de-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cb8de-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="cb8de-112">Információt kap az értesítési központtal társított engedélyezési szabályokról.</span><span class="sxs-lookup"><span data-stu-id="cb8de-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="cb8de-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="cb8de-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="cb8de-114">Az értesítési hub engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cb8de-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="cb8de-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="cb8de-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="cb8de-116">Beolvassa az értesítési központ PNS hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="cb8de-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="cb8de-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cb8de-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="cb8de-118">Információt kap az értesítési hub névteréről.</span><span class="sxs-lookup"><span data-stu-id="cb8de-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="cb8de-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cb8de-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="cb8de-120">Információt kap az értesítési hub névteréhez társított engedélyezési szabályokról.</span><span class="sxs-lookup"><span data-stu-id="cb8de-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="cb8de-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="cb8de-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="cb8de-122">Az értesítési hub névtér-engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="cb8de-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="cb8de-123">Új – AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cb8de-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="cb8de-124">Értesítési hubot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cb8de-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="cb8de-125">Új – AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cb8de-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="cb8de-126">Létrehoz egy engedélyezési szabályt, és hozzárendeli a szabályt egy értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="cb8de-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="cb8de-127">Új – AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="cb8de-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="cb8de-128">A NotificationHub tartozó engedélyezési szabály kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="cb8de-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="cb8de-129">Új – AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cb8de-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="cb8de-130">Az értesítési hub névteret hozza létre.</span><span class="sxs-lookup"><span data-stu-id="cb8de-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="cb8de-131">Új – AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cb8de-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="cb8de-132">Létrehoz egy engedélyezési szabályt, és hozzárendeli a szabályt egy értesítési hub-névtérhez.</span><span class="sxs-lookup"><span data-stu-id="cb8de-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="cb8de-133">Új – AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="cb8de-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="cb8de-134">Egy névtérhez tartozó engedélyezési szabály kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="cb8de-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="cb8de-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cb8de-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="cb8de-136">Egy meglévő értesítési hub eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="cb8de-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="cb8de-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cb8de-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="cb8de-138">Egy engedélyezési szabály eltávolítása az értesítési központból.</span><span class="sxs-lookup"><span data-stu-id="cb8de-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="cb8de-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cb8de-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="cb8de-140">Az értesítési hub névterének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="cb8de-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="cb8de-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cb8de-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="cb8de-142">Az értesítési központ névterének engedélyezési szabályait távolítja el.</span><span class="sxs-lookup"><span data-stu-id="cb8de-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="cb8de-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="cb8de-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="cb8de-144">Egy értesítési központhoz tartozó tulajdonságértékek beállítása.</span><span class="sxs-lookup"><span data-stu-id="cb8de-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="cb8de-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cb8de-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="cb8de-146">Engedélyezési szabályokat állít be az értesítési központban.</span><span class="sxs-lookup"><span data-stu-id="cb8de-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="cb8de-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="cb8de-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="cb8de-148">Az értesítési hub-névtér tulajdonság-értékeit állítja be.</span><span class="sxs-lookup"><span data-stu-id="cb8de-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="cb8de-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="cb8de-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="cb8de-150">Az értesítési hub névterének engedélyezési szabályait állítja be.</span><span class="sxs-lookup"><span data-stu-id="cb8de-150">Sets authorization rules for a notification hub namespace.</span></span>

