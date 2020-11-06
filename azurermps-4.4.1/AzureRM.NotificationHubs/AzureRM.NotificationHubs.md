---
Module Name: AzureRM.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/AzureRM.NotificationHubs.md
ms.openlocfilehash: 2997b465f02801e2b01004d45209e95af7998ff6
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490472"
---
# <span data-ttu-id="f0335-101">AzureRM. NotificationHubs modul</span><span class="sxs-lookup"><span data-stu-id="f0335-101">AzureRM.NotificationHubs Module</span></span>
## <span data-ttu-id="f0335-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0335-102">Description</span></span>
<span data-ttu-id="f0335-103">Ez a témakör az Azure Notification hub-parancsmagok súgótémaköröket jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="f0335-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="f0335-104">Az értesítési hubok a leküldéses értesítéseket több ügyfélnek küldik el, függetlenül attól, hogy milyen platformon (iOS, Android, Windows Phone 8, Windows áruház stb.) használják ezeket az ügyfelek.</span><span class="sxs-lookup"><span data-stu-id="f0335-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="f0335-105">Ezek a hubok nagyjából egyenértékűek az egyes alkalmazásokkal: az egyes alkalmazások általában saját értesítési központtal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="f0335-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="f0335-106">Az értesítési hubok a névterek néven ismert logikai tárolókban, míg a megosztott hozzáférés-aláírási (SAS) engedélyezési szabályok az hubokhoz és névterekhez való hozzáférés kezelésére szolgálnak.</span><span class="sxs-lookup"><span data-stu-id="f0335-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="f0335-107">Az alábbi elemek mindegyike felügyelhető az értesítési hub-parancsmagok használatával.</span><span class="sxs-lookup"><span data-stu-id="f0335-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="f0335-108">AzureRM. NotificationHubs parancsmagok</span><span class="sxs-lookup"><span data-stu-id="f0335-108">AzureRM.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="f0335-109">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f0335-109">Get-AzureRmNotificationHub</span></span>](Get-AzureRmNotificationHub.md)
<span data-ttu-id="f0335-110">Információt kap az értesítési hubokról.</span><span class="sxs-lookup"><span data-stu-id="f0335-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="f0335-111">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f0335-111">Get-AzureRmNotificationHubAuthorizationRules</span></span>](Get-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="f0335-112">Információt kap az értesítési központtal társított engedélyezési szabályokról.</span><span class="sxs-lookup"><span data-stu-id="f0335-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="f0335-113">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="f0335-113">Get-AzureRmNotificationHubListKeys</span></span>](Get-AzureRmNotificationHubListKeys.md)
<span data-ttu-id="f0335-114">Az értesítési hub engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f0335-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="f0335-115">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="f0335-115">Get-AzureRmNotificationHubPNSCredentials</span></span>](Get-AzureRmNotificationHubPNSCredentials.md)
<span data-ttu-id="f0335-116">Beolvassa az értesítési központ PNS hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="f0335-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="f0335-117">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f0335-117">Get-AzureRmNotificationHubsNamespace</span></span>](Get-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="f0335-118">Információt kap az értesítési hub névteréről.</span><span class="sxs-lookup"><span data-stu-id="f0335-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="f0335-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f0335-119">Get-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="f0335-120">Információt kap az értesítési hub névteréhez társított engedélyezési szabályokról.</span><span class="sxs-lookup"><span data-stu-id="f0335-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="f0335-121">Get-AzureRmNotificationHubsNamespaceListKeys</span><span class="sxs-lookup"><span data-stu-id="f0335-121">Get-AzureRmNotificationHubsNamespaceListKeys</span></span>](Get-AzureRmNotificationHubsNamespaceListKeys.md)
<span data-ttu-id="f0335-122">Az értesítési hub névtér-engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f0335-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="f0335-123">Új – AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f0335-123">New-AzureRmNotificationHub</span></span>](New-AzureRmNotificationHub.md)
<span data-ttu-id="f0335-124">Értesítési hubot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f0335-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="f0335-125">Új – AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f0335-125">New-AzureRmNotificationHubAuthorizationRules</span></span>](New-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="f0335-126">Létrehoz egy engedélyezési szabályt, és hozzárendeli a szabályt egy értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="f0335-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="f0335-127">Új – AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="f0335-127">New-AzureRmNotificationHubKey</span></span>](New-AzureRmNotificationHubKey.md)
<span data-ttu-id="f0335-128">A NotificationHub tartozó engedélyezési szabály kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="f0335-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="f0335-129">Új – AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f0335-129">New-AzureRmNotificationHubsNamespace</span></span>](New-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="f0335-130">Az értesítési hub névteret hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f0335-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="f0335-131">Új – AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f0335-131">New-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](New-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="f0335-132">Létrehoz egy engedélyezési szabályt, és hozzárendeli a szabályt egy értesítési hub-névtérhez.</span><span class="sxs-lookup"><span data-stu-id="f0335-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="f0335-133">Új – AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="f0335-133">New-AzureRmNotificationHubsNamespaceKey</span></span>](New-AzureRmNotificationHubsNamespaceKey.md)
<span data-ttu-id="f0335-134">Egy névtérhez tartozó engedélyezési szabály kulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="f0335-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="f0335-135">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f0335-135">Remove-AzureRmNotificationHub</span></span>](Remove-AzureRmNotificationHub.md)
<span data-ttu-id="f0335-136">Egy meglévő értesítési hub eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="f0335-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="f0335-137">Remove-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f0335-137">Remove-AzureRmNotificationHubAuthorizationRules</span></span>](Remove-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="f0335-138">Egy engedélyezési szabály eltávolítása az értesítési központból.</span><span class="sxs-lookup"><span data-stu-id="f0335-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="f0335-139">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f0335-139">Remove-AzureRmNotificationHubsNamespace</span></span>](Remove-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="f0335-140">Az értesítési hub névterének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="f0335-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="f0335-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f0335-141">Remove-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Remove-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="f0335-142">Az értesítési központ névterének engedélyezési szabályait távolítja el.</span><span class="sxs-lookup"><span data-stu-id="f0335-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="f0335-143">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f0335-143">Set-AzureRmNotificationHub</span></span>](Set-AzureRmNotificationHub.md)
<span data-ttu-id="f0335-144">Egy értesítési központhoz tartozó tulajdonságértékek beállítása.</span><span class="sxs-lookup"><span data-stu-id="f0335-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="f0335-145">Set-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f0335-145">Set-AzureRmNotificationHubAuthorizationRules</span></span>](Set-AzureRmNotificationHubAuthorizationRules.md)
<span data-ttu-id="f0335-146">Engedélyezési szabályokat állít be az értesítési központban.</span><span class="sxs-lookup"><span data-stu-id="f0335-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="f0335-147">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="f0335-147">Set-AzureRmNotificationHubsNamespace</span></span>](Set-AzureRmNotificationHubsNamespace.md)
<span data-ttu-id="f0335-148">Az értesítési hub-névtér tulajdonság-értékeit állítja be.</span><span class="sxs-lookup"><span data-stu-id="f0335-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="f0335-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f0335-149">Set-AzureRmNotificationHubsNamespaceAuthorizationRules</span></span>](Set-AzureRmNotificationHubsNamespaceAuthorizationRules.md)
<span data-ttu-id="f0335-150">Az értesítési hub névterének engedélyezési szabályait állítja be.</span><span class="sxs-lookup"><span data-stu-id="f0335-150">Sets authorization rules for a notification hub namespace.</span></span>

