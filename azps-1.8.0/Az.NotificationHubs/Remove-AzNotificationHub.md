---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: c3740884d49683b7990aea1ed7543f39a4ccf80f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669887"
---
# <span data-ttu-id="91d2d-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="91d2d-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="91d2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91d2d-102">SYNOPSIS</span></span>
<span data-ttu-id="91d2d-103">Egy meglévő értesítési hub eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="91d2d-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="91d2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91d2d-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91d2d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="91d2d-105">DESCRIPTION</span></span>
<span data-ttu-id="91d2d-106">A **Remove-AzNotificationHub** parancsmag eltávolít egy meglévő értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="91d2d-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="91d2d-107">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="91d2d-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="91d2d-108">A platformokon megtalálható a következők: iOS, Android, Windows Phone 8 és Windows áruház.</span><span class="sxs-lookup"><span data-stu-id="91d2d-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="91d2d-109">Az értesítési hubok nagyjából egyenértékűek az egyes alkalmazásokkal: az egyes alkalmazások általában saját értesítési központtal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="91d2d-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="91d2d-110">A **Remove-AzNotificationHub** parancsmag használatával eltávolíthatja a meglévő értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="91d2d-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="91d2d-111">A hub eltávolítását követően már nem használhatja azt a hub-ot, amellyel leküldéses értesítéseket küldhet a felhasználóknak.</span><span class="sxs-lookup"><span data-stu-id="91d2d-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="91d2d-112">Példák</span><span class="sxs-lookup"><span data-stu-id="91d2d-112">EXAMPLES</span></span>

### <span data-ttu-id="91d2d-113">1. példa: az értesítési központ eltávolítása</span><span class="sxs-lookup"><span data-stu-id="91d2d-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="91d2d-114">Ez a parancs eltávolítja a ContosoInternalHub nevű értesítési hubot.</span><span class="sxs-lookup"><span data-stu-id="91d2d-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="91d2d-115">A hub eltávolításához meg kell adnia azt a névteret, ahol a hub található, valamint a hub által hozzárendelt erőforrás csoport.</span><span class="sxs-lookup"><span data-stu-id="91d2d-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="91d2d-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91d2d-116">PARAMETERS</span></span>

### <span data-ttu-id="91d2d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d2d-117">-DefaultProfile</span></span>
<span data-ttu-id="91d2d-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="91d2d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91d2d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="91d2d-119">-Force</span></span>
<span data-ttu-id="91d2d-120">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="91d2d-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="91d2d-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="91d2d-121">-Namespace</span></span>
<span data-ttu-id="91d2d-122">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="91d2d-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="91d2d-123">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="91d2d-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="91d2d-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="91d2d-124">-NotificationHub</span></span>
<span data-ttu-id="91d2d-125">Az eltávolítandó értesítési csomópontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="91d2d-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="91d2d-126">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="91d2d-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="91d2d-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="91d2d-127">-ResourceGroup</span></span>
<span data-ttu-id="91d2d-128">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="91d2d-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="91d2d-129">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="91d2d-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="91d2d-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="91d2d-130">-Confirm</span></span>
<span data-ttu-id="91d2d-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="91d2d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91d2d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91d2d-132">-WhatIf</span></span>
<span data-ttu-id="91d2d-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="91d2d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91d2d-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="91d2d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91d2d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d2d-135">CommonParameters</span></span>
<span data-ttu-id="91d2d-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91d2d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d2d-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91d2d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d2d-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91d2d-138">INPUTS</span></span>

### <span data-ttu-id="91d2d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="91d2d-139">System.String</span></span>

## <span data-ttu-id="91d2d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91d2d-140">OUTPUTS</span></span>

### <span data-ttu-id="91d2d-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="91d2d-141">System.Void</span></span>

## <span data-ttu-id="91d2d-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91d2d-142">NOTES</span></span>

## <span data-ttu-id="91d2d-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91d2d-143">RELATED LINKS</span></span>

[<span data-ttu-id="91d2d-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="91d2d-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="91d2d-145">Új – AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="91d2d-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="91d2d-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="91d2d-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


