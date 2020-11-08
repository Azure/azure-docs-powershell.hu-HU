---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/remove-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Remove-AzNotificationHubsNamespace.md
ms.openlocfilehash: e03be5a1daae753e1538b171586d9a8e46ad8021
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184306"
---
# <span data-ttu-id="61aca-101">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="61aca-101">Remove-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="61aca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="61aca-102">SYNOPSIS</span></span>
<span data-ttu-id="61aca-103">Az értesítési hub névterének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="61aca-103">Removes a notification hub namespace.</span></span>

## <span data-ttu-id="61aca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="61aca-104">SYNTAX</span></span>

```
Remove-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61aca-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="61aca-105">DESCRIPTION</span></span>
<span data-ttu-id="61aca-106">A **Remove-AzNotificationHubsNamespace** parancsmag eltávolítja az értesítési hub névterét a központi telepítőből.</span><span class="sxs-lookup"><span data-stu-id="61aca-106">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="61aca-107">A névterek olyan logikai tárolók, amelyek megkönnyítik az értesítési hubok rendszerezését és kezelését.</span><span class="sxs-lookup"><span data-stu-id="61aca-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="61aca-108">A **Remove-AzNotificationHubsNamespace** parancsmag eltávolítja az értesítési hub névterét a központi telepítőből.</span><span class="sxs-lookup"><span data-stu-id="61aca-108">The **Remove-AzNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="61aca-109">Ha futtatja ezt a parancsmagot, a megadott névtér törlődik az adott névtérhez társított összes értesítési csomóponttal együtt.</span><span class="sxs-lookup"><span data-stu-id="61aca-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="61aca-110">Példák</span><span class="sxs-lookup"><span data-stu-id="61aca-110">EXAMPLES</span></span>

### <span data-ttu-id="61aca-111">1. példa: értesítési hub-névtér eltávolítása</span><span class="sxs-lookup"><span data-stu-id="61aca-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="61aca-112">Ez a parancs eltávolítja a ContosoNamespace nevű névteret.</span><span class="sxs-lookup"><span data-stu-id="61aca-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="61aca-113">Meg kell adnia a névtérhez rendelt erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="61aca-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="61aca-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="61aca-114">PARAMETERS</span></span>

### <span data-ttu-id="61aca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61aca-115">-DefaultProfile</span></span>
<span data-ttu-id="61aca-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="61aca-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61aca-117">-Force</span><span class="sxs-lookup"><span data-stu-id="61aca-117">-Force</span></span>
<span data-ttu-id="61aca-118">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="61aca-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="61aca-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="61aca-119">-Namespace</span></span>
<span data-ttu-id="61aca-120">A parancsmag által eltávolított névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="61aca-120">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="61aca-121">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="61aca-121">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="61aca-122">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="61aca-122">-ResourceGroup</span></span>
<span data-ttu-id="61aca-123">Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.</span><span class="sxs-lookup"><span data-stu-id="61aca-123">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="61aca-124">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="61aca-124">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="61aca-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="61aca-125">-Confirm</span></span>
<span data-ttu-id="61aca-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="61aca-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61aca-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61aca-127">-WhatIf</span></span>
<span data-ttu-id="61aca-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="61aca-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61aca-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="61aca-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61aca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61aca-130">CommonParameters</span></span>
<span data-ttu-id="61aca-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="61aca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61aca-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61aca-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61aca-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="61aca-133">INPUTS</span></span>

### <span data-ttu-id="61aca-134">System. String</span><span class="sxs-lookup"><span data-stu-id="61aca-134">System.String</span></span>

## <span data-ttu-id="61aca-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61aca-135">OUTPUTS</span></span>

### <span data-ttu-id="61aca-136">System. Void</span><span class="sxs-lookup"><span data-stu-id="61aca-136">System.Void</span></span>

## <span data-ttu-id="61aca-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="61aca-137">NOTES</span></span>

## <span data-ttu-id="61aca-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61aca-138">RELATED LINKS</span></span>

[<span data-ttu-id="61aca-139">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="61aca-139">Get-AzNotificationHubsNamespace</span></span>](./Get-AzNotificationHubsNamespace.md)

[<span data-ttu-id="61aca-140">Új – AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="61aca-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="61aca-141">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="61aca-141">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


