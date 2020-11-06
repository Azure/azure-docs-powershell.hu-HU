---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHub.md
ms.openlocfilehash: b0911045313b26b19fd1de70af926e8c8e066ca8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494781"
---
# <span data-ttu-id="94586-101">Remove-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="94586-101">Remove-AzureRmNotificationHub</span></span>

## <span data-ttu-id="94586-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="94586-102">SYNOPSIS</span></span>
<span data-ttu-id="94586-103">Egy meglévő értesítési hub eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="94586-103">Removes an existing notification hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94586-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="94586-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94586-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="94586-105">DESCRIPTION</span></span>
<span data-ttu-id="94586-106">A **Remove-AzureRmNotificationHub** parancsmag eltávolít egy meglévő értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="94586-106">The **Remove-AzureRmNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="94586-107">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="94586-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="94586-108">A platformokon megtalálható a következők: iOS, Android, Windows Phone 8 és Windows áruház.</span><span class="sxs-lookup"><span data-stu-id="94586-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="94586-109">Az értesítési hubok nagyjából egyenértékűek az egyes alkalmazásokkal: az egyes alkalmazások általában saját értesítési központtal rendelkeznek.</span><span class="sxs-lookup"><span data-stu-id="94586-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>

<span data-ttu-id="94586-110">A **Remove-AzureRmNotificationHub** parancsmag használatával eltávolíthatja a meglévő értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="94586-110">You can remove an existing notification hub by using the **Remove-AzureRmNotificationHub** cmdlet.</span></span>
<span data-ttu-id="94586-111">A hub eltávolítását követően már nem használhatja azt a hub-ot, amellyel leküldéses értesítéseket küldhet a felhasználóknak.</span><span class="sxs-lookup"><span data-stu-id="94586-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="94586-112">Példák</span><span class="sxs-lookup"><span data-stu-id="94586-112">EXAMPLES</span></span>

### <span data-ttu-id="94586-113">1. példa: az értesítési központ eltávolítása</span><span class="sxs-lookup"><span data-stu-id="94586-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="94586-114">Ez a parancs eltávolítja a ContosoInternalHub nevű értesítési hubot.</span><span class="sxs-lookup"><span data-stu-id="94586-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="94586-115">A hub eltávolításához meg kell adnia azt a névteret, ahol a hub található, valamint a hub által hozzárendelt erőforrás csoport.</span><span class="sxs-lookup"><span data-stu-id="94586-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="94586-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="94586-116">PARAMETERS</span></span>

### <span data-ttu-id="94586-117">-Force</span><span class="sxs-lookup"><span data-stu-id="94586-117">-Force</span></span>
<span data-ttu-id="94586-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94586-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="94586-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="94586-119">-Namespace</span></span>
<span data-ttu-id="94586-120">Azt a névteret adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="94586-120">Specifies the namespace to which the notification hub is assigned.</span></span>

<span data-ttu-id="94586-121">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="94586-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="94586-122">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="94586-122">-NotificationHub</span></span>
<span data-ttu-id="94586-123">Az eltávolítandó értesítési csomópontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="94586-123">Specifies the notification hub to be removed.</span></span>

<span data-ttu-id="94586-124">Az értesítési hubok az ügyfelek által használt platformtól függetlenül több ügyfélnek küldenek leküldéses értesítéseket.</span><span class="sxs-lookup"><span data-stu-id="94586-124">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="94586-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94586-125">-ResourceGroup</span></span>
<span data-ttu-id="94586-126">Azt az erőforráscsoport-csoportot adja meg, amelyhez az értesítési hub hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="94586-126">Specifies the resource group to which the notification hub is assigned.</span></span>

<span data-ttu-id="94586-127">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="94586-127">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="94586-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="94586-128">-Confirm</span></span>
<span data-ttu-id="94586-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="94586-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94586-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94586-130">-WhatIf</span></span>
<span data-ttu-id="94586-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="94586-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94586-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="94586-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94586-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94586-133">-DefaultProfile</span></span>
<span data-ttu-id="94586-134">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="94586-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94586-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94586-135">CommonParameters</span></span>
<span data-ttu-id="94586-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="94586-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94586-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94586-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94586-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="94586-138">INPUTS</span></span>

## <span data-ttu-id="94586-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="94586-139">OUTPUTS</span></span>

## <span data-ttu-id="94586-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="94586-140">NOTES</span></span>

## <span data-ttu-id="94586-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="94586-141">RELATED LINKS</span></span>

[<span data-ttu-id="94586-142">Get-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="94586-142">Get-AzureRmNotificationHub</span></span>](./Get-AzureRmNotificationHub.md)

[<span data-ttu-id="94586-143">Új – AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="94586-143">New-AzureRmNotificationHub</span></span>](./New-AzureRmNotificationHub.md)

[<span data-ttu-id="94586-144">Set-AzureRmNotificationHub</span><span class="sxs-lookup"><span data-stu-id="94586-144">Set-AzureRmNotificationHub</span></span>](./Set-AzureRmNotificationHub.md)


