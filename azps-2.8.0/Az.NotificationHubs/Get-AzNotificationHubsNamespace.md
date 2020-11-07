---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: dbb475402ef4068f893cd7d444b5357bf1707578
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838246"
---
# <span data-ttu-id="83c4a-101">Get-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="83c4a-101">Get-AzNotificationHubsNamespace</span></span>

## <span data-ttu-id="83c4a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="83c4a-103">Információt kap az értesítési hub névteréről.</span><span class="sxs-lookup"><span data-stu-id="83c4a-103">Gets information about a notification hub namespace.</span></span>

## <span data-ttu-id="83c4a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83c4a-104">SYNTAX</span></span>

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83c4a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="83c4a-105">DESCRIPTION</span></span>
<span data-ttu-id="83c4a-106">**A Get-AzNotificationHubsNamespace** parancsmag információt kap az értesítési hub névteréről.</span><span class="sxs-lookup"><span data-stu-id="83c4a-106">**The Get-AzNotificationHubsNamespace** cmdlet gets information about notification hub namespaces.</span></span>
<span data-ttu-id="83c4a-107">Ez a parancsmag lehetőséget nyújt arra, hogy az összes névtérre vonatkozóan információt kapjanak, és hogy a megadott erőforráscsoporthoz rendelt névterekre vonatkozóan milyen információkra van szükség. vagy egy adott névtérről szóló információk visszaadására.</span><span class="sxs-lookup"><span data-stu-id="83c4a-107">This cmdlet provides you the option of getting information for all your namespaces, information about the namespaces assigned to a specified resource group; or for returning information about a specific namespace.</span></span>
<span data-ttu-id="83c4a-108">A névterek olyan logikai tárolók, amelyek megkönnyítik az értesítési hubok rendszerezését és kezelését.</span><span class="sxs-lookup"><span data-stu-id="83c4a-108">Namespaces are logical containers that help you organize and manage your notification hubs.</span></span>
<span data-ttu-id="83c4a-109">Legalább egy értesítési hub-névtérnek kell lennie: minden értesítési hubot egy névtérhez kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="83c4a-109">You must have at least one notification hub namespace: all notification hubs must be assigned to a namespace.</span></span>
<span data-ttu-id="83c4a-110">Egyetlen névtérben több hub jelenhet meg, ami azt jelenti, hogy csak egy névtérre van szüksége a szervezetében.</span><span class="sxs-lookup"><span data-stu-id="83c4a-110">A single namespace can house multiple hubs which means that you might only need one namespace in your organization.</span></span>
<span data-ttu-id="83c4a-111">Több névtér is használható azonban a hubok jobb rendszerezéséhez, vagy ha konkrét személyekre engedélyt szeretne adni a hubok kijelölt részhalmazának kezeléséhez.</span><span class="sxs-lookup"><span data-stu-id="83c4a-111">However, you can also have multiple namespaces to better organize your hubs, or to give specific individuals permission to manage a selected subset of hubs.</span></span>
<span data-ttu-id="83c4a-112">A **Get-AzNotificationHubsNamespace** parancsmag a névtérre vonatkozó alapvető információkat ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="83c4a-112">The **Get-AzNotificationHubsNamespace** cmdlet returns basic information about the namespace itself.</span></span>
<span data-ttu-id="83c4a-113">Ha a névtérhez társított engedélyezési szabályokról szeretne információt kapni, használja a Get-AzNotificationHubsNamespaceAuthorizationRulest.</span><span class="sxs-lookup"><span data-stu-id="83c4a-113">To get information about the authorization rules associated with a namespace use Get-AzNotificationHubsNamespaceAuthorizationRules.</span></span>

## <span data-ttu-id="83c4a-114">Példák</span><span class="sxs-lookup"><span data-stu-id="83c4a-114">EXAMPLES</span></span>

