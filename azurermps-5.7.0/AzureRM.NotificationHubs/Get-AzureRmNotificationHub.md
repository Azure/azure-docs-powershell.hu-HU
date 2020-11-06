---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
ms.openlocfilehash: cfe24ac2900e46a031980886f80bf39b9eee28e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504515"
---
# <span data-ttu-id="f8783-101">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f8783-101">Get-AzureRmNotificationHub</span></span>

## <span data-ttu-id="f8783-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f8783-102">SYNOPSIS</span></span>
<span data-ttu-id="f8783-103">Információt kap az értesítési hubokról.</span><span class="sxs-lookup"><span data-stu-id="f8783-103">Gets information about your notification hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8783-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f8783-104">SYNTAX</span></span>

```
Get-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8783-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f8783-105">DESCRIPTION</span></span>
<span data-ttu-id="f8783-106">A **Get-AzureRmNotificationHub** parancsmag információkat kap a megadott névtérben lévő értesítési hubokról, és egy adott erőforráscsoport számára van hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="f8783-106">The **Get-AzureRmNotificationHub** cmdlet gets information about the notification hubs in a specified namespace and assigned to a specified resource group.</span></span>
<span data-ttu-id="f8783-107">Információkat kaphat például az összes értesítési hubokról a névtér ContosoNamespace, és hozzárendelve a ContosoNotificationsGroup erőforráscsoporthoz.</span><span class="sxs-lookup"><span data-stu-id="f8783-107">For example, you can get information for all the notification hubs in the namespace ContosoNamespace and assigned to the ContosoNotificationsGroup resource group.</span></span>

<span data-ttu-id="f8783-108">Másik lehetőségként a *NotificationHub* paraméterrel korlátozhatja a visszaadott adatokat az adott értesítési központra vonatkozó információkra.</span><span class="sxs-lookup"><span data-stu-id="f8783-108">Alternatively, you can use the *NotificationHub* parameter to limit the returned data to information about a specific notification hub.</span></span>

<span data-ttu-id="f8783-109">Az értesítési hubok a leküldéses értesítéseket több ügyfélnek küldik el, függetlenül attól, hogy milyen platformról, például iOS, Android, Windows Phone 8 vagy Windows áruházból, ezek az ügyfelek használják őket.</span><span class="sxs-lookup"><span data-stu-id="f8783-109">Notification hubs are used to send push notifications to multiple clients regardless of the platform, such as iOS, Android, Windows Phone 8, and Windows Store, used by those clients.</span></span>
<span data-ttu-id="f8783-110">Ezek a hubok nagyjából egyenértékűek az egyes alkalmazásokkal, és az egyes alkalmazások általában saját értesítési központtal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="f8783-110">These hubs are roughly equivalent to individual apps and each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="f8783-111">Ez a parancsmag csak a hub adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f8783-111">This cmdlet only gets information about the hub itself.</span></span>
<span data-ttu-id="f8783-112">Más parancsmagok, például a Get-AzureRmNotificationHubAuthorizationRules, a Get-AzureRmNotificationHubListKeys és a Get-AzureRmNotificationHubPNSCredentials szükségesek a hub engedélyezési szabályairól, a csatlakozási karakterláncokról és a platform értesítési szolgáltatásának hitelesítő adatairól.</span><span class="sxs-lookup"><span data-stu-id="f8783-112">Other cmdlets, such as Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys, and Get-AzureRmNotificationHubPNSCredentials, are needed to get information about a hub's authorization rules, connection strings, and platform notification service credentials.</span></span>

## <span data-ttu-id="f8783-113">Példák</span><span class="sxs-lookup"><span data-stu-id="f8783-113">EXAMPLES</span></span>

### <span data-ttu-id="f8783-114">1. példa: információ kérése egy adott névtérben lévő összes értesítési hubokról</span><span class="sxs-lookup"><span data-stu-id="f8783-114">Example 1: Get information for all notification hubs in a specific namespace</span></span>
```
PS C:\>Get-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="f8783-115">Ez a parancs információkat kap az erőforráscsoport ContosoNotificationsGroup rendelt ContosoNamespace nevű névtérben található összes értesítési hubokról.</span><span class="sxs-lookup"><span data-stu-id="f8783-115">This command gets information for all the notification hubs in the namespace named ContosoNamespace that have been assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="f8783-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f8783-116">PARAMETERS</span></span>

### <span data-ttu-id="f8783-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8783-117">-DefaultProfile</span></span>
<span data-ttu-id="f8783-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f8783-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8783-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f8783-119">-Namespace</span></span>
<span data-ttu-id="f8783-120">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="f8783-120">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="f8783-121">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="f8783-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8783-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="f8783-122">-NotificationHub</span></span>
<span data-ttu-id="f8783-123">Annak az értesítési csomópontnak a nevét adja meg, amelyre a parancsmag beérkezik.</span><span class="sxs-lookup"><span data-stu-id="f8783-123">Specifies the name of the notification hub that this cmdlet gets.</span></span>

<span data-ttu-id="f8783-124">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="f8783-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8783-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f8783-125">-ResourceGroup</span></span>
<span data-ttu-id="f8783-126">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="f8783-126">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="f8783-127">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="f8783-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8783-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8783-128">CommonParameters</span></span>
<span data-ttu-id="f8783-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f8783-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8783-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8783-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8783-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8783-131">INPUTS</span></span>

### <span data-ttu-id="f8783-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="f8783-132">None</span></span>
<span data-ttu-id="f8783-133">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="f8783-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f8783-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8783-134">OUTPUTS</span></span>

### <span data-ttu-id="f8783-135">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. NotificationHubs. models. NotificationHubAttributes]</span><span class="sxs-lookup"><span data-stu-id="f8783-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes]</span></span>

## <span data-ttu-id="f8783-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f8783-136">NOTES</span></span>

## <span data-ttu-id="f8783-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8783-137">RELATED LINKS</span></span>

[<span data-ttu-id="f8783-138">Get-AzureRmNotificationHubAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="f8783-138">Get-AzureRmNotificationHubAuthorizationRules</span></span>](./Get-AzureRmNotificationHubAuthorizationRules.md)

[<span data-ttu-id="f8783-139">Get-AzureRmNotificationHubListKeys</span><span class="sxs-lookup"><span data-stu-id="f8783-139">Get-AzureRmNotificationHubListKeys</span></span>](./Get-AzureRmNotificationHubListKeys.md)

[<span data-ttu-id="f8783-140">Get-AzureRmNotificationHubPNSCredentials</span><span class="sxs-lookup"><span data-stu-id="f8783-140">Get-AzureRmNotificationHubPNSCredentials</span></span>](./Get-AzureRmNotificationHubPNSCredentials.md)

[<span data-ttu-id="f8783-141">Új – AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f8783-141">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="f8783-142">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f8783-142">Remove-AzureRmNotificationHub</span></span>](./Remove-AzureRmNotificationHub.md)

[<span data-ttu-id="f8783-143">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="f8783-143">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)

