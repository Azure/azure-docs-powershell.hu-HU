---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/remove-azurermnotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
ms.openlocfilehash: f4dc14fd922852fa67085588c78847623eb5eb64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495828"
---
# <span data-ttu-id="0bd38-101">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0bd38-101">Remove-AzureRmNotificationHub</span></span>

## <span data-ttu-id="0bd38-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0bd38-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd38-103">Egy meglévő értesítési hub eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="0bd38-103">Removes an existing notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bd38-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0bd38-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bd38-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0bd38-105">DESCRIPTION</span></span>
<span data-ttu-id="0bd38-106">A **Remove-AzureRmNotificationHub** parancsmag eltávolít egy meglévő értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="0bd38-106">The **Remove-AzureRmNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="0bd38-107">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="0bd38-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="0bd38-108">A platformokon megtalálható a következők: iOS, Android, Windows Phone 8 és Windows áruház.</span><span class="sxs-lookup"><span data-stu-id="0bd38-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="0bd38-109">Az értesítési hubok nagyjából egyenértékűek az egyes alkalmazásokkal: az egyes alkalmazások általában saját értesítési központtal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="0bd38-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="0bd38-110">A **Remove-AzureRmNotificationHub** parancsmag használatával eltávolíthatja a meglévő értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="0bd38-110">You can remove an existing notification hub by using the **Remove-AzureRmNotificationHub** cmdlet.</span></span>
<span data-ttu-id="0bd38-111">A hub eltávolítását követően már nem használhatja azt a hub-ot, amellyel leküldéses értesítéseket küldhet a felhasználóknak.</span><span class="sxs-lookup"><span data-stu-id="0bd38-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="0bd38-112">Példák</span><span class="sxs-lookup"><span data-stu-id="0bd38-112">EXAMPLES</span></span>

### <span data-ttu-id="0bd38-113">1. példa: az értesítési központ eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0bd38-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="0bd38-114">Ez a parancs eltávolítja a ContosoInternalHub nevű értesítési hubot.</span><span class="sxs-lookup"><span data-stu-id="0bd38-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="0bd38-115">A hub eltávolításához meg kell adnia azt a névteret, ahol a hub található, valamint a hub által hozzárendelt erőforrás csoport.</span><span class="sxs-lookup"><span data-stu-id="0bd38-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="0bd38-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0bd38-116">PARAMETERS</span></span>

### <span data-ttu-id="0bd38-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd38-117">-DefaultProfile</span></span>
<span data-ttu-id="0bd38-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0bd38-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bd38-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0bd38-119">-Force</span></span>
<span data-ttu-id="0bd38-120">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0bd38-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0bd38-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0bd38-121">-Namespace</span></span>
<span data-ttu-id="0bd38-122">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="0bd38-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="0bd38-123">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="0bd38-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="0bd38-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="0bd38-124">-NotificationHub</span></span>
<span data-ttu-id="0bd38-125">Az eltávolítandó értesítési csomópontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="0bd38-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="0bd38-126">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="0bd38-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="0bd38-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0bd38-127">-ResourceGroup</span></span>
<span data-ttu-id="0bd38-128">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="0bd38-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="0bd38-129">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="0bd38-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="0bd38-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="0bd38-130">-Confirm</span></span>
<span data-ttu-id="0bd38-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0bd38-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bd38-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bd38-132">-WhatIf</span></span>
<span data-ttu-id="0bd38-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="0bd38-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0bd38-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0bd38-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bd38-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd38-135">CommonParameters</span></span>
<span data-ttu-id="0bd38-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0bd38-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd38-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bd38-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd38-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bd38-138">INPUTS</span></span>

### <span data-ttu-id="0bd38-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0bd38-139">System.String</span></span>

## <span data-ttu-id="0bd38-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0bd38-140">OUTPUTS</span></span>

### <span data-ttu-id="0bd38-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="0bd38-141">System.Void</span></span>

## <span data-ttu-id="0bd38-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0bd38-142">NOTES</span></span>

## <span data-ttu-id="0bd38-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0bd38-143">RELATED LINKS</span></span>

[<span data-ttu-id="0bd38-144">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0bd38-144">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="0bd38-145">Új – AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0bd38-145">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="0bd38-146">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0bd38-146">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


