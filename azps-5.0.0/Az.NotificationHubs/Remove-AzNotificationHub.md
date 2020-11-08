---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: 66f3dae7d92b9db18db418bf9de62671f084b7c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186045"
---
# <span data-ttu-id="d87db-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d87db-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="d87db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d87db-102">SYNOPSIS</span></span>
<span data-ttu-id="d87db-103">Egy meglévő értesítési hub eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="d87db-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="d87db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d87db-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d87db-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d87db-105">DESCRIPTION</span></span>
<span data-ttu-id="d87db-106">A **Remove-AzNotificationHub** parancsmag eltávolít egy meglévő értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="d87db-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="d87db-107">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="d87db-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="d87db-108">A platformokon megtalálható a következők: iOS, Android, Windows Phone 8 és Windows áruház.</span><span class="sxs-lookup"><span data-stu-id="d87db-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="d87db-109">Az értesítési hubok nagyjából egyenértékűek az egyes alkalmazásokkal: az egyes alkalmazások általában saját értesítési központtal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="d87db-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="d87db-110">A **Remove-AzNotificationHub** parancsmag használatával eltávolíthatja a meglévő értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="d87db-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="d87db-111">A hub eltávolítását követően már nem használhatja azt a hub-ot, amellyel leküldéses értesítéseket küldhet a felhasználóknak.</span><span class="sxs-lookup"><span data-stu-id="d87db-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="d87db-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d87db-112">EXAMPLES</span></span>

### <span data-ttu-id="d87db-113">1. példa: az értesítési központ eltávolítása</span><span class="sxs-lookup"><span data-stu-id="d87db-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="d87db-114">Ez a parancs eltávolítja a ContosoInternalHub nevű értesítési hubot.</span><span class="sxs-lookup"><span data-stu-id="d87db-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="d87db-115">A hub eltávolításához meg kell adnia azt a névteret, ahol a hub található, valamint a hub által hozzárendelt erőforrás csoport.</span><span class="sxs-lookup"><span data-stu-id="d87db-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="d87db-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d87db-116">PARAMETERS</span></span>

### <span data-ttu-id="d87db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d87db-117">-DefaultProfile</span></span>
<span data-ttu-id="d87db-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d87db-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d87db-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d87db-119">-Force</span></span>
<span data-ttu-id="d87db-120">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d87db-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d87db-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d87db-121">-Namespace</span></span>
<span data-ttu-id="d87db-122">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="d87db-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="d87db-123">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="d87db-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="d87db-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="d87db-124">-NotificationHub</span></span>
<span data-ttu-id="d87db-125">Az eltávolítandó értesítési csomópontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="d87db-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="d87db-126">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="d87db-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="d87db-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d87db-127">-ResourceGroup</span></span>
<span data-ttu-id="d87db-128">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="d87db-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="d87db-129">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="d87db-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="d87db-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d87db-130">-Confirm</span></span>
<span data-ttu-id="d87db-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d87db-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d87db-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d87db-132">-WhatIf</span></span>
<span data-ttu-id="d87db-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d87db-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d87db-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d87db-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d87db-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d87db-135">CommonParameters</span></span>
<span data-ttu-id="d87db-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d87db-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d87db-137">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d87db-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d87db-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d87db-138">INPUTS</span></span>

### <span data-ttu-id="d87db-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d87db-139">System.String</span></span>

## <span data-ttu-id="d87db-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d87db-140">OUTPUTS</span></span>

### <span data-ttu-id="d87db-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="d87db-141">System.Void</span></span>

## <span data-ttu-id="d87db-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d87db-142">NOTES</span></span>

## <span data-ttu-id="d87db-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d87db-143">RELATED LINKS</span></span>

[<span data-ttu-id="d87db-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d87db-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="d87db-145">Új – AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d87db-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="d87db-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="d87db-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