### <span data-ttu-id="83c4a-115">1. példa: információk kérése az összes értesítési hub-névtérről</span><span class="sxs-lookup"><span data-stu-id="83c4a-115">Example 1: Get information for all notification hub namespaces</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace
```

<span data-ttu-id="83c4a-116">Ez a parancs információt ad az összes értesítési hub-névtérről.</span><span class="sxs-lookup"><span data-stu-id="83c4a-116">This command returns information for all your notification hub namespaces.</span></span>

### <span data-ttu-id="83c4a-117">2. példa: információk beszerzése egyetlen értesítési központi névtérről</span><span class="sxs-lookup"><span data-stu-id="83c4a-117">Example 2: Get information for a single notification hub namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

<span data-ttu-id="83c4a-118">Ez a parancs egyetlen értesítési hub-névtérről kap információt: ContosoNamespace.</span><span class="sxs-lookup"><span data-stu-id="83c4a-118">This command gets information for a single notification hub namespace: ContosoNamespace.</span></span>

### <span data-ttu-id="83c4a-119">3. példa: információk kérése egy adott névtérhez rendelt minden értesítési hubhoz</span><span class="sxs-lookup"><span data-stu-id="83c4a-119">Example 3: Get information for all notification hubs assigned to a specific namespace</span></span>
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

<span data-ttu-id="83c4a-120">Ez a parancs információt kap az erőforráscsoport ContosoNotificationsGroup társított összes értesítési hub-névtérről.</span><span class="sxs-lookup"><span data-stu-id="83c4a-120">This command gets information for all notification hub namespaces assigned to the resource group ContosoNotificationsGroup.</span></span>

## <span data-ttu-id="83c4a-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83c4a-121">PARAMETERS</span></span>

### <span data-ttu-id="83c4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83c4a-122">-DefaultProfile</span></span>
<span data-ttu-id="83c4a-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="83c4a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83c4a-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="83c4a-124">-Namespace</span></span>
<span data-ttu-id="83c4a-125">A névtér egyedi nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="83c4a-125">Specifies a unique name for the namespace.</span></span>
<span data-ttu-id="83c4a-126">A névterek lehetőséget nyújtanak az értesítési hubok csoportosítására és kategorizálására.</span><span class="sxs-lookup"><span data-stu-id="83c4a-126">Namespaces provide a way to group and categorize notification hubs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83c4a-127">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="83c4a-127">-ResourceGroup</span></span>
<span data-ttu-id="83c4a-128">Azt az erőforráscsoportot adja meg, amelyhez a névtér van társítva.</span><span class="sxs-lookup"><span data-stu-id="83c4a-128">Specifies the resource group to which the namespace is assigned.</span></span>
<span data-ttu-id="83c4a-129">Az erőforráscsoportok elemek (például névterek, értesítési hubok és engedélyezési szabályok) rendszerezése olyan módon, hogy egyszerűen csak a Készletkezelés és az Azure felügyeletet segítse elő.</span><span class="sxs-lookup"><span data-stu-id="83c4a-129">Resource groups organize items such as namespaces, notification hubs, and authorization rules in ways that help simply inventory management and Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83c4a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83c4a-130">CommonParameters</span></span>
<span data-ttu-id="83c4a-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83c4a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83c4a-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83c4a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83c4a-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83c4a-133">INPUTS</span></span>

### <span data-ttu-id="83c4a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="83c4a-134">System.String</span></span>

## <span data-ttu-id="83c4a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83c4a-135">OUTPUTS</span></span>

### <span data-ttu-id="83c4a-136">Microsoft. Azure. Command. NotificationHubs. models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="83c4a-136">Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="83c4a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83c4a-137">NOTES</span></span>

## <span data-ttu-id="83c4a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83c4a-138">RELATED LINKS</span></span>

[<span data-ttu-id="83c4a-139">Get-AzNotificationHubsNamespaceAuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="83c4a-139">Get-AzNotificationHubsNamespaceAuthorizationRules</span></span>](./Get-AzNotificationHubsNamespaceAuthorizationRules.md)

[<span data-ttu-id="83c4a-140">Új – AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="83c4a-140">New-AzNotificationHubsNamespace</span></span>](./New-AzNotificationHubsNamespace.md)

[<span data-ttu-id="83c4a-141">Remove-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="83c4a-141">Remove-AzNotificationHubsNamespace</span></span>](./Remove-AzNotificationHubsNamespace.md)

[<span data-ttu-id="83c4a-142">Set-AzNotificationHubsNamespace</span><span class="sxs-lookup"><span data-stu-id="83c4a-142">Set-AzNotificationHubsNamespace</span></span>](./Set-AzNotificationHubsNamespace.md)


