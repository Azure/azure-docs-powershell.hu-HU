---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: 944805a4883edce9354cfa372bfd30db145fc4ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479855"
---
# <span data-ttu-id="97720-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="97720-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="97720-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97720-102">SYNOPSIS</span></span>
<span data-ttu-id="97720-103">Információkat kap az értesítési központokról.</span><span class="sxs-lookup"><span data-stu-id="97720-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="97720-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="97720-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97720-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="97720-105">DESCRIPTION</span></span>
<span data-ttu-id="97720-106">A **Get-AzNotificationHub** parancsmag információt kap egy megadott névtér értesítési központjáról, és hozzárendel egy adott erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="97720-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="97720-107">Információkat kaphat például a ContosoNamespace névtér összes értesítési központjáról, és hozzárendelheti őket a ContosoNotificationsGroup erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="97720-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="97720-108">Másik lehetőségként az *NotificationHub* paraméterrel korlátozhatja a visszaadott adatokat egy adott értesítési központ adataira.</span><span class="sxs-lookup"><span data-stu-id="97720-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="97720-109">Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek, függetlenül attól, hogy milyen platformot használnak (például iOS, Android, Windows Phone 8 és Windows Áruház).</span><span class="sxs-lookup"><span data-stu-id="97720-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="97720-110">Ezek a központok nagyjából egyenértékűek az egyes alkalmazásokkal, és mindegyik alkalmazásnak általában saját értesítési központja lesz.</span><span class="sxs-lookup"><span data-stu-id="97720-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="97720-111">Ez a parancsmag csak a központról kap információt.</span><span class="sxs-lookup"><span data-stu-id="97720-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="97720-112">Más parancsmagokra, például a Get-AzNotificationHubAuthorizationRules, a Get-AzNotificationHubListKeys és a Get-AzNotificationHubPNSCredentials parancsmagra van szükség a központ engedélyezési szabályaival, kapcsolati karakterláncokkal és platformértesítési szolgáltatás hitelesítő adataival kapcsolatos információkhoz.</span><span class="sxs-lookup"><span data-stu-id="97720-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="97720-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="97720-113">EXAMPLES</span></span>

### <span data-ttu-id="97720-114">1. példa: Információ lekérte az adott névtér összes értesítési központját</span><span class="sxs-lookup"><span data-stu-id="97720-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```powershell
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="97720-115">Ez a parancs információkat kap a ContosoNamespace nevű névtér összes, a ContosoNotificationsGroup erőforráscsoporthoz hozzárendelt értesítési központról.</span><span class="sxs-lookup"><span data-stu-id="97720-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

### <span data-ttu-id="97720-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="97720-116">Example 2</span></span>

<span data-ttu-id="97720-117">Információkat kap az értesítési központokról.</span><span class="sxs-lookup"><span data-stu-id="97720-117">Gets information about your notification hubs.</span></span> <span data-ttu-id="97720-118">(automatikusan generált)</span><span class="sxs-lookup"><span data-stu-id="97720-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNotificationHub -Namespace 'ContosoNamespace' -NotificationHub 'ContosoInternalHub' -ResourceGroup 'ContosoNotificationsGroup'
```

## <span data-ttu-id="97720-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97720-119">PARAMETERS</span></span>

### <span data-ttu-id="97720-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97720-120">-DefaultProfile</span></span>
<span data-ttu-id="97720-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="97720-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97720-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="97720-122">-Namespace</span></span>
<span data-ttu-id="97720-123">Azt a névteret adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="97720-123">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="97720-124">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="97720-124">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="97720-125">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="97720-125">-NotificationHub</span></span>
<span data-ttu-id="97720-126">A parancsmag értesítési központjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="97720-126">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="97720-127">Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek attól függetlenül, hogy milyen platformon használják őket.</span><span class="sxs-lookup"><span data-stu-id="97720-127">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="97720-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="97720-128">-ResourceGroup</span></span>
<span data-ttu-id="97720-129">Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="97720-129">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="97720-130">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="97720-130">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="97720-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97720-131">CommonParameters</span></span>
<span data-ttu-id="97720-132">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97720-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97720-133">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97720-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97720-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97720-134">INPUTS</span></span>

### <span data-ttu-id="97720-135">System.String</span><span class="sxs-lookup"><span data-stu-id="97720-135">System.String</span></span>

## <span data-ttu-id="97720-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97720-136">OUTPUTS</span></span>

### <span data-ttu-id="97720-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="97720-137">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="97720-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="97720-138">NOTES</span></span>

## <span data-ttu-id="97720-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97720-139">RELATED LINKS</span></span>

[<span data-ttu-id="97720-140">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="97720-140">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="97720-141">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="97720-141">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="97720-142">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="97720-142">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="97720-143">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="97720-143">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="97720-144">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="97720-144">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="97720-145">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="97720-145">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


