---
Module Name: Az.NotificationHubs
Module Guid: f875725d-8ce4-423f-a6af-ea880bc63f13
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs
Help Version: 4.1.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Az.NotificationHubs.md
ms.openlocfilehash: dd39a8f87120ea7aaddb4570276e1e3060873e2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336318"
---
# <span data-ttu-id="1ee15-101">Az.NotificationHubs modul</span><span class="sxs-lookup"><span data-stu-id="1ee15-101">Az.NotificationHubs Module</span></span>
## <span data-ttu-id="1ee15-102">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ee15-102">Description</span></span>
<span data-ttu-id="1ee15-103">Ez a témakör az Azure Értesítési központ parancsmagokkal kapcsolatos súgótémaköreket mutatja be.</span><span class="sxs-lookup"><span data-stu-id="1ee15-103">This topic displays help topics for the Azure Notification Hub cmdlets.</span></span> <span data-ttu-id="1ee15-104">Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek, függetlenül attól, hogy milyen platformon (iOS, Android, Windows Phone 8, Windows Áruház stb.) használják őket.</span><span class="sxs-lookup"><span data-stu-id="1ee15-104">Notification hubs are used to send push notifications to multiple clients regardless of the platform (iOS, Android, Windows Phone 8, Windows Store, etc.) used by those clients.</span></span> <span data-ttu-id="1ee15-105">Ezek a központok nagyjából egyenértékűek az egyes appokkal: mindegyik alkalmazásnak általában saját értesítési központja lesz.</span><span class="sxs-lookup"><span data-stu-id="1ee15-105">These hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span> <span data-ttu-id="1ee15-106">Az értesítési központok a névterek néven ismert logikai tárolókba vannak rendezve, és a megosztott hozzáférés-aláírás (SAS) engedélyezési szabályai a hubok és a névterek elérésének kezelésére használhatók.</span><span class="sxs-lookup"><span data-stu-id="1ee15-106">Notification hubs are organized within logical containers known as namespaces, and Shared Access Signature (SAS) authorization rules are used to manage access to hubs and namespaces.</span></span> <span data-ttu-id="1ee15-107">Ezeket az elemeket az Értesítési központ parancsmagokkal is felügyelheti.</span><span class="sxs-lookup"><span data-stu-id="1ee15-107">All of these elements can be administered by using the Notification Hub cmdlets.</span></span>

## <span data-ttu-id="1ee15-108">Az.NotificationHubs parancsmagok</span><span class="sxs-lookup"><span data-stu-id="1ee15-108">Az.NotificationHubs Cmdlets</span></span>
### [<span data-ttu-id="1ee15-109">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1ee15-109">Get-AzNotificationHub</span></span>](Get-AzNotificationHub.md)
<span data-ttu-id="1ee15-110">Információkat kap az értesítési központokról.</span><span class="sxs-lookup"><span data-stu-id="1ee15-110">Gets information about your notification hubs.</span></span>

### [<span data-ttu-id="1ee15-111">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ee15-111">Get-AzNotificationHubAuthorizationRule</span></span>](Get-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="1ee15-112">Információkat kap az értesítési központhoz társított engedélyezési szabályokról.</span><span class="sxs-lookup"><span data-stu-id="1ee15-112">Gets information about the authorization rules associated with a notification hub.</span></span>

### [<span data-ttu-id="1ee15-113">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="1ee15-113">Get-AzNotificationHubListKey</span></span>](Get-AzNotificationHubListKey.md)
<span data-ttu-id="1ee15-114">Lekérte az értesítési központ engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat.</span><span class="sxs-lookup"><span data-stu-id="1ee15-114">Gets the primary and secondary connection strings associated with a notification hub authorization rule.</span></span>

### [<span data-ttu-id="1ee15-115">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="1ee15-115">Get-AzNotificationHubPNSCredential</span></span>](Get-AzNotificationHubPNSCredential.md)
<span data-ttu-id="1ee15-116">Egy értesítési központ PNS-hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1ee15-116">Gets the PNS credentials for a notification hub.</span></span>

### [<span data-ttu-id="1ee15-117">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1ee15-117">Get-AzNotificationHubsNamespace</span></span>](Get-AzNotificationHubsNamespace.md)
<span data-ttu-id="1ee15-118">Információkat kap egy értesítési központ névterről.</span><span class="sxs-lookup"><span data-stu-id="1ee15-118">Gets information about a notification hub namespace.</span></span>

### [<span data-ttu-id="1ee15-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ee15-119">Get-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Get-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="1ee15-120">Információkat kap az értesítési központ névterére vonatkozó engedélyezési szabályokról.</span><span class="sxs-lookup"><span data-stu-id="1ee15-120">Gets information about the authorization rules associated with a notification hub namespace.</span></span>

### [<span data-ttu-id="1ee15-121">Get-AzNotificationHubsNamespaceListKey</span><span class="sxs-lookup"><span data-stu-id="1ee15-121">Get-AzNotificationHubsNamespaceListKey</span></span>](Get-AzNotificationHubsNamespaceListKey.md)
<span data-ttu-id="1ee15-122">Behozza az értesítési központ névtér-engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat.</span><span class="sxs-lookup"><span data-stu-id="1ee15-122">Gets the primary and secondary connection strings associated with a notification hub namespace authorization rule.</span></span>

