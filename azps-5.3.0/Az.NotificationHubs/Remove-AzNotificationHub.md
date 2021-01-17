---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 62631E1C-FB43-4E87-82C2-159A9D1D4221
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHub.md
ms.openlocfilehash: 66f3dae7d92b9db18db418bf9de62671f084b7c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385110"
---
# <span data-ttu-id="0c618-101">Remove-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0c618-101">Remove-AzNotificationHub</span></span>

## <span data-ttu-id="0c618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c618-102">SYNOPSIS</span></span>
<span data-ttu-id="0c618-103">Eltávolít egy meglévő értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="0c618-103">Removes an existing notification hub.</span></span>

## <span data-ttu-id="0c618-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0c618-104">SYNTAX</span></span>

```
Remove-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c618-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0c618-105">DESCRIPTION</span></span>
<span data-ttu-id="0c618-106">A **Remove-AzNotificationHub** parancsmag eltávolít egy meglévő értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="0c618-106">The **Remove-AzNotificationHub** cmdlet removes an existing notification hub.</span></span>
<span data-ttu-id="0c618-107">Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek attól függetlenül, hogy milyen platformon használják őket.</span><span class="sxs-lookup"><span data-stu-id="0c618-107">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>
<span data-ttu-id="0c618-108">A platformok többek között a következők: iOS, Android, Windows Phone 8 és Windows Áruház.</span><span class="sxs-lookup"><span data-stu-id="0c618-108">Platforms include, but are not limited to: iOS, Android, Windows Phone 8, and Windows Store.</span></span>
<span data-ttu-id="0c618-109">Az értesítési központok nagyjából egyenértékűek az egyes appokkal: mindegyik alkalmazásnak általában saját értesítési központja lesz.</span><span class="sxs-lookup"><span data-stu-id="0c618-109">Notification hubs are roughly equivalent to individual apps: each of your apps will typically have its own notification hub.</span></span>
<span data-ttu-id="0c618-110">A **Remove-AzNotificationHub** parancsmag használatával eltávolíthat egy meglévő értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="0c618-110">You can remove an existing notification hub by using the **Remove-AzNotificationHub** cmdlet.</span></span>
<span data-ttu-id="0c618-111">Miután eltávolított egy központot, már nem használhatja azt a központot leküldéses értesítések küldére a felhasználóknak.</span><span class="sxs-lookup"><span data-stu-id="0c618-111">After a hub has been removed you can no longer use that hub to send push notifications to users.</span></span>

## <span data-ttu-id="0c618-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0c618-112">EXAMPLES</span></span>

### <span data-ttu-id="0c618-113">1. példa: Értesítési központ eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0c618-113">Example 1: Remove a notification hub</span></span>
```
PS C:\>Remove-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

<span data-ttu-id="0c618-114">Ez a parancs eltávolítja a ContosoInternalHub nevű értesítési központot.</span><span class="sxs-lookup"><span data-stu-id="0c618-114">This command removes the notification hub named ContosoInternalHub.</span></span>
<span data-ttu-id="0c618-115">A központ eltávolításához meg kell adnia a központ helyének névterét, valamint azt az erőforráscsoportot, amelyhez a központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="0c618-115">In order to remove the hub, you must specify the namespace where the hub is located as well as the resource group the hub is assigned to.</span></span>

## <span data-ttu-id="0c618-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c618-116">PARAMETERS</span></span>

### <span data-ttu-id="0c618-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c618-117">-DefaultProfile</span></span>
<span data-ttu-id="0c618-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0c618-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c618-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0c618-119">-Force</span></span>
<span data-ttu-id="0c618-120">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="0c618-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0c618-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0c618-121">-Namespace</span></span>
<span data-ttu-id="0c618-122">Azt a névteret adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="0c618-122">Specifies the namespace to which the notification hub is assigned.</span></span>
<span data-ttu-id="0c618-123">A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="0c618-123">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="0c618-124">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="0c618-124">-NotificationHub</span></span>
<span data-ttu-id="0c618-125">Az eltávolítható értesítési központot határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0c618-125">Specifies the notification hub to be removed.</span></span>
<span data-ttu-id="0c618-126">Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek attól függetlenül, hogy milyen platformon használják őket.</span><span class="sxs-lookup"><span data-stu-id="0c618-126">Notification hubs are used to send push notifications to multiple clients regardless of the platform used by those clients.</span></span>

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

### <span data-ttu-id="0c618-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0c618-127">-ResourceGroup</span></span>
<span data-ttu-id="0c618-128">Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="0c618-128">Specifies the resource group to which the notification hub is assigned.</span></span>
<span data-ttu-id="0c618-129">Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.</span><span class="sxs-lookup"><span data-stu-id="0c618-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="0c618-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c618-130">-Confirm</span></span>
<span data-ttu-id="0c618-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0c618-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c618-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c618-132">-WhatIf</span></span>
<span data-ttu-id="0c618-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0c618-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c618-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c618-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c618-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c618-135">CommonParameters</span></span>
<span data-ttu-id="0c618-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c618-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c618-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c618-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c618-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c618-138">INPUTS</span></span>

### <span data-ttu-id="0c618-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0c618-139">System.String</span></span>

## <span data-ttu-id="0c618-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c618-140">OUTPUTS</span></span>

### <span data-ttu-id="0c618-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="0c618-141">System.Void</span></span>

## <span data-ttu-id="0c618-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0c618-142">NOTES</span></span>

## <span data-ttu-id="0c618-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c618-143">RELATED LINKS</span></span>

[<span data-ttu-id="0c618-144">Get-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0c618-144">Get-AzNotificationHub</span></span>](./Get-AzNotificationHub.md)

[<span data-ttu-id="0c618-145">New-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0c618-145">New-AzNotificationHub</span></span>](./New-AzNotificationHub.md)

[<span data-ttu-id="0c618-146">Set-AzNotificationHub</span><span class="sxs-lookup"><span data-stu-id="0c618-146">Set-AzNotificationHub</span></span>](./Set-AzNotificationHub.md)


