---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHub.md
ms.openlocfilehash: d270e3020e03a02461d9c54e19458af10401ee79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186060"
---
# <span data-ttu-id="a0f2b-101">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a0f2b-101">Get-AzNotificationHub</span></span>

## <span data-ttu-id="a0f2b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f2b-103">Információt kap az értesítési hubokról.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-103">Gets information about your notification hubs.</span></span>

## <span data-ttu-id="a0f2b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0f2b-104">SYNTAX</span></span>

```
Get-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0f2b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0f2b-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f2b-106">A **Get-AzNotificationHub** parancsmag információkat kap a megadott névtérben lévő értesítési hubokról, és egy adott erőforráscsoport számára van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-106">The **Get-AzNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="a0f2b-107">Információkat kaphat például az összes értesítési hubokról a névtér ContosoNamespace, és hozzárendelve a ContosoNotificationsGroup erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>
<span data-ttu-id="a0f2b-108">Másik lehetőségként a *NotificationHub* paraméterrel korlátozhatja a visszaadott adatokat az adott értesítési központra vonatkozó információkra.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>
<span data-ttu-id="a0f2b-109">Az értesítési hubok a leküldéses értesítéseket több ügyfélnek küldik el, függetlenül attól, hogy milyen platformról, például iOS, Android, Windows Phone 8 vagy Windows áruházból, ezek az ügyfelek használják őket.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="a0f2b-110">Ezek a hubok nagyjából egyenértékűek az egyes alkalmazásokkal, és az egyes alkalmazások általában saját értesítési központtal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="a0f2b-111">Ez a parancsmag csak a hub adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="a0f2b-112">Más parancsmagok, például a Get-AzNotificationHubAuthorizationRules, a Get-AzNotificationHubListKeys és a Get-AzNotificationHubPNSCredentials szükségesek a hub engedélyezési szabályairól, a csatlakozási karakterláncokról és a platform értesítési szolgáltatásának hitelesítő adatairól.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-112">Other cmdlets, such as Get-AzNotificationHubAuthorizationRules, Get-AzNotificationHubListKeys, and Get-AzNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="a0f2b-113">Példák</span><span class="sxs-lookup"><span data-stu-id="a0f2b-113">EXAMPLES</span></span>

### <span data-ttu-id="a0f2b-114">1. példa: információ kérése egy adott névtérben lévő összes értesítési hubokról</span><span class="sxs-lookup"><span data-stu-id="a0f2b-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="a0f2b-115">Ez a parancs információkat kap az erőforráscsoport ContosoNotificationsGroup rendelt ContosoNamespace nevű névtérben található összes értesítési hubokról.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="a0f2b-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0f2b-116">PARAMETERS</span></span>

### <span data-ttu-id="a0f2b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f2b-117">-DefaultProfile</span></span>
<span data-ttu-id="a0f2b-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a0f2b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0f2b-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a0f2b-119">-Namespace</span></span>
<span data-ttu-id="a0f2b-120">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-120">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="a0f2b-121">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="a0f2b-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="a0f2b-122">-NotificationHub</span></span>
<span data-ttu-id="a0f2b-123">Annak az értesítési csomópontnak a nevét adja meg, amelyre a parancsmag beérkezik.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>
<span data-ttu-id="a0f2b-124">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="a0f2b-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a0f2b-125">-ResourceGroup</span></span>
<span data-ttu-id="a0f2b-126">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-126">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="a0f2b-127">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="a0f2b-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="a0f2b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f2b-128">CommonParameters</span></span>
<span data-ttu-id="a0f2b-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0f2b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f2b-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f2b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f2b-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0f2b-131">INPUTS</span></span>

### <span data-ttu-id="a0f2b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a0f2b-132">System.String</span></span>

## <span data-ttu-id="a0f2b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0f2b-133">OUTPUTS</span></span>

### <span data-ttu-id="a0f2b-134">Microsoft. Azure. Command. NotificationHubs. models. NotificationHubAttributes</span><span class="sxs-lookup"><span data-stu-id="a0f2b-134">Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes</span></span>

## <span data-ttu-id="a0f2b-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0f2b-135">NOTES</span></span>

## <span data-ttu-id="a0f2b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0f2b-136">RELATED LINKS</span></span>

[<span data-ttu-id="a0f2b-137">Get-AzNotificationHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a0f2b-137">Get-AzNotificationHubAuthorizationRule</span></span>](./Get-AzNotificationHubAuthorizationRule.md)

[<span data-ttu-id="a0f2b-138">Get-AzNotificationHubListKey</span><span class="sxs-lookup"><span data-stu-id="a0f2b-138">Get-AzNotificationHubListKey</span></span>](./Get-AzNotificationHubListKey.md)

[<span data-ttu-id="a0f2b-139">Get-AzNotificationHubPNSCredential</span><span class="sxs-lookup"><span data-stu-id="a0f2b-139">Get-AzNotificationHubPNSCredential</span></span>](./Get-AzNotificationHubPNSCredential.md)

[<span data-ttu-id="a0f2b-140">Új – AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a0f2b-140">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="a0f2b-141">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a0f2b-141">Remove-AzNotificationHub</span></span>](./Remove-AzNotificationHub.md)

[<span data-ttu-id="a0f2b-142">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="a0f2b-142">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)