### [<span data-ttu-id="1ee15-123">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1ee15-123">New-AzNotificationHub</span></span>](New-AzNotificationHub.md)
<span data-ttu-id="1ee15-124">Létrehoz egy értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="1ee15-124">Creates a notification hub.</span></span>

### [<span data-ttu-id="1ee15-125">New-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ee15-125">New-AzNotificationHubAuthorizationRule</span></span>](New-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="1ee15-126">Engedélyezési szabályt hoz létre, és hozzárendeli a szabályt egy értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="1ee15-126">Creates an authorization rule and assigns the rule to a notification hub.</span></span>

### [<span data-ttu-id="1ee15-127">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="1ee15-127">New-AzNotificationHubKey</span></span>](New-AzNotificationHubKey.md)
<span data-ttu-id="1ee15-128">A NotificationHub engedélyezési szabálykulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="1ee15-128">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

### [<span data-ttu-id="1ee15-129">New-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1ee15-129">New-AzNotificationHubsNamespace</span></span>](New-AzNotificationHubsNamespace.md)
<span data-ttu-id="1ee15-130">Létrehoz egy értesítési központ névterét.</span><span class="sxs-lookup"><span data-stu-id="1ee15-130">Creates a notification hub namespace.</span></span>

### [<span data-ttu-id="1ee15-131">New-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ee15-131">New-AzNotificationHubsNamespaceAuthorizationRule</span></span>](New-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="1ee15-132">Engedélyezési szabályt hoz létre, és hozzárendeli azt egy értesítési központ névterhez.</span><span class="sxs-lookup"><span data-stu-id="1ee15-132">Creates an authorization rule and assigns that rule to a notification hub namespace.</span></span>

### [<span data-ttu-id="1ee15-133">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="1ee15-133">New-AzNotificationHubsNamespaceKey</span></span>](New-AzNotificationHubsNamespaceKey.md)
<span data-ttu-id="1ee15-134">A Névtér engedélyezési szabálykulcsának újragenerálása</span><span class="sxs-lookup"><span data-stu-id="1ee15-134">Regenerate the Authorization Rule Key for a Namespace.</span></span>

### [<span data-ttu-id="1ee15-135">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1ee15-135">Remove-AzNotificationHub</span></span>](Remove-AzNotificationHub.md)
<span data-ttu-id="1ee15-136">Eltávolít egy meglévő értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="1ee15-136">Removes an existing notification hub.</span></span>

### [<span data-ttu-id="1ee15-137">Remove-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ee15-137">Remove-AzNotificationHubAuthorizationRule</span></span>](Remove-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="1ee15-138">Eltávolít egy engedélyezési szabályt egy értesítési központban.</span><span class="sxs-lookup"><span data-stu-id="1ee15-138">Removes an authorization rule from a notification hub.</span></span>

### [<span data-ttu-id="1ee15-139">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1ee15-139">Remove-AzNotificationHubsNamespace</span></span>](Remove-AzNotificationHubsNamespace.md)
<span data-ttu-id="1ee15-140">Eltávolítja az értesítési központ névterét.</span><span class="sxs-lookup"><span data-stu-id="1ee15-140">Removes a notification hub namespace.</span></span>

### [<span data-ttu-id="1ee15-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ee15-141">Remove-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Remove-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="1ee15-142">Eltávolít egy engedélyezési szabályt az értesítési központ névterében.</span><span class="sxs-lookup"><span data-stu-id="1ee15-142">Removes an authorization rule from a notification hub namespace.</span></span>

### [<span data-ttu-id="1ee15-143">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="1ee15-143">Set-AzNotificationHub</span></span>](Set-AzNotificationHub.md)
<span data-ttu-id="1ee15-144">Egy értesítési központ tulajdonságértékét állítja be.</span><span class="sxs-lookup"><span data-stu-id="1ee15-144">Sets property values for a notification hub.</span></span>

### [<span data-ttu-id="1ee15-145">Set-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ee15-145">Set-AzNotificationHubAuthorizationRule</span></span>](Set-AzNotificationHubAuthorizationRule.md)
<span data-ttu-id="1ee15-146">Engedélyezési szabályokat állít be egy értesítési központhoz.</span><span class="sxs-lookup"><span data-stu-id="1ee15-146">Sets authorization rules for a notification hub.</span></span>

### [<span data-ttu-id="1ee15-147">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="1ee15-147">Set-AzNotificationHubsNamespace</span></span>](Set-AzNotificationHubsNamespace.md)
<span data-ttu-id="1ee15-148">Beállítja egy értesítési központ névterének tulajdonságértékét.</span><span class="sxs-lookup"><span data-stu-id="1ee15-148">Sets property values for a notification hub namespace.</span></span>

### [<span data-ttu-id="1ee15-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1ee15-149">Set-AzNotificationHubsNamespaceAuthorizationRule</span></span>](Set-AzNotificationHubsNamespaceAuthorizationRule.md)
<span data-ttu-id="1ee15-150">Engedélyezési szabályokat állít be az értesítési központ névterében.</span><span class="sxs-lookup"><span data-stu-id="1ee15-150">Sets authorization rules for a notification hub namespace.</span></span>

