---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 5EDFBF19-928F-4F95-BD93-CF8BAEA11C52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Remove-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: ff315c7f3634c0a8a4afd5c4b54926c0a260ed75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494776"
---
# <span data-ttu-id="72e4d-101">Remove-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="72e4d-101">Remove-AzureRmNotificationHubsNamespace</span></span>

## <span data-ttu-id="72e4d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="72e4d-103">Az értesítési hub névterének eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="72e4d-103">Removes a notification hub namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72e4d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72e4d-104">SYNTAX</span></span>

```
Remove-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72e4d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="72e4d-105">DESCRIPTION</span></span>
<span data-ttu-id="72e4d-106">A **Remove-AzureRmNotificationHubsNamespace** parancsmag eltávolítja az értesítési hub névterét a központi telepítőből.</span><span class="sxs-lookup"><span data-stu-id="72e4d-106">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>

<span data-ttu-id="72e4d-107">A névterek olyan logikai tárolók, amelyek megkönnyítik az értesítési hubok rendszerezését és kezelését.</span><span class="sxs-lookup"><span data-stu-id="72e4d-107">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="72e4d-108">A **Remove-AzureRmNotificationHubsNamespace** parancsmag eltávolítja az értesítési hub névterét a központi telepítőből.</span><span class="sxs-lookup"><span data-stu-id="72e4d-108">The **Remove-AzureRmNotificationHubsNamespace** cmdlet removes a notification hub namespace from your deployment.</span></span>
<span data-ttu-id="72e4d-109">Ha futtatja ezt a parancsmagot, a megadott névtér törlődik az adott névtérhez társított összes értesítési csomóponttal együtt.</span><span class="sxs-lookup"><span data-stu-id="72e4d-109">When you run this cmdlet, the specified namespace will be deleted along with all the notification hubs associated with that namespace.</span></span>

## <span data-ttu-id="72e4d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="72e4d-110">EXAMPLES</span></span>

### <span data-ttu-id="72e4d-111">1. példa: értesítési hub-névtér eltávolítása</span><span class="sxs-lookup"><span data-stu-id="72e4d-111">Example 1: Remove a notification hub namespace</span></span>
```
PS C:\>Remove-AzureRmNotificationHubsNamespace -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="72e4d-112">Ez a parancs eltávolítja a ContosoNamespace nevű névteret.</span><span class="sxs-lookup"><span data-stu-id="72e4d-112">This command removes the namespace named ContosoNamespace.</span></span>
<span data-ttu-id="72e4d-113">Meg kell adnia a névtérhez rendelt erőforráscsoportot.</span><span class="sxs-lookup"><span data-stu-id="72e4d-113">You must specify the resource group the namespace is assigned to.</span></span>

## <span data-ttu-id="72e4d-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72e4d-114">PARAMETERS</span></span>

### <span data-ttu-id="72e4d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="72e4d-115">-Force</span></span>
<span data-ttu-id="72e4d-116">Ne kérjen megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72e4d-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="72e4d-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="72e4d-117">-Namespace</span></span>
<span data-ttu-id="72e4d-118">A parancsmag által eltávolított névteret adja meg.</span><span class="sxs-lookup"><span data-stu-id="72e4d-118">Specifies the namespace that this cmdlet removes.</span></span>
<span data-ttu-id="72e4d-119">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="72e4d-119">Namespaces provide a way to group and categorize notification hubs.</span></span>

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

### <span data-ttu-id="72e4d-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72e4d-120">-ResourceGroup</span></span>
<span data-ttu-id="72e4d-121">Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.</span><span class="sxs-lookup"><span data-stu-id="72e4d-121">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="72e4d-122">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="72e4d-122">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

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

### <span data-ttu-id="72e4d-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="72e4d-123">-Confirm</span></span>
<span data-ttu-id="72e4d-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72e4d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72e4d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72e4d-125">-WhatIf</span></span>
<span data-ttu-id="72e4d-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="72e4d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72e4d-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="72e4d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72e4d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e4d-128">-DefaultProfile</span></span>
<span data-ttu-id="72e4d-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72e4d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72e4d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e4d-130">CommonParameters</span></span>
<span data-ttu-id="72e4d-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72e4d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e4d-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72e4d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e4d-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72e4d-133">INPUTS</span></span>

## <span data-ttu-id="72e4d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72e4d-134">OUTPUTS</span></span>

## <span data-ttu-id="72e4d-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72e4d-135">NOTES</span></span>

## <span data-ttu-id="72e4d-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72e4d-136">RELATED LINKS</span></span>

[<span data-ttu-id="72e4d-137">Get-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="72e4d-137">Get-AzureRmNotificationHubsNamespace</span></span>](./Get-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="72e4d-138">Új – AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="72e4d-138">New-AzureRmNotificationHubsNamespace</span></span>](./New-AzureRmNotificationHubsNamespace.md)

[<span data-ttu-id="72e4d-139">Set-AzureRmNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="72e4d-139">Set-AzureRmNotificationHubsNamespace</span></span>](./Set-AzureRmNotificationHubsNamespace.md)


